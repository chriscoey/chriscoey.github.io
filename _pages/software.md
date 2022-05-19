---
layout: page
permalink: /software/
title: software
description: 
nav: true
nav_order: 3
---

I contribute to [JuMP](https://jump.dev/) and [MathOptInterface](https://github.com/jump-dev/MathOptInterface.jl).
I am a primary developer of the following optimization packages (ordered chronologically) in [Julia](https://julialang.org/).


### Pajarito solver

[Pajarito.jl](https://github.com/JuliaOpt/Pajarito.jl) is an outer approximation solver for mixed integer conic optimization problems over standard second-order, positive semidefinite, and exponential cones.
Pajarito has several cutting plane algorithms that combine the power of external MILP solvers and continuous conic solvers.
We discuss the theory and implementation in Chapter 4 of [my thesis](/assets/pdf/phd_thesis.pdf), which is an updated and shortened version of the paper [outer approximation with conic certificates for mixed-integer convex problems](https://arxiv.org/abs/1808.05290) (with Miles Lubin and Juan Pablo Vielma).
Based on the now-defunct MathProgBase, Pajarito is succeeded by MOIPajarito, which is based on MathOptInterface.


### Pavito solver

[Pavito.jl](https://github.com/jump-dev/Pavito.jl) implements outer approximation algorithms for smooth mixed integer nonlinear programming (MINLP) problems, using gradient cuts. 
Pavito uses external MILP and NLP solvers.


### Hypatia solver

[Hypatia.jl](https://github.com/chriscoey/Hypatia.jl) is a primal-dual conic interior point algorithm for continuous conic problems over generic proper cones.
We discuss Hypatia in Chapter 1 of [my thesis](/assets/pdf/phd_thesis.pdf), which is based on the paper [performance enhancements for a generic conic interior point algorithm](https://arxiv.org/abs/2107.04262) (with Lea Kapelevich and Juan Pablo Vielma).
We model three dozen applied [examples](https://github.com/chriscoey/Hypatia.jl/tree/master/examples); some appear in Chapters 2 and 3 of [my thesis](/assets/pdf/phd_thesis.pdf), which are based on our papers [solving natural conic formulations with Hypatia.jl](https://arxiv.org/abs/2005.01136) and [conic optimization with spectral functions on Euclidean Jordan algebras](https://arxiv.org/abs/2103.04104) (with Lea Kapelevich and Juan Pablo Vielma).


### MOIPajarito solver

[MOIPajarito.jl](https://github.com/chriscoey/MOIPajarito.jl) replaces Pajarito and is soon to be formally released.
MOIPajarito implements Pajarito's outer approximation algorithms but has a completely redesigned architecture, including a generic cone interface that allows adding support for new convex cones.
We discuss MOIPajarito in Chapter 5 of [my thesis](/assets/pdf/phd_thesis.pdf).


### PajaritoExtras.jl

[PajaritoExtras.jl](https://github.com/chriscoey/PajaritoExtras.jl) extends MOIPajarito by adding support for a dozen cones that are already supported by Hypatia.
The examples folder contains applied mixed integer conic examples over these cones, formulated with JuMP and solved using MOIPajarito.
These cones, examples, and benchmark results are discussed in Chapter 5 of [my thesis](/assets/pdf/phd_thesis.pdf).
