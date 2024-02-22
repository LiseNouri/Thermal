# Exercises

## Blackbody Earth

Calculate the radiant flux in an orbit at 200 km altitude that is emitted by the earth. 
Assume that Earth is a black body, Black body temperature T = 252 K and Earth mean radius R = 6371 km. 

```{admonition} Click to see the solution
:class: dropdown, tip
$Q_{total}=4\,\pi\, R^2\, \sigma \,T^4 $

$Q_{total}= 4\,\pi\, (6371+200)^2\, 5.67\cdot 10^{-8} \,252^4 = 128.05[MW]
$
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
##  Heat Balance in a Spacecraft
Consider a spacecraft with two radiators of A m2 each. 
One radiator is permanently pointing to the Sun with a normal incidence, the other one is permanently in shade. 
The radiators are Optical Solar Reflectors (OSR) with the following optical properties $\alpha/\varepsilon =0.1/0.8$. 
In this case, we only consider the heat solar input ($S=1400W/m^2$) and there’s an internal equipment dissipation of 165W. 
The spacecraft may be represented as one node. 

- What is the required radiator areas when the maximum temperature of the spacecraft is 33 degrees ?

```{admonition} Click to see the solution
:class: dropdown, tip
First we establish the heat balance: 

$Q_{in} = Q_{sun} +Q_R =\alpha A S +Q_R $

$Q_{out} = 2 A \varepsilon \sigma T^4 $

$Q_{in}= Q_{out}$

$\alpha A S +Q_R =2 A \varepsilon \sigma T^4 $

Solving for the area (A): 

$A=\frac{Q_R}{2 \varepsilon \sigma T^4 -\alpha S}$


```

- With that area, what is the heater power demand to keep $T_{min}>= -30$ degrees when the equipment is all off? 

```{admonition} Click to see the solution
:class: dropdown, tip
$Q_{in} = Q_{sun} +Q_{heater} =\alpha A S +Q_{heater} $

$Q_{out} = 2 A \varepsilon \sigma T^4 $

$Q_{in}= Q_{out}$

Solving for the heat power demand: 
$Q_{heater}=2 A \varepsilon \sigma T^4 - \alpha A S$


```

## Radiation Exchange in a Spacecraft

Assess view factor between solar panel rear side and S/C side wall and space. 
Consider first that the solar panel size is 100 x 200 mm and S/C side wall is 100 x 300 mm. 
Repeat for S/C side wall 100 x 50 mm. 

```{admonition} Click to see the solution
:class: dropdown, tip
The solution is in lecture W2.2

```

## Two Infinite Plates

```{figure} images/InfinitePlates.png
:height: 500px
:name: InfinitePlates
Heat flows of two infinite plates
```
```{admonition} Click to see the solution
:class: dropdown, tip
The solution goes here
```

## SPEXone Polarimeter
PACE's SPEXone instrument [^label1] is a multi-angle polarimeter that measures sunlight intensity, Degree of Linear Polarization (DoLP), and Angle of Linear Polarization (AoLP) from Earth's atmosphere, land surface, and ocean. 
Its development aimed to achieve high accuracy in DoLP measurements, enabling accurate characterization of aerosols, which are a significant source of error in climate change quantification.

The development of SPEXone is the result of a collaboration between SRON Netherlands Institute for Space Research and Airbus Netherlands, with help from experts from TNO and other dutch companies.

[^label1]: [SPEXone instrument](https://pace.oceansciences.org/spexone.htm)

Some characteristics of the instrument are: 
* Heat dissipation: 12 W
* Size: 40x30x15 $cm^3$
* Radiator facing space: $\alpha/\epsilon$ = 0.2/0.8 (Solar White)
* SLI towards Spacecraft, radiative link with $\alpha/\epsilon$ = 0.14 / 0.035
* 3 Ti alloy struts: k= 7 W/m K, L =15cm, A = $2 cm^2$ per strut 
* Connection Radiator - Instrument: Strap: 1 W/K
* $T_{SC}$ = 270 K, assumed black body 
* Environment: 45 W on radiator

Considering that the instrument has an operational temperature of 25 degrees, is this a good thermal design? How would you improve it?

```{admonition} Click to see the solution
:class: dropdown, tip
The solution goes here
```