---
layout: page
title: Prōtóplasto
description: Hollow-core 3D printed pavilion · team project · ETH Zürich, 2023
img: assets/img/projects/protoplasto/cover.jpg # card thumbnail, e.g. pdf p.31
importance: 1
category: robotic fabrication
related_publications: false
images:
  slider: true
---

A pavilion that tests fast robotic printing of lightweight, non-load-bearing building components with Large-Scale Hollow-Core 3D Printing (HC3DP),
together with digital assembly for quick deployment. It has three parts: HC3DP columns, crowns, and a canopy of robot-cut fibreglass pipes/trusses joined by
jet-fusion printed nodes.

{% comment %} pdf p.31 {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/protoplasto/cover.jpg" title="Prototypes display @ RFL, Gramazio Kohler, ETH Zürich" caption="Prototypes display,<br>@ RFL, Gramazio Kohler Research, ETH Zürich" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### crown

Four column-to-spaceframe connections were compared for joint count, adaptability and structural strength. Var_3 was fabricated.

{% comment %} pdf p.33: left = variants, right = Var_3 photo {% endcomment %}

<div class="row">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/crown_variants.jpg" title="crown variants" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/crown_var3.jpg" title="Var_3 fabrication" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Connection variants (left) and the fabricated Var_3 (right).
</div>

### process

<swiper-container keyboard="true" navigation="true" pagination="true" pagination-clickable="true" rewind="true">
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/design.png" caption="design iteration" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/material.jpg" caption="The earth based material is first mixed 
  with sludge, clay, water, lime and gravels." class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/mixing.jpg" caption="Taking out the sludge for mixing" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/demo_2.jpg" caption="Set up in open space" class="img-fluid rounded z-depth-1" %}</swiper-slide>
  <swiper-slide>{% include figure.liquid path="assets/img/projects/protoplasto/demo_3.jpg" caption="Photo: © Gramazio Kohler Research, ETH Zürich" class="img-fluid rounded z-depth-1" %}</swiper-slide>
</swiper-container>

### custom Printing machine

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/impact_printing/gamachine1.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/impact_printing/machine2.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/impact_printing/machine3.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Assembly

The pipes were assembled by hand in sub-modules, guided by AR programs and Grasshopper scripts.

{% comment %} pdf p.34 {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/assembly_1.jpg" title="canopy layout" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/assembly_2.jpg" title="sub-modules" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

### Column printing

HC3DP is much faster than regular 3D printing for large elements: a 2 m column prints in about 8 hours. The columns sit on concrete bases and were
load-tested at ETH Hönggerberg.

{% comment %} pdf p.35 {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/column_print.jpg" title="column printing" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/column_load_test.jpg" title="load test" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Printing a column (left) and the load test (right).
</div>

### Demonstrator

{% comment %} pdf p.36 + p.37 {% endcomment %}

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/demo_1.jpg" title="demonstrator" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/demo_2.jpg" title="demonstrator in open space" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/projects/protoplasto/demo_3.jpg" title="pavilion" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Role:programming, canopy design, robotic processing & assembly
