---
layout: page
title: Materials Science Animations
description: Educational animations for materials science
img: assets/img/12.jpg
importance: 1
category: fun
---

>What I cannot see, I do not understand.

This is an example gallery for my materials science animations created with [ManimCE](https://www.manim.community/).

## **Thermodynamics**
### Atomistic simulation of the critical radius
In the classical nucleation theory, there is a concept called the `critical radius` for nucleation. When a nucleus's radius is smaller than the critical radius, it tends to shrink; when it is larger than the critical radius, the nucleus becomes stable and will continue to grow in size. This is a result of the energy barrier created by the competition between the interfacial energy and the volumetric energy difference when a new phase nucleates. 

The question is if any nucleus with a radius smaller than the critical radius tends to shrink, how could any stable nuclei form?
The answer is that nucleation is a stochastic process where the atoms are colliding into each other with some probabilities
of impingement and detachment. It is possible that random energy fluctuations can push the nucleus radius beyond the critical radius, allowing stable nuclei to form.

This animation uses [Pymunk](http://www.pymunk.org/en/latest/) for the MD simulation and [NetworkX](https://networkx.org/) for the graph network construction. ManimCE is used to render the outputs after each time step.

<div style="padding:56.25% 0 0 0;position:relative;">
<iframe src="https://player.vimeo.com/video/738681862?h=53d7843ed9&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" 
frameborder="0" 
allow="autoplay; fullscreen; picture-in-picture" 
allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" 
title="Atomistic Simulation of the Critical Radius">
</iframe>
</div>
<script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>
### Cu-Ag Phase diagram construction from common tangents
This shows the construction of a real Cu-Ag binary phase diagram from the common tangents of gibbs curves. 
The Gibbs free energy curves are extracted from [Thermo-Calc](https://thermocalc.com/).

<div style="padding:177.78% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/738774697?h=3fed4c0593&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CuAgPhaseDiagram"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
