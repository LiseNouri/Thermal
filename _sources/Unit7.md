# Thermal Modelling


Modelling is a mathematical representation of a physical system. In terms of space, time, and parameter discretization, the modelling approach can be continuous for simple analytical models, discretized in a spatial network of nodes and node couplings, or statistical as in the Monte Carlo ray-tracing method used to compute radiative exchanges. 

To begin the mathematical procedure, the first step is to establish the **Geometrical Mathematical Model (GMM)**. 
This model represents the system's geometry and is essential for calculating the external thermal loads on the outer surfaces and the radiation exchange between different parts of the spacecraft. 
Typically, it involves a simplified representation of geometry, excluding any details that are not relevant from a thermal perspective. 
The GMM can be estimated analytically, but {ref}`MCRT` (MCRT) is the standard industry solution.

After establishing a fundamental geometry for thermal analysis, this geometry is divided into a network of nodes. 
In order to accomplish this, the fundamental geometric shapes that comprise the geometrical mathematical model are interconnected. 
Every node represents an isothermal component that is defined by its temperature Ti and its thermal capacitance Ci. 
The numerical method used in this case is referred to as the 'lumped parameter network'. This is because the continuous parameters of the thermal system have been condensed or grouped together into a discrete set of nodes. 

The energy equation of each node (i) can be written as: 

$$
C_{i} \frac{dT_i}{dt}=Q_i+∑_{j=1}^n K_{ij}\cdot (T_j-T_i )+∑_{j=1}^n R_{ij} \cdot (T_j^4-T_i^4)
$$ (EnergyEquation)


Applying this equation to all the individual nodes of the spacecraft results in a system of ordinary differential equations. 
Solving this system allows us to determine the temperature of each specific point. 
In order to determine the temperature of the satellite, it is necessary to have both the conductive and radiative thermal couplings matrices, as well as the external loads and dissipation thermal loads vectors, as stated in the equation. 
The matrices and vectors serve as a mathematical depiction of the spacecraft's thermal model. 
This model consists of concentrated thermal capacitance nodes connected by a network of thermal conductors, primarily radiative and conductive in nature. Hence, this collection of numbers is referred to as the **Thermal Mathematical Model (TMM)**. 
Here, iterative finite difference solvers are commonly used to calculate temperatures within the spacecraft. 

```{figure} images/ThermalModelling.png
:height: 500px
:name: ThermalModelling

Thermal Design Cycle
```
Since the thermal analysis of spacecraft in orbit is a computationally expensive task, software tools now exist to automate the process and provide feedback to the engineer to help arrive at the important analysis cases using fewer parametric runs than traditional methods. 
Some of the industry standard programs are ESARAD, TRASYS, THERMICA, SINDARadCAD (radiation exchange packages) and ESATAN, SINDA (Lumped finite-difference thermal balance packages)

(MCRT)=
## Monte-Carlo Raytracing 

The Monte-Carlo Raytracing (MCRT) method considers the individual history of thermal radiation energy, from the point of emission to the point of absorption. 
These energy packets may follow an infinite number of paths: rays can be emitted from any point on every radiative face, in any direction, and may reach and be reflected by any other radiative face in the model. 
An estimate of the radiative couplings (and heat fluxes) can be made by averaging the results obtained from a finite random sample of rays.
The MCRT is therefore a stochastic method. 
The individual history of each ray: its emission point, emission direction and ray/face interaction, is randomly determined. 
This means that to obtain high fidelity there is likely to be a high computational cost. 
A potential issue of the MCRT method is that surfaces with low emissivity may take longer to find an accurate value. Another source of errors lies in the fact that the reciprocity law in the MCRT
radiative coupling calculations: matrix line sums will not be exactly one. 

ESARAD (now integrated in ESATAN) takes care of the Montecarlo Raytracing. 
The current version has three types of accuracy each with their own advantages and disadvantages. 
- Use a fixed number of rays per face. Total cutoff: percentage of the total energy emitted from a face that can be excluded from the results (default: 0.005)
- Use ray density per face
- Use accuracy control→ Desired accuracy of the line sums
 
 ## Lumped finite-difference
 
 Numerical discretization is the process of converting partial differential equations into algebraic equations. 
 Currently, the available methods for discretizing time differential items are limited to explicit, implicit, and Crank-Nicolson methods. 
 Hence, the general discretization methods primarily address the handling of spatial differential terms. 
 As a result, typical thermal analysts are not exposed to the process of dividing spatial differential elements into discrete units. 
 Nonetheless, understanding the discretization method used in thermal analysis software is useful for understanding the configuration of certain boundary conditions, as well as the rules governing the output or mapping of analysis results.
 
 ### Use of Finite Elements Method in thermal analysis

Heat transfer exhibits significant nonlinearity, particularly in radiation, and thermal analysts strive to minimize the number of thermal elements (nodes) in order to decrease computational effort and cost. 
An advantage of finite element methods is their versatility in performing both thermal and structural analysis using the same program. 
If there is a significant difference between the thermal and structural node, joint analysis of thermal and structural models in structural finite element programs is not possible due to the absence of similar constraints. 
Practically, this discrepancy will impose a burden on the structural analyst, as they will need to estimate temperatures in their structural model in order to calculate thermal distortions. 
On the flip side, a thermal analyst may dedicate a significant amount of time assessing conduction in a model that only loosely resembles an actual structure.
