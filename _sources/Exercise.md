# Exercises

## Blackbody Earth

Calculate the radiant flux in an orbit at 200 km altitude that is emitted by the earth. Assume that Earth is a black body, Black body temperature T = 252 K and Earth mean radius R = 6371 km. 

```{admonition} Click to see the solution
:class: dropdown, tip
The solution goes here
```
## Heat Balance in a Cube
Consider a 1 m cube, where the panel -Z  points to nadir, and the Y axis corresponds to the flight direction. 
The panels in ±Z and ±Y have the following optical properties: $\alpha_s /\epsilon$  = 0.15/0.75 (SSM) whereas the ±X panels have view to space and are perfectly insulated. 
The cube follows a polar earth orbit at 750 km altitude and the fluxes per panel can be seen in the {numref}`exercise2`. 

```{list-table} Orbit averaged absorbed fluxes per panel (in W)
:header-rows: 1
:name: exercise2

* - 
  - Solar
  - Albedo
  - Earthshine
  - Electrical Dissipation
* - Nadir -Z
  - 7 W
  - 12 W
  - 150 W
  - 50W
* - Zenith +Z
  - 50 W
  - 0 W
  - 0 W
  - 250W
* - Side +Y and -Y
  - 2 x 35 W
  - 2 x 4 W
  - 2 x 45 W
  - 2 x 150 W  
```

**What is the temperature of the Cube?**
You can assume that the body is isothermal. 
This means that there are no temperature gradients within the body, because the body is considered as a single point, or a single node.

```{admonition} Click to see the solution
:class: dropdown, tip
$Q_{in}=Q_{solar}+Q_{albedo}+Q_{earthshine}+Q_{disipation}=987 W $

$Q_{out}=A_{zy}\cdot \epsilon \cdot\sigma\cdot T^4$

Solving for T: 

$T=276K=3^{\circ} $ 
```

