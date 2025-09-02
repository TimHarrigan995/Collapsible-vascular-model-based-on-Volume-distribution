# Collapsible-vascular-model-based-on-Volume-distribution
Python (Jupyter) files and a writeup showing a stable simulation of vascular collapse

Many vein-side blood vessels are collapsed at any specific time, because unlike the arterial side of the circulation the pressure in the vessels is typically low and can often be less than the pressure in the tissues around them.
Modeling the flow in the veins of the body is difficult because the pressure-volume relationship for the vessel has a substantial range of vessel volume where the transmural pressure changes very little, if at all.  This makes any model of the veinous side of the circulation very difficult if pressure is used to characterize the state of the vessel.  The typical "capacitor" model for a tube or an artery becomes numerically difficult to use, because the effective capacitance (volume change per pressure change) becomes very large, and because a nonlinear model of the vessel is very difficult to use if a very small pressure increment causes a large volume increment.
This program triees out using volume as the state variable that is time -stepped in the simuulation.  Instead of time-stepping the momentum equation, as in most hydraulic models, I am time stepping the conservation of mass equation.  This wrks because, for the models I am using, the volume of fluid in all the defined vessels and system capacitances can define the pressure distribution, which determines flow, which goes into the conservarition of mass equaiton.

The resistances of the vessels are also complex functions of teh cross-sectional area, and in this model I simplify the relationship by taking the 1/r^4 relationship for a tube with a round cross section, and replacing it with a 1/A^2 relationship (Ais cross sectional area).

There is a write-up ans several jupyter notebooks in this repository in case you would like to check out the code.
