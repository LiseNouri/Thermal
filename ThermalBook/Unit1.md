# Background Theory and Key Concepts

This chapter will introduce some background theory and key concepts needed for thermal engineering. 
## Thermal Control Objectives

Spacecraft operate in environments with extreme and variable temperatures, which can significantly impact system performance and reliability. The following points highlight why thermal control, analysis, and engineering are essential for a successful space mission:

*Operational Temperature Ranges: Spacecraft equipment only functions properly within specific temperature limits. For example, batteries may lose charge if they become too cold or could overheat and explode. Similarly, propulsion system fuel or thermal system fluids can freeze if temperatures drop too low.

*Temperature Gradients: Managing temperature differences across the spacecraft is also important. Uneven temperatures can cause deformation, which is especially critical in precision systems like optical instruments, as it can affect measurement accuracy. Additionally, temperature gradients can introduce mechanical stresses, particularly at bonded interfaces which can potentially lead to structural failure.

*Material Fatigue: Repeated temperature swings can lead to material fatigue over time, compromising the integrity of spacecraft components.

*Material Property Changes: Extreme temperatures can alter material properties. For instance, adhesives may outgas at high temperatures, and materials can become brittle under cryogenic conditions.

*Performance-Dependent Temperatures: Certain systems require specific temperature conditions for optimal performance. For example, solar cells operate more efficiently at lower temperatures, sensors generate less noise when cooler, and a 3D printer must heat materials to their melting point to function properly.


## Types of Heat tranfer

Heat transfer deals with the transfer of the thermal energy between the environment and the spacecraft and between spacecraft elements. It is either expressed as a heat flow (Q in Watt) or as a flux (q in W/m2). Three mechanisms of heat transfer:
```{glossary}
Radiation
  Heat transfer by electromagnetic radiation. No medium is required for this heat transfer. Heat is transported from one surface to another. 
  This is also how the external fluxes from sun and planets transfer heat. This is the most important heat transfer mechanism in space. 

Conduction
  Conduction is the heat transfer by molecular interaction. This is heat transfer through parts and contact points. 
  Locally this is important and essential within your system. 

Convection:
	Convection is the heat transfer by gas or fluid movement. 
	This is absent in the space environment, but can play a role in thermal control or subsystems of spacecraft (e.g. fuel systems, heat pipes, human spaceflight). 
	Convection can be natural or forced (e.g. by a fan). Note that convection works different in space and in a gravity environment. Convection occurs due to a combination of temperature and density differences in the fluid, and body forces such as gravity. In a gravity environment hot fluids rise up as it is lighter than the surrounding fluids. 

```
## Heat Flux, Heat flow and Heat Transfer
Heat transfer and heat flow is the transfer of thermal energy (heat) per unit time. 
This is denoted with the symbol a capital Q. This is a scaler and expressed in Watt (W=J/s).

Heat Flux is the transfer of thermal energy (heat) per unit time per unit area. 
This is denoted with a Φ. The heat flux is a vector and expressed in W/m2 (=J/s/m2)

## Temperature ranges

During your time as thermal engineer you will encounter references to specific temperature ranges. 
The exact definition can differ but in general:
- The High temperature range considers temperature above 470K. 
- The cryogenic temperature range considers temperatures below 200K.
Two other important temperatures to remember:
- 273.15 K = 0 °C : Useful for conversion between Kelvin and Celsius. Both are used in thermal engineering. 
- 77 K  = -196 °C: Boiling point nitrogen. Many cold test are cooled with nitrogen. 
This means testing close to or lower than this boiling temperature is a lot more difficult. 

## Thermal Control Objectives
Why spacecraft thermal control, analysis and engineering?

- Equipment is only functional in certain temperature ranges. Batteries can lose their charge if they get to cold, or explode if they overheat. The fuel in propulsion systems or the fluids in thermal systems can freeze. 
- Control over temperature gradients is important as temperature gradients introduce deformation. For example for an optical system this can influence the measurements. This can also introduce stresses in the structure, specially at bonded interfaces.
- Temperature swings can cause fatigue in the materials. 
- At the extreme ranges temperatures can cause changes in material properties, e.g. outgassing of adhesives, or brittleness at cryogenic temperatures.
- Certain temperatures might be needed for certain performance. Solar cells are more efficient at lower temperatures, sensors measure less noise at lower temperatures and a 3D printer needs to heat materials to melting point. 

## Thermal Control Requirements
These needs lead to a number of typical thermal requirements onto the thermal subsystem:
- Temperature range, both for operations and qualification:
These requirements are defined to keep system in their survival or operational range. This is to secure the integrity of materials, an optimal functioning of parts and to keep parts within their tested range. 
- Temperature gradients and uniformity
These requirements are defined to keep a temperature uniform over a certain area. This is important for alignment of parts and internal stresses. Sometimes these requirements are defined to make sure any part of a system is within a small range from the point where the temperature is measured. 
- Temperature stability
These requirements are defined to keep temperatures uniform over time. This is important for sensors for example, and ensures measurements are taken in similar conditions. 
- Interface heat flux and flows
Interface requirements are defined to help the systems design
Other requirements onto the thermal system often include:
- The thermal environment
- Electrical power and other consumables (e.g. coolant that boils off. )
- TM/TC allocation
- Mass
- Limits on optical properties for a system
The amount of systems requirements depend on wether an active or a passive system is required. An active system needs power and communications from the satellite bus. A passive system will always work. 
The thermal environment will both define on-ground conditions and orbital conditions. More on this topic in the next chapter. 


