---
title: "Fast particle-mesh code for Milgromian dynamics"
collection: publications
category: manuscripts
permalink: /publication/2024-02-17-paper-title-number-4
date: 2024-01-22
venue: 'Astronomy & Astrophysics'
paperurl: 'https://doi.org/10.1051/0004-6361/202347830'
---



***Abstract***: 
*Context*. Modified Newtonian dynamics (MOND) is a promising alternative to dark matter. To further test the theory, there is a need for fluid- and particle-dynamics simulations. The force in MOND is not a direct particle-particle interaction, but derives from a potential for which a nonlinear partial differential equation (PDE) needs to be solved. Normally, this makes the problem of simulating dynamical evolution computationally expensive.  
*Aims*. We intend to develop a fast particle-mesh (PM) code for MOND (the AQUAL formalism).  
*Methods*. We transformed the nonlinear equation for MOND into a system of linear PDEs plus one algebraic equation. An iterative scheme with the fast Fourier transform (FFT) produces successively better numerical approximations.  
*Results*. The algorithm was tested for dynamical systems in MOND where analytical solutions are known: the two-body problem, a body with a circular ring, and a spherical distribution of particles in thermal equilibrium in the self-consistent potential.  
*Conclusions*. The PM code can accurately calculate the forces at subpixel scale and reproduces the analytical solutions. Four iterations are required for the potential, but when the spatial steps are small compared to the kernel width, one iteration is suffices. The use of a smoothing kernel for the accelerations is inevitable in order to eliminate the self-gravity of the point particles. Our PDE solver is 15 to 42 times as slow as a standard Poisson solver. However, the smoothing and particle propagation takes up most of the time above one particle per 103 pixels. The FFTs, the smoothing, and the propagation part in the code can all be parallelized.
