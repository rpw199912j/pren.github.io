---
layout: distill
title: Convex Hull Construction of Phase Diagrams
description: A visual introduction
date: 2023-03-17
tags: thermodynamics

authors:
  - name: Peiwen Ren
    affiliations:
      name: Stanford University

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Common Tangent Construction
  - name: Convex Hull Construction
  - name: Isothermal Ternary Phase Diagram
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2

# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }

---
## Common Tangent Construction
For a two-component system (component A and component B) with two phases (phase $$\alpha$$ and phase $$\beta$$), phase equilibria are established when 3 conditions are met:

1. $$ T^\alpha=T^\beta $$
2. $$ P^\alpha=P^\beta $$
3. $$ \mu^\alpha_A=\mu^\beta_A,\; \mu^\alpha_B=\mu^\beta_B $$

All of these conditions give rise to the common tangent construction. Namely, the thermal and mechnical equilibria make sure the common tangent construction is valid only when there is no temperature or pressure gradient across different phases. The chemical potential equilibrium enforces that the partial differentials of $$\mu$$ with respect to component A and B have to be on the same line. For a binary system, the common tangent points are found by solving a system of two equations:

1. $$ \frac{\partial\mu^\alpha}{\partial X_B}\bigg|_{X_B^\alpha} = \frac{\partial\mu^\beta}{\partial X_B}\bigg|_{X_B^\beta} $$
2. $$ \frac{\mu^\beta(X_B^\beta)-\mu^\alpha(X_B^\alpha)}{X_B^\beta-X_B^\alpha}=\frac{\partial\mu^\alpha}{\partial X_B}\bigg|_{X_B^\alpha} \text{ or } = \frac{\partial\mu^\beta}{\partial X_B}\bigg|_{X_B^\beta}$$

The first equation means that the tangent lines of the $$ \alpha $$ and $$ \beta $$ evaluated at $$ X_B^\alpha $$ and  $$ X_B^\beta $$ respectively are parallel. The second equation then ensures the two tangent lines coincide, satisfying the chemical potential equilibrium. Graphically, solving these two equations can be represented with the following animation.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820758208?h=4730b42075&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CommonTangent_p1"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p>&nbsp;</p>

It is also worth pointing out that the absolute values of the reference energies $$ \mu^{oL} $$ and $$ \mu^{oS} $$ of the pure components do not matter. What matters is the **energy difference** between the phases at pure components. As long as $$ \mu^{oL}_A - \mu^{oS}_A $$ and $$ \mu^{oL}_B - \mu^{oS}_B $$ stay fixed, the compositions of the common tangent points will stay put. 

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820758195?h=2c9decd025&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CommonTangent_p2"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

## Convex Hull Construction
Alternatively, finding the common tangent points can be reformulated as a convex hull problem. The convex hull is the smallest convex shape that can bound the Gibbs free energy curves. One can imagine pulling a string from below the Gibbs free energy curves. The string is being pulled up with a very strong force, such that it comes into very close contact with the gibbs energy curves. The shape formed after such close contact is the convex hull. Whenever there is a gap between the convex hull and the Gibbs free energy curves, there is a two-phase phase equilibrium, where the gap's endpoints are equivalent to the common tangent points.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820758201?h=ce2cacb752&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CommonTangent_p3"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>
<p>&nbsp;</p>

Now that we can find common tangents at a given temperature and pressure. If we fix pressure and now allow temperature to change, we can construct the familiar temperature-composition phase diagram.

<div style="padding:100% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/820775444?h=533e43b478&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="CuAgPhaseDiagram_LightMode"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>


## Isothermal Ternary Phase Diagram
The convex hull idea can be easily extended to higher dimensions. For a ternary system, the convex hull becomes a piece of cloth being pulled up against the Gibbs energy surfaces, rather than a string in the binary case. If we choose a certain pressure and temperature, we can visulize an isothermal section of the ternary phase diagram.

<div style="padding-bottom:56.25%; position:relative; display:block; width: 100%">
  <iframe width="100%" height="100%"
    src="/assets/html/ternary_isothermal_slice_400K.html"
    frameborder="0" allowfullscreen="" style="position:absolute; top:0; left: 0">
  </iframe>
</div>
<p>&nbsp;</p>

If we lower the temperature from 400K to 280K, the isothermal section changes to
<div style="padding-bottom:56.25%; position:relative; display:block; width: 100%">
  <iframe width="100%" height="100%"
    src="/assets/html/ternary_isothermal_slice_280K.html"
    frameborder="0" allowfullscreen="" style="position:absolute; top:0; left: 0">
  </iframe>
</div>



***


