# Background Theory and Key Concepts

## Key Concepts:

This part of the lectures introduces some key concepts, and introduces a global overview of the thermal subsystem. More detail will be provided in subsequent lectures. 
> this is a quote
>
> 
### Why spacecraft thermal control?

- Equipment is only functional in certain temperature ranges. Batteries can lose their charge if they get to cold, or explode if they overheat. The fuel in propulsion systems or the fluids in thermal systems can freeze. 
- Control over temperature gradients is important as temperature gradients introduce deformation. For example for an optical system this can influence the measurements. This can also introduce stresses in the structure, specially at bonded interfaces.
- Temperature swings can cause fatigue in the materials. 
- At the extreme ranges temperatures can cause changes in material properties, e.g. outgassing of adhesives, or brittleness at cryogenic temperatures.

The numbers below form some indication of a characteristic thermal control subsystem for a spacecraft. These number can very per application:
- Appearance: > 95 % spacecraft exterior
- Mass: 2 - 5 % of spacecraft dry mass
- Cost: 3 - 5 % of spacecraft cost
- Power: < 5 % of total spacecraft power


Typical elements of the thermal subsystem are:
- Surface coatings and finishes
- Multilayer insulations and heat shield / barriers
- Radiators
- Mounting materials (struts)
- Interface fillers, noth insulating and conducting
- Passive coolers
- Flexible conductive links
- Heat pipes, both passive (contact conductance) and actively pumped.
- Temperature sensors
- Heaters and thermostats
- Active coolers (e.g. Peltier elements or cryostats)
- Louvers
- Phase change materials

### Heat tranfer

Heat transfer deals with the transfer of the thermal energy between the environment and the space craft and between spacecraft elements. It is either expressed as a heat flow (Q in Watt) or as a flux (q in W/m2). Three mechanisms of heat transfer:
```{glossary}
Radiation
  Heat transfer by electromagnetic radiation, No medium is required for this heat transfer, Most important heat transfer mechanism in space

Conduction
  Heat transfer by molecular interaction, Heat transfer through parts and contact points, Locally important and essential

Convection:
Heat transfer by gas or fluid movement
Absent in the space environment, but can play a role in thermal control or subsystems of spacecraft (e.g. fuel systems, heat pipes, human spaceflight
Can be natural or forced (e.g. by a fan). Works different in space and in a gravity environment. 
```





Thermal design and analysis is involved in all phases of spacecraft design:
- In feasibility phases, the thermal environment is analyzed, rough thermal concepts are compared. Preliminary analysis is performed. In this phase general concept is selected, often with high level (hand) calculations.
- In the preliminary design phase, the preliminary thermal design is defined, and thermal models are developed. The analysis focusses on the worst cases (hot and cold). Some development tests can occur, for which analysis and correlation between test and model needs to be performed. 
- In the detailed design phase, the final Thermal control subsystem design in analyzed. The models are updated, and all mission cases are analyzed. 
- During the qualification the thermal models are adapted for testing. Test predictions and correlations are being made. The thermal models will be updated after these tests. Often the thermal engineer also supports AIT activities with their expertise. At the end of this phase, models and documentation needs to be archived for future use.
- During the utilization phase, mission predictions and flight correlations are performed.

The thermal modelling process starts with the mission requirements (environment, orbit operational requirements) and an spacecraft design (geometry, thermos-optical properties, materials, operation). From this information a geometric (radiative) model and a thermal model are made. A radiative solver will calculate the radiative load and interactions in the spacecraft model. The thermal model represents the conductive couplings, heater settings, heat capacity, heater settings etc.. These two models, are combined in the main thermal mode, which is solved for temperatures, heat fluxes, heater cycles. And thermos-hydraulic parameters. The results are validated.
For hand calculations a roughly similar process is followed. This is an iterative process, as design changes warrant changes to the model. 
