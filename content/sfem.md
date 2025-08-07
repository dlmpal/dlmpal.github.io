---
title: 'sfem'
date: 2024-05-19
type: landing

design:
  # Section spacing
  spacing: '5rem'

# Page sections
sections:
  - block: markdown
    id: sfem-intro
    content:
      title: SFEM
      text: |
        [SFEM](https://github.com/dlmpal/sfem) is a C++ framework for the solution of Partial Differential Equations on unstructured meshes, using the Finite Elemenet and Finite Volume methods. It supports distributed memory parallelism via the MPI protocol. SFEM utilizes PETSc for sparse linear algebra computations, and METIS for mesh partitioning. SLEPc is an optional dependency, which enables the computation of eigenvalues of discretized operators.

        Below are a few examples detailing the current capabilities of SFEM. The code for these examples will be added soon.

  - block: markdown
    id: sfem-example-1
    content:
      title: Spherical Shell under Internal Pressure
      text: |
        This example highlights SFEM's ability to handle larger meshes. 
        A spherical shell octant is meshed with ~770,000 second order 
        tetrahedral elements, corresponding to approximately 1.5 million degrees of 
        freedom. The shell is considered linear elastic and is subject to a 
        costant pressure value acting on its inner wall.The mesh is partitioned 
        among 8 processes using METIS and the resulting linear system is solved 
        using PETSc's Conjugate Gradient solver.
        
        <figure>
        <img src="/sfem/partition_plot.png" width="800" height="400">
        <figcaption>Spherical shell problem: Element partition plot</figcaption>
        </figure>
        
        <figure>
        <img src="/sfem/disp_mag_plot.png" width="800" height="400">
        <figcaption>Spherical shell problem: Displacement magnitude plot</figcaption>
        </figure>

  - block: markdown
    id: sfem-example-2
    content:
      title: Linear Accoustics
      text: |
        This example is used to showcase SFEM's ability to handle hyperbolic problems. 
        The two-dimensional linearized Euler equations are discretized in space using the finite-volume method
        and integrated in time with a fourth-order Runge-Kutta integrator. The interface fluxes are reconstructed
        using Rusanov's scheme. A monopole source is located at the center of the rectangular domain.
        <figure>
        <img src="/sfem/euler_vel_x.gif" width="800" height="400">
        <figcaption> Linear accoustics problem: Contours of the x-velocity component</figcaption> 
        </figure>

  - block: markdown
    id: sfem-example-3
    content:
      title: Potential Flow
      text: |
        In this example SFEM is used to solve a potential flow problem around a quarter
        circle. The problem is discretized using third-order quadrilateral elements, and
        a Laplace equation is solved for the velocity potential. The velocity field, 
        defined as the gradient of the potential, is then projected onto the same Continuous Galerkin
        space using a L2 projection.
        
        <figure>
        <img src="/sfem/solution_gradient.png" width="800" height="400">
        <figcaption>Potential flow problem: Velocity field magnitude and direction plot</figcaption>
        </figure>

  - block: markdown
    id: sfem-example-4
    content:
      title: Beam Modal Analysis
      text: |
        In this example SFEM is used to compute the first six eigenmodes of an elastic beam, 
        which is fully fixed on one end. The beam is discretized using second-order tetrahedral elements and 
        the resulting eigenproblem is solved using SLEPc. For validation, the resulting frequencies are compared 
        with those provided by beam theory. 

        <figure>
        <img src="/sfem/modes_plot.png" width="800" height="400">
        <figcaption> Beam Modal Analysis: Plots of the first four eigenmodes of the beam</figcaption> 
        </figure>
---
