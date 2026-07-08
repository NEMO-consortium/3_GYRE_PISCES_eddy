# Mesoscale eddy parameterisations in NEMO5

This article provides an overview of mesoscale eddy parameterisations available in NEMO version 5.0.2. This tutorial is designed for beginners who want to be introduced to eddy parameterisations and learn how to set up NEMO experiments in order to compare available parameterisations. 

* __Prerequisites__: Install NEMO v5.0.2 following the [NEMO Basics](https://github.com/NEMO-consortium/0_NEMO_basics) tutorial. 
* __Objectives__: To introduce mesoscale eddy parameterisations in NEMO, and allow users to test them in a simple test case.
* __Configuration__: GYRE_PISCES

## Overview

In this tutorial, you will :
* set-up and run an idealised gyre configuration (GYRE_PISCES).
* use basic XIOS file manipulation to add extra variables in output files.
* restart different experiments from an initial state, that can be used as a benchmark for eddy parameterisations. 
* modify the configuration namelist in order to set-up mesoscale eddy parameterisations. 
* compare your simulation outputs in order to assess the impact of eddy parameterisation choices on the ocean state.

## Mesoscale parameterisations within the GYRE_PISCES configuration

The GYRE configuration has been built to simulate the seasonal cycle of a double-gyre box model (see Figure below). The configuration is meant to represent an idealized North Atlantic or North Pacific basin.
It consists in an idealized rectangular domain, rotated by 45°, over which an analytical seasonal forcing is applied.
The circulation is forced by analytical profiles of wind and buoyancy fluxes. The applied forcings vary seasonally in a sinusoidal manner between winter and summer extrema.

Even though this is a very simple example, it allows one to investigate the parameterised transports of mesoscale eddies on tracers and their contribution to the large scale circulation.
In this tutorial, we will use a 1° horizontal resolution test case, which is cheap enough to be run on a personal computer and can be used as a demonstrator for comparing mesoscale parameterisations.

Now that you know a bit more about the configuration you're going to use, it's time to start [tutorial 1](docs/tutorial-1.md).

&nbsp;

![alt text](docs/imgs/Levy-OM-2010-Fig1.png)
__Figure:__ Left panel: the analytical wind forcings which vary between winter (solid line) and summer (dashed line) in a sinusoidal manner. Right panel: the rotated domain and the mean barotropic stream function as shown in [Lévy et al. (2010)](http://dx.doi.org/10.1016/j.ocemod.2010.04.001)
