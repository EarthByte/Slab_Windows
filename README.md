# Slab_Windows
Workflow for Code to making reconstructions of slab geometries, and associated slab windows, using topological plate reconstructions through deep time.

The code is based on this repository: https://github.com/siwill22/pgpslabs but has been altered and extended in several ways.

The idea is principally inspired by various papers of Derek Thorkelson's and others, including a paper by McGirr et al. (2021) that included an implementation of the workflow at https://github.com/siwill22/pgpslabs, to map the extent of slab windows through geological time. The windows form where mid-ocean ridges intersect with subduction zones. This code maps points in the slabs themselves, so that slab-windows are visualised as gaps between different slab segments.

Assumptions:
•	Instead of assuming a single dip angle throughout all slabs, this workflow uses a published method to compute the paleo-slab dip based on a combination of parameters, based on a paper by Mather et al. (2023). The workflow to compute slab dip can be found here: https://github.com/brmather/Slab-Dip

•	convergence rates and ages of subducting plates are taken from a given plate reconstruction and associated paleo-age grids. Usualy, the paleo-age grids are computed using GPlately: 

https://github.com/GPlates/gplately/blob/master/Notebooks/10-SeafloorGrids.ipynb

In the current version, the slabs are represented as points along lines of equal subduction age (currently no method is implemented to turn these into a surface). The attributes at each point are the age of subuction, and  the age of the subducting seafloor.

# References
McGirr, R., Seton, M. and Williams, S., 2021. Kinematic and geodynamic evolution of the Isthmus of Panama region: Implications for Central American Seaway closure. Bulletin, 133(3-4), pp.867-884.
Mather, B.R., Müller, R.D., Alfonso, C.P., Seton, M. and Wright, N.M., 2023. Kimberlite eruptions driven by slab flux and subduction angle. Scientific Reports, 13(1), p.9216.
