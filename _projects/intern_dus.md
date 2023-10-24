---
layout: page
title: Intern
description: at Demcon Unmanned Systems
img: assets/img/intern/cover.jpg
importance: 1
category: intern
---

### Mission
Demcon Unmanned Systems manufactures and supplies unmanned vessels with autonomous capabilities. This internship project is about designing `an efficient real-time sampling based path planning algorithm` for the `path tracking` of unmanned vessels, which fulfills following requiremets:
* to follow the predefined path as close as possible and reach the destination;
* to avoid the obstacles when they get in the way of the predefined path;
* to perform in real-time;
* to generate the path within certain angle constraints.

### Method

<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-1.png" title="example image" class="img-fluid rounded z-depth-1" caption="Determine initial point"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-2.png" title="example image" class="img-fluid rounded z-depth-1" caption="Generate edges"%}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-3.png" title="example image" class="img-fluid rounded z-depth-1" caption="Connect to the predefined path"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-4.png" title="example image" class="img-fluid rounded z-depth-1" caption="Select the optimal path"%}
    </div>
</div>

<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-5.png" title="example image" class="img-fluid rounded z-depth-1" caption="Determine initial point"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-6.png" title="example image" class="img-fluid rounded z-depth-1" caption="Generate edges"%}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-7.png" title="example image" class="img-fluid rounded z-depth-1" caption="Connect to the predefined path"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-8.png" title="example image" class="img-fluid rounded z-depth-1" caption="Select the optimal path"%}
    </div>
</div>


### Results

<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/single_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Circumvent a single obstacle"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/wide_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Circumvent a wide obstacle"%}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/long_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Circumvent a wide obstacle"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/multiple_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Circumvent multiple obstacles"%}
    </div>
</div>