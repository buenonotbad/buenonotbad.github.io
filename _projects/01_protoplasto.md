---
layout: page
title: Prōtóplasto
description: Hollow-core 3D printed pavilion · team project · ETH Zürich, 2023
img: assets/img/projects/protoplasto/demo1.jpg # thumbnail
importance: 1
category: Robotic Fabrication
related_publications: false
images:
  slider: true
---

Team research project @ ETH Zürich · Spring 2023<br>
**Role** · Programming · Canopy design · Robotic fabrication · Digital assembly

{% comment %} pdf p.31 {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/protoplasto/demo1.jpg" caption="The first demonstrator: an HC3DP column carrying a space-frame canopy" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Prōtóplasto explores fast robotic fabrication of lightweight, non-load-bearing building components with Large-Scale Hollow-Core 3D Printing (HC3DP),
combined with digital assembly for quick deployment. The prototype is a pavilion in three parts: HC3DP columns, a canopy of robot-cut fiberglass pipes
joined by jet-fusion 3D-printed nodes, and crowns that connect the canopy to each column.

{% include video.liquid path="https://www.youtube.com/embed/0PFK9tWmeIU" class="img-fluid rounded z-depth-1" width="100%" height="400" %}

### Hollow-core 3D printing (HC3DP)

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" rewind="true">
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/hollow_core.jpg" caption="Hollow-core printed samples" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/hollow_core_section.png" caption="Cross-sections of printed samples" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/hollow_core_texture.jpg" caption="Tapered cross-section column" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/hollow_core_extrusion.jpg" caption="Extrusion" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/hollow_core_deformation.jpg" caption="Printed samples" class="img-fluid rounded z-depth-1" %}</swiper-slide>
</swiper-container>

### Space-frame design

Three tree-like units, each on a $2.5$ m column, share one canopy of roughly $10 × 10$ m. The space frame is modularized for radial, self-interlocking,
scaffold-free assembly, and its design was optimized through algorithmic search and iteration.

<div class="row img-pair">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/design1.png" caption="Roof plan" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/design_modularized.png" caption="Roof modularization" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/design2.png" caption="Elevation" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Crowns

The crown links the printed column to the space-frame canopy. Candidate `Var_3`, built from standardized space-frame modules ($40$ joints, $88$ pipes), was fabricated.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/protoplasto/crown_design.png" caption="Design and sample" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Columns

HC3DP prints large non-load-bearing elements much faster than conventional 3D printing: a 2 m column takes about 8 hours. Each column was fixed to a
concrete base for stability and load-tested at ETH Hönggerberg.

{% comment %} pdf p.35 {% endcomment %}

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" rewind="true">
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/column_design1.png" caption="Design" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/column_candidates.jpg" caption="Candidate search" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/printing_setup.png" caption="Printing setup" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/load_testing.png" caption="Load test" class="img-fluid rounded z-depth-1" %}</swiper-slide>
</swiper-container>

<div class="row img-tall">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/column_printed.jpg" caption="Printed column sample" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/protoplasto/crown_connection.jpg" caption="Crown-column connection sample" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/protoplasto/carrying.jpg" caption="Light enough to carry by hand" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Assembly

The canopy and crowns are made of robot-cut fiberglass pipes and jet-fusion printed joints. The pipes were assembled by hand into pre-designed sub-modules,
which interlock when mounted.

{% comment %} pdf p.34 {% endcomment %}

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" rewind="true">
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/assembling2.jpg" caption="Pre-assembling sub-modules in the lab" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/assembling3.jpg" caption="Joining the sub-modules into a canopy" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/assembly_top.png" caption="Modules ready" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/demo4.png" caption="Assembled structure with AR overlay" class="img-fluid rounded z-depth-1" %}</swiper-slide>
</swiper-container>

<div class="row">
    <div class="col-sm-7 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/demo3.jpg" caption="The first completed demonstrator" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/demo2.jpg" caption="Looking up into the canopy" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### On-site demonstrators

{% comment %} pdf p.36 + p.37 {% endcomment %}

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/assembling.jpg" caption="On-site assembly" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/on_site.png" caption="Finishing the structure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/cover.jpg" caption="Completed structure" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Press

Prōtóplasto was exhibited as a media installation at the Futurama Innovation Hub in Aargau, Switzerland, and featured by NCCR Digital Fabrication and in
the 3D printing press.

- [Prōtóplasto: Ultra-Lightweight Plastic](https://dfab.ch/news/protoplasto-ultra-lightweight-plastic) · _NCCR Digital Fabrication_, Nov 2024
- [Prōtóplasto zeigt neue Perspektiven für den Einsatz von Kunststoffen in der Architektur auf](https://www.3dnatives.com/de/protoplasto-zeigt-neue-perspektiven-fuer-kunststoffen-in-architektur-auf-04122024/)
  · _3Dnatives_ (in German), Dec 2024

### References

1. M. Leschok, L. Reiter, B. Dillenburger. Large-scale hollow-core 3D printing (HC3DP): A polymer 3D printing technology for large-scale ultralightweight
   components. _Additive Manufacturing_ 78, 103874 (2023). [doi:10.1016/j.addma.2023.103874](https://doi.org/10.1016/j.addma.2023.103874)
2. M. Leschok, M. Kladeftira, Y.-F. Chan, B. Dillenburger. Large-Scale Hollow-Core 3D Printing: Variable Cross-Section and Printing Features for
   Lightweight Plastic Elements. _3D Printing and Additive Manufacturing_ 11(3), 907–918 (2024).
   [doi:10.1089/3dp.2023.0287](https://doi.org/10.1089/3dp.2023.0287)
3. M. Leschok, M. Kladeftira, N. Eftekhar, B. Dillenburger. Prōtóplasto: A Discrete Roof-Column System with Hollow-Core 3D Printing and Bespoke Space
   Frames. In _Fabricate 2024_, UCL Press, 122–129. [doi:10.2307/jj.11374766.19](https://doi.org/10.2307/jj.11374766.19)

Project page: [Digital Building Technologies – Prōtóplasto](https://dbt.arch.ethz.ch/project/protoplasto/)
