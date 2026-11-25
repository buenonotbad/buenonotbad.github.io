---
layout: page
title: Neural Implicit Field Topology Optimization
description: Reducing the error tail of neural implicit topology optimization · individual research paper · UB, 2026
img: assets/img/projects/neural_topo/examples.png # thumbnail
importance: 1
category: AI
related_publications: false
---

Individual research project · University at Buffalo · 2026<br>
Sole author: method, experiments, and writing. Started as a course project in High Performance Computing II.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/neural_topo/examples.png" caption="Selected test problems at the same amount of material (red arrow: load, green: supports). Plain fine-tuning (middle) leaves a member broken or missing; skeleton-guided fine-tuning (bottom) keeps the load path connected. CE: compliance error vs the SIMP reference." class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Neural networks can predict a near-optimal structural layout in a single forward pass, instead of the hundreds of
finite-element analyses (FEA) that classical topology optimization (SIMP) needs. On average they are already very good:
for NITO [1], a neural implicit model, the median compliance error is below **1%**. The problem is the **tail**: a few percent
of the predicted designs miss a member or break a load path, and their compliance is **more than double** the SIMP reference.
In structural design, one broken load path can make a design unusable, so the tail matters more than the average.

This project targets that tail. All models are compared at the **same amount of material**, since adding material lowers
compliance by itself and can make any method look better.

### Skeleton-guided fine-tuning

Pixel-wise training losses treat every pixel the same, but most pixel errors are either harmless or easy to fix. The
failures are missing **centerlines**, often of thin strut-like members. I fine-tune NITO with an extra term that rewards
material on the skeleton of every member of the reference design (a Skeleton Recall loss [2]), which needs only the
reference design and no FEA during training.

With every design cut at exactly its target volume, the 90th percentile of the compliance error drops from **16.8% to 10.2%**
(1,000 test problems, 3 seeds; the 95% confidence interval of the gain excludes zero in every seed).

Losses that re-weight pixels (by load path, thin members, optimality conditions, or focal loss) do not achieve this: they
only shift the binarization threshold locally, moving the model along the baseline's compliance–material curve.

### Calibrated thresholding

Network outputs are continuous densities that must be thresholded into a solid/void design. Instead of the usual fixed
0.5, I calibrate one global threshold per material budget on validation problems; on new problems it hits the target volume
within **0.1 percentage points**. At the same average material and at negligible extra cost, it yields a smaller error tail
than cutting each design at its own target volume, because the network's uncertainty steers the extra material to the
hardest problems.

<!-- col-sm-7 ≈ 60% width on desktop, full width on phones; margin auto centers it -->
<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0" style="margin: 0 auto">
        {% include figure.liquid path="assets/img/projects/neural_topo/budget.png" caption="Compliance-error tail vs extra material budget. Solid: calibrated global threshold; dashed: every design cut at its own volume." class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Warm start for SIMP

On problems like its training data, the network output plus **5 SIMP iterations** already has a smaller error tail than
plain SIMP after **200 iterations** (200 FEA runs), and the skeleton-guided model saves one to two more iterations when the
FEA budget is small.

On textbook problems unlike the training data, a cheap connectivity check catches broken network designs and falls back to plain SIMP, so the pipeline is no worse than SIMP alone.

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0" style="margin: 0 auto">
        {% include figure.liquid path="assets/img/projects/neural_topo/warmstart.png" caption="Error tail vs number of FEA per problem. At 0 FEA the network output is binarized at 0.5." class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Acknowledgments

I thank Prof. Matthew G. Knepley for his helpful feedback on this project in the High Performance Computing II course.

### Manuscript

```bibtex
@unpublished{huang2026reducing,
  author = {Huang, Yixiao},
  title  = {Reducing the Error Tail of Neural Implicit Topology Optimization: Skeleton-Guided Fine-Tuning and Calibrated Thresholding},
  year   = {2026},
  note   = {Manuscript in preparation}
}
```

### References

1. A. H. Nobari, G. Giannone, L. Regenwetter, F. Ahmed. NITO: Neural Implicit Fields for Resolution-Free and Domain-Adaptable
   Topology Optimization. _Transactions on Machine Learning Research_ (2025). [arXiv:2402.05073](https://arxiv.org/abs/2402.05073)
2. Y. Kirchhoff et al. Skeleton Recall Loss for Connectivity Conserving and Resource Efficient Segmentation of Thin Tubular
   Structures. _ECCV 2024_. [arXiv:2404.03010](https://arxiv.org/abs/2404.03010)
3. R. V. Woldseth, N. Aage, J. A. Baerentzen, O. Sigmund. On the use of artificial neural networks in topology optimisation.
   _Structural and Multidisciplinary Optimization_ 65, 294 (2022). [doi:10.1007/s00158-022-03347-1](https://doi.org/10.1007/s00158-022-03347-1)
