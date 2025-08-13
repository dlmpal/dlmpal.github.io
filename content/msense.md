---
title: 'msense'
date: 2024-05-19
type: landing

design:
  # Section spacing
  spacing: '5rem'

# Page sections
sections:
  - block: markdown
    id: msense-intro
    content:
      title: mSense
      text: |
        [mSense](https://github.com/dlmpal/mSense) is a Python package developed for Multidisciplinary Analysis and Optimization (MDAO). It allows the user to quickly setup and solve MDAO problems, and makes it easy to switch between various
        Multidisciplinary Analysis (MDA) methods and Multidisciplinary Optimization (MDO) architectures. MSense is written with an object-oriented approach and can be used through its Python Application Programming Interface (API). A basic user guide can be found [here](http://velos0.ltt.mech.ntua.gr/kgianna/diplomat/fp/pallas.pdf#page=108)

        ### Supported MDO architectures
        Currently, the following MDO architectures are implemented in mSense:
        1. Multidisciplinary Feasible (MDF)
        2. Individual Discipline Feasible (IDF)
        3. Collaborative Optimization (CO)

        A comparison of the mSense implementation of the above architectures was performed [in my diploma thesis](http://velos0.ltt.mech.ntua.gr/kgianna/diplomat/fp/pallas.pdf#page=39), based on Sellar's problem. 
        <img src="/msense/sellar_prob_err_hist.png" width="500" height="250">
        <figcaption> Sellar problem: Comparison of the MDF, IDF and CO architectures</figcaption> 
        
        ### Aerostructural wing optimization example
        The simultaneous aerodynamic and structural optimization of aircraft wings is a classic MDO problem. 
        [In my diploma thesis](http://velos0.ltt.mech.ntua.gr/kgianna/diplomat/fp/pallas.pdf#page=81), I used mSense to optimize the shape of the ONERA M6 wing (parameterized with volumetric NURBS), along with its structure, which was described using a simple beam finite-element model. The optimization objective was to increase the wing's lift-to-drag ratio, while respecting a stress constraint, resulting from the structural model. The problem was setup and solved in mSense, using the MDF architecture.

        <table>
        <tr>
        <td>
        <figure>
        <img src="/msense/wing_xdsm.png" width="500" height="250">
        <figcaption> Aerostructural wing optimization: Extended Design Structure Matrix (XDSM) </figcaption>
        </figure>
        </td>
        </tr>
        
        <tr>
        <td>
        <figure>
        <img src="/msense/lift_drag_weight.png" width="500" height="250">
        <figcaption> Aerostructural wing optimization: Evolution of the wing's drag, lift, weight and CL/CD values during optimization</figcaption>
        </figure>
        </td>
        </tr>
        
        <tr>
        <td>
        <figure>
        <img src="/msense/deformed_vs_undeformed.png" width="800" height="400">
        <figcaption> Aerostructural wing optimization: Comparison of the baseline (left) and optimized (right) wings</figcaption> 
        </figure>
        </td>
        </tr>
        </table>
---

<!-- ### Airfoil shape optimization        
A NACA-0012 airfoil is placed inside a two-dimensional inviscid flow field. 
The airfoil is able to rotate about an axis normal to the flow plane, 
and a torsional spring is attached at its quarter chord. The shape of the airfoil (parameterized
with volumetric NURBS) is optimized in order to achieve a desired lift value.  -->
