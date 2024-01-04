---
layout: post
title: Lithium-ion battery modelling: A control-oriented physics-based modelling approach 
---

{{ page.title }}
================

<p class="meta">31 Dec 2023 - Boston</p>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>

In electric vehicle (EV) applications, one would ideally like to have sensors embedded within the battery cells to measure individual internal electrochemical variables and temperature at the electrode level. If that would be possible, one would be able to devise battery algorithms to counteract against possible safety hazards ahead of time and predicting the true actual battery internal state, which has the potential to maximize battery performance, ensure safety and extend battery life. However, traditional battery management systems (BMS) are limited to current, voltage, and temperature measurements (battery surface) and, achieving that ideal would significantly increase the battery manufacturing costs. Alternatively, we choose to rely on physics-based models that are capable of describing transport phenomena in solid and electrolyte, electrochemical kinetics and thermodynamics within lithium-ion batteries. A model that fits these requirements is the well known pseudo-two-dimensional (P2D) model, which is based on a set of nonlinear partial differential equations and one algebraic equation that describe the mass conservation, charge conservation and kinetics within the porous electrode structure of LIBs. The P2D model was originally developed by Doyle et al. in [doyle1993] and is derived from the porous electrode and concentration solution theories. However, one of the drawbacks of the P2D model is its large number of parameters to be estimated, which makes difficult the model parameterization using only non-destructive methods because some of these parameters appear together on the model equations and then, cannot be estimated individually. In order to minimize this challenge, the lumped-parameter (LP) P2D model from [CHU2019] is adopted in this work. The LP P2D is developed based on the idea of eliminating redundant parameters and their geometric dependency using a systematic parameter-reduction method. Moreover, refinements to this LP P2D model framework have appeared in the literature, including: 1) double layer effects and constant-phase element (CPE) dynamics at the solid-electroyte interface [CHU2019]; 2) a heat generation model that couples the LPM and thermal model [kawakitaEVS2022]; and 3) a multi-species multi-reaction model that models the electrode OCP behavior as a composite of simpler OCP functions [LuDissertation2022]. 

This chapter will review the standard P2D model and the derived LP P2D model in Sections [sec:The-P2D-model] and [sec:Lumped-parameter-P2D-model], respectively. Then, Section [sec:LP-P2D-model enhancements] will then present model enhancements to the LP P2D model.


$$\begin{align*}
0\leq x\leq L^{\mathrm{n}} &  & \text{negative electrode}\\
L^{\mathrm{n}}\leq x\leq L^{\mathrm{n}}+L^{\mathrm{s}} &  & \text{separator}\\
L^{\mathrm{n}}+L^{\mathrm{s}}\leq x\leq L^{\mathrm{n}}+L^{\mathrm{s}}+L^{\mathrm{p}} &  & \text{positive electrode}
\end{align*}$$
