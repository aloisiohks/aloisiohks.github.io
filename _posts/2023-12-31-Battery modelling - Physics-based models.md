---
layout: post
title: Battery modelling - Physics-based models
---

{{ page.title }}
================

<p class="meta">31 Dec 2023 - Boston</p>


In an ideal BMS, one would ideally like to have sensors embedded within the the battery cells to measure individual internal electrochemical variables and temperature. If that would be possible, one would be able to devise battery algorithms to counteract against possible safety hazards ahead of time and predicting the true actual battery internal state, which has the potential to maximize battery performance, ensure safety and extend battery life. However, achieving that ideal would significantly increase the battery manufacturing costs. Instead, we choose to mimic this ideal BMS, by relying on physics-based models that are capable of describing transport phenomena in solid and electrolyte, electrochemical kinetics and thermodynamics within lithium-ion batteries. A model that fits these requirements is the well known pseudo-two-dimensional (P2D) model, which is based on a set of nonlinear partial differential equations and one algebraic equation that describe the mass conservation, charge conservation and kinetics within the porous electrode structure of LIBs. The P2D model was originally developed by Doyle et al. in [doyle1993] and is derived from the porous electrode and concentration solution theories. However, one of the drawbacks of the P2D model is its large number of parameters to be estimated, which makes difficult the model parameterization using only non-destructive methods

$$
0\leq x\leq L^{\mathrm{n}}		\text{negative\;electrode}
L^{\mathrm{n}}\leq x\leq L^{\mathrm{n}}+L^{\mathrm{s}}		\text{separator}
L^{\mathrm{n}}+L^{\mathrm{s}}\leq x\leq L^{\mathrm{n}}+L^{\mathrm{s}}+L^{\mathrm{p}}		\text{positive\;electrode}
$$
