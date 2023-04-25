---
layout: page
title: Materials Science Animations
description: Educational animations for materials science
img: assets/img/manim_logo.png
importance: 1
category: fun
---

>What I cannot see, I do not understand.

This is an example gallery for my materials science animations created with [ManimCE](https://www.manim.community/).

<p>&nbsp;</p>

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

### Gibbs free energy equation

The following animation shows a step-by-step breakdown of the Gibbs free energy equation in a binary system, 
as well as how each variable affects the final shape of the Gibbs curve.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/739055634?h=f3169f450c&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="BinarySolution"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>


<p>&nbsp;</p>

### Cu-Ag Phase diagram construction from common tangents
This shows the construction of a real Cu-Ag binary phase diagram from the common tangents of gibbs curves. 
The Gibbs free energy curves are extracted from [Thermo-Calc](https://thermocalc.com/).

<div style="padding:100% 0 0 0;position:relative;">
    <iframe src="https://player.vimeo.com/video/738774697?h=3fed4c0593&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen;   picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CuAgPhaseDiagram">
    </iframe></div>
<script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

### Legendre Transformations
Legendre transformation allows one to swap the independently controlled variables while retaining all the information in the original thermodynamic potential. The following animation shows the transformation between $$ U(S,V) $$ and $$ F(T,V) $$, where $$ F $$ is the tangent line intercept with the $$ U $$ axis. 

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/815746822?h=5adc2842d3&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Legendre2D"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

One can clearly see the change in concavity when we go from an extensive variable $$ S $$ to an intensive variable $$ T $$. We can also go one step further, showing the Legendre transformation from $$ U(S,V) $$ to $$ G(T,P) $$, where $$ G $$ is the tangent plane intercept with the $$ U $$ axis.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/804055211?h=125fe612d8&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="Legendre3D"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

## **Kinetics**
### Diffusion with Cahn-Hilliard Equation
The Cahn-Hilliard equation is often used to model phase separation as a result of spinodal decomposition. The following animations are created with a hand-written finite-difference partial differential equation solver in Numpy. The numerical calculations are optimized with the [Numba](https://numba.pydata.org/) package. Here, we explore the effect of the average starting composition and noise distribution on the final microstructure.

With the average start composition as 0.5, and random noises $$ \pm 0.05 $$:
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820788402?h=6fa7c37ac5&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CahnHilliard2D-Random-Noise-0.5+-0.05"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p>&nbsp;</p>

With the average start composition as 0.3, and random noises $$ \pm 0.05 $$:
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820788389?h=9e491f1dc9&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CahnHilliard2D-Random-Noise-0.3+-0.05.mp4"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p>&nbsp;</p>

With the average start composition as 0.5, and square noises $$ \pm 0.1 $$:
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820788413?h=d4e825a4e7&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CahnHilliard2D-Square-Noise-0.5+-0.1"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p>&nbsp;</p>

With the average start composition as 0.5, and wave noises $$ \pm 0.1 $$:
<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820788436?h=6986fc1340&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CahnHilliard2D-Wave-Noise-0.5+-0.1"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p>&nbsp;</p>


### TTT Diagram
To model phase transformation kinetics, we can write the phase fraction by volume that has been transformed ( $$f_\mathrm{transformed}$$ )
as a function of the steady-state nucleation rate ( $$J$$ ), the growth rate ( $$\dot{R}$$ ), and time ( $$t$$ ):

$$f_\mathrm{transformed}=1-\exp\left(-\frac{\pi}{3}J{\dot{R}}^3t^4\right)$$

When the temperature ( $$T$$ ) is below the phase transformation point, the nucleation rate should decrease with increasing temperature (i.e., decreasing undercooling), 
and the growth rate should increase with increasing temperature. As the temperature increases, we can trace the time durations it takes to reach 10%, 50%, and 99% transformed to obtain a Time-Temperature-Transformation (TTT) diagram.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/738863364?h=17e100eb2b&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="PhaseFractionToTTT"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

### Voronoi crystall growth
When the crystal growth is isometric, and all nuclei have the same growth rate, the final cell boundary is equivalent to a [Voronoi diagram](https://en.wikipedia.org/wiki/Voronoi_diagram).

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/738878038?h=676bd5917d&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="VoronoiCrystalGrowth"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

### Fourier series as solutions to partial differential equation
When students are first taught the solution to Fick's Second Law of diffusion, they are often presented with the following formula:

$$c(x,t)=\frac{4c_0}{\pi}\sum_{j=0}^\infty\left(\frac{1}{2j+1}\right)\sin\left[\frac{\left(2j+1\right)\pi x}{L}\right]\exp\left[-\left(\frac{\left(2j+1\right)\pi}{L}\right)^2Dt\right]$$

where $$c(x,t)$$ is the concentration profile as a function of position ($$x$$) and time ($$t$$); $$L$$ is the diffusion length; $$c_0$$ is the initial impurity concentration; $$D$$ is the diffusion coefficient. If the students have no prior exposure to Fourier series, they may be puzzled by this formula and wonder why we are summing over sine functions. To reduce confusion, we can visualize the summation of an infinite sine series giving rise to a square wave, which satisfies the initial boundary conditions:

$$c(x,t=0)=\frac{4c_0}{\pi}\sum_{j=0}^\infty\left(\frac{1}{2j+1}\right)\sin\left[\frac{\left(2j+1\right)\pi x}{L}\right]$$

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/739070037?h=2fd31994f0&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="FourierSeries.mp4"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

## **Crystallography**
### Cubic 3-fold rotational symmetry
The 3-fold rotational symmetry for a cube.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/739072172?h=a0fd666dcc&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CubicSymmetry"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

<p>&nbsp;</p>

## **First-Principle Calculations**
### Convex hull phase diagram
The following animation visualizes the 3D convex hull phase diagram. The geometric intuition for the convex hull is that 
one can imagine there is a piece of cloth being pulled upward from the bottom, and when that cloth comes into contact with all the phase points in
3D, the shape that the cloth makes when being pulled very tightly is the convex hull. Near the end, the animation also shows a re-constructed convex hull
and its 2D phase diagram projection when one phase's energy is lowered.

The data is queried from the [OQMD](https://oqmd.org/) database, and the convex hull phase diagram is constructed with the 
[Pymatgen](https://pymatgen.org/) package.

<div style="padding:60% 0 0 0;position:relative;">
    <iframe src="https://player.vimeo.com/video/738852675?h=f09494478b&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen;   picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="ConvexHullPhaseDiagram.mp4">
    </iframe>
</div><script src="https://player.vimeo.com/api/player.js"></script>
