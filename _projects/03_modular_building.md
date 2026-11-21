---
layout: page
title: Reconfigurable Modules
description: Graph-search reconfiguration of a modular building · individual project · UCLA, 2022
img: assets/img/projects/modular_building/cover.jpg
importance: 3
category: digital
related_publications: false
---

Individual academic project @ UCLA · Spring 2022<br>


Developed in discussion with [Arrival](https://en.wikipedia.org/wiki/Arrival_%28company%29), a UK maker of electric vans built from modular, recyclable
parts, this project carries the same idea from vehicles to buildings. A building becomes a modular structure with a _metabolism_: as demand changes, for
example after a short peak of events such as the LA 2028 Olympics, its modules are disassembled, refitted in a micro-factory, and shipped back to be
reassembled into a new form.

{% comment %} Arrival images not the best yet {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/modular_building/cover.jpg" caption="Arrival's modular approach to vehicle production. Image: Arrival" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/modular_building/microfactory.jpg" caption="Arrival's micro-factory. Image: The New York Times" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Algorithm

The modules sit on a voxel grid, and the space around the grid is treated as a graph.  Given an initial and a target form with the same number of modules, every module is assigned a target cell position by computation. It then travels there along a contructed path.

{% comment %} TODO: replace with your pseudo code {% endcomment %}

```text
Input:  initial configuration S, target configuration T   (|S| = |T|)
Output: a sequence of module moves that turns S into T

...
```

### Demo

The program, written in C# and run in Unity as an agent-based simulation, transforms one arbitrary pixelized form into another by computing a path for
each module and routing the modules one by one. In this demo, 1,500+ modules reassemble into a target form of the same size.

<div class="row">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="https://player.vimeo.com/video/677168413" class="img-fluid rounded z-depth-1" width="100%" height="400" %}
    </div>
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include video.liquid path="https://player.vimeo.com/video/896784882?h=845636b9ed" class="img-fluid rounded z-depth-1" width="100%" height="400" %}
    </div>
</div>


{% include video.liquid path="https://player.vimeo.com/video/703057411?h=8b84ae630e" class="img-fluid rounded z-depth-1" width="100%" height="400" %}

