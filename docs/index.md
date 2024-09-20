---
layout: page
title: Urban LES intercomparison
tagline: 
description: Urban LES Comparison project
---
## Overview
Motivation for this project can be summed up in few key points


- Bright future: microscale turbulence resolving models – essential element of urban services and planning
- Aiding urban-canopy parameterizations in meso-scale & global-scale atmospheric models
- How good is LES in reproducing urban boundary layer?
- What approaches (numerics + physics) work best?


## Participants

Currently there are 2 paticipant models: 
- LES from RCC LMSU 
> Mixed dynamic subgrid closure + nesting
> Double-moment cloud microphysics & radiation (RRTM) modules
> Land surface coupling
> Atmospheric chemistry & aerosol transport
> CPU/GPU support via C/C++/MPI/OpenMP/CUDA

- Fluidity from Institute of Atmospheric Physics CAS
> Basic Information for Fluidity:
> Numerics:
> Spatial discretisations: first-order and second-order Continuous Galerkin, Discontinuous Galerkin, Control Volume
> Temporal discretisation: first-order explicit, second-order semi-implicit and implicit
> Turbulence Package:
> Reynolds-Averaged Navier-Stokes (RANS) Modelling
> Generic length scale turbulence parameterization (based on two equations, for the transport of turbulent kinetic energy (TKE) and a generic second quantity)
> Standard k – ε Turbulence Model
> Large-Eddy Simulation (LES):
> Second-order dissipation model
> Fourth-order dissipation model
> Dynamic Smagorinsky model


 to become a participant send an email to [Andrey Debolskiy](and.debol@srcc.msu.ru) or [Evgeny Mortikov](mortikov@srcc.msu.ru)

## Stages

### Idealized urban configurations
The preliminary setup follows JAS paper [1](https://journals.ametsoc.org/view/journals/atsc/80/1/JAS-D-22-0044.1.xml)
here is a scheme for the experiments
![image](assets/images/scheme.png)

#### Stratified idealized urban cases

### Realistic urban developments

## Outputs

for output see notebooks [here](https://github.com/anddebol/ulescomp/tree/main/notebooks)


## Comparison


