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

A new sampling-based tree generating algorithm is proposed to address the issues of brute force branching tree and RRT. It is called `Torch`, because the generated tree look similar to the torch that burns fire on top.

The tree will be generated when there is an obstacle in the way. It is initialized with certain angle $$\alpha$$, field of view, and number of layeers. Compared with brute force branching, the number of samples required by `Torch` grows polynomially with the increase of number of layers, instead of exponentially. Compared with RRT, `Torch` is efficient in sampling in the nearby regions. 

At the first timestep, the algorithm involves determining the initial point, generating edges, connecting to the referenced path and selecting the optimal path.

<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-1.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 1. Determine initial point"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-2.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 2. Generate edges"%}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-3.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 3. Connect to the referenced path"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-4.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 4. Select the optimal path"%}
    </div>
</div>

At the next timestep, when the vessel travels on one of the edges and deviates from the referenced path, the initial point will be updated, and the tree will be generated at a different direction. The following steps of connecting to the original path and selecting the optimal path remains the same.
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-5.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 5. Determine initial point"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-6.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 6. Generate edges"%}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-7.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 7. Connect to the predefined path"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/chap2-torch-8.png" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 8. Select the optimal path"%}
    </div>
</div>

The algorithm `Torch` can also be combined with RRT in order to cover a larger sampling region. In this way, `Torch` provides a warmstart for the RRT, and RRT is generated starting from the distal layer of `Torch`. `Torch-RRT` is demonstrated in `Fig. 9` and `Fig. 10`. 
### Results

The performance of `Torch` and `Torch-RRT` is demonstrated in scenarios containing a single obstacle, a wide obstacle, a long obstacle and multiple obstacles. Tests have shown that the computational efficiency and CPU consumption of `Torch` and `Torch-RRT` outperform brute force branching and RRT.

<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/single_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 9. Circumvent a single obstacle"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/wide_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 10. Circumvent a wide obstacle"%}
    </div>
</div>
<div class="row">
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/long_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 11. Circumvent a wide obstacle"%}
    </div>
    <div class="col-sm mt-1 mt-md-0">
        {% include figure.html path="assets/img/intern/multiple_obs.gif" title="example image" class="img-fluid rounded z-depth-1" caption="Fig. 12. Circumvent multiple obstacles"%}
    </div>
</div>