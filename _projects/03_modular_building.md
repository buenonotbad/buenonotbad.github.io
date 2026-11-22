---
layout: page
title: Reconfigurable Modules
description: Graph-search reconfiguration of a modular building · individual project · UCLA, 2022
img: assets/img/projects/modular_building/cover.jpg
importance: 3
category: digital
related_publications: false
pseudocode: true
---

Individual academic project @ UCLA · Spring 2022<br>

Developed in discussion with [Arrival](https://en.wikipedia.org/wiki/Arrival_%28company%29), a UK maker of electric vans built from modular, recyclable
parts, this project carries the same idea from vehicles to buildings. A building becomes a modular structure with a _metabolism_: as demand changes, for
example after a short peak of events such as the LA 2028 Olympics, its modules are disassembled, refitted in a micro-factory, and shipped back to be
reassembled into a new form.

{% comment %} Arrival images not the best yet {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/modular_building/1.jpg" caption="Arrival's modular approach to vehicle production. Image: Arrival" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="https://www.youtube.com/embed/DXZEHJeoqSo" class="img-fluid rounded z-depth-1" width="100%" height="400" %}
    </div>
</div>

### Algorithm

{% comment %} TODO: yet to complete pseudo code here {% endcomment %}

```pseudocode
\begin{algorithm}
\caption{Reconfiguration}
\begin{algorithmic}
\INPUT initial and target configurations $S = \{p_1, \ldots, p_n\}$, $T = \{p'_1, \ldots, p'_n\}$, with cell positions $p_i, p'_i \in \mathbb{R}^3$
\OUTPUT a sequence of module paths $\mathcal{P}$ that turns $S$ into $T$

\STATE \COMMENT{build the graph of passable space}
\STATE $G = (V, E) \gets$ grid adjacency of the passable space around $S$ and $T$

\STATE \COMMENT{map each module to its free neighboring nodes}
\FORALL{$m \in S$}
    \STATE $H[m] \gets \{\, v \in V : v \text{ adjacent to } m \,\}$
\ENDFOR

\STATE \COMMENT{route the modules one by one}
\STATE $\mathcal{P} \gets$ empty sequence
\FORALL{$m \in S$}
    \STATE assign $m$ a target $t(m) \in T$
    \STATE $P \gets$ \CALL{AStar}{$G, H[m], t(m)$}
    \STATE move $m$ along $P$ and update $G$
    \STATE append $P$ to $\mathcal{P}$
\ENDFOR
\RETURN $\mathcal{P}$
\end{algorithmic}
\end{algorithm}
```

<!-- pseudocode.js adds its math after MathJax has run, so MathJax never adds the CSS for those glyphs and they show up blank; re-run MathJax once -->
<script>
  window.addEventListener("load", function refreshMath() {
    if (!window.MathJax || !MathJax.startup || !MathJax.startup.promise) return setTimeout(refreshMath, 200);
    MathJax.startup.promise.then(() => {
      MathJax.startup.document.clear();
      MathJax.startup.document.updateDocument();
    });
  });
</script>

### Demo

The program, written in C# and run in Unity as an agent-based simulation, transforms one arbitrary pixelized form into another by computing a path for
each module and routing the modules one by one. In this demo, 1,500+ modules reassemble into a target form of the same size.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="https://player.vimeo.com/video/677168413" class="img-fluid rounded z-depth-1" caption = "Demo: reassemble" width="100%" height="400" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="https://player.vimeo.com/video/896784882?h=845636b9ed" class="img-fluid rounded z-depth-1" caption = "Demo: in-situ transform" width="100%" height="400" %}
    </div>
</div>

{% include video.liquid path="https://player.vimeo.com/video/703057411?h=8b84ae630e" class="img-fluid rounded z-depth-1" width="100%" caption = "Demo: Conceptual modular recycling for LA Olympic 2028" height="400" %}
