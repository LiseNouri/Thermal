# Spacecraft Thermal Environment

Spacecraft encounter a number of environments during their lifetime. In space the spacecraft is under the influence of: Deep space, Solar radiation, Albedo and Planetary infrared radiation

## Deep Space
Deep space is the cold darkness that surrounds the spacecraft. Due to cosmic background radiation, the temperature of deep space is 2.7K. For most engineering purposes this is set at 3K.[^ECSS] 
Taking into account the background radiation is significant for certain applications, such as cryogenic radiators and sensors. However for other application, it can also be neglected, e.g. the thermal balance of a rocket nozzle. 

[^ECSS]: [European Cooperation for Space Standardization - ECSS](https://ecss.nl/)

## Solar Radiation

Solar {term}`radiation` is the heat coming from the sun. The solar spectrum can be approximated by a black body curve with a temperature of 5778K [^ECSS], the peak of this spectrum is around 500nm wavelength. Most power of this radiation is in the familiar visible spectrum.

The heat produced by the sun is represented by the Solar Constant $S_\odot^N$, expressed in $W/m^2$. 
```{glossary}
The Solar Constant: 
	The value of the nominal total solar irradiance corresponds to the mean total electromagnetic energy from the Sun, integrated over all wavelengths, incident per unit area, and per unit time at a distance of 1 AU.
``` 
The current best estimate of the Solar constant is 1361 W/m2. 
Note that the Solar Constant is a mean value and should not be strictly considered a constant. 
The long term solar cycle varies approximately with 1.3 W/m2. {cite}`SpaceEnvironment`
The nominal value for the solar constant was determined officially in IAU 2015 resolution B3, during your career you are likely to encounter slightly different values from older documents. (Prsa et al, 2016, nom values).
A satellite around earth is exposed to different levels of solar radiation. When the earth is at Aphelion (summer solstice) it will be 1316 W/m2, in Perihelion (Winter solstice) 1407 W/m2. 

## Albedo
Solar radiation is also reflected by planetary bodies. When it is reflected by earth this is called Albedo. 
When the light is reflected, the spectral properties are not changed, though the radiation is assumed to be diffuse after reflection. 
In other words, the albedo radiation does not travel in parallel rays. 

Typically albedo is expressed as a fraction of the solar constant. 
An average value is 0.3. this means 30% of the power of the solar radiation is reflected, thus the heating of the albedo power is $0.3 \cdot 1361\, =\, 408 W/m^2$.
Albedo varies locally in an orbit, especially around earth. You can see this yourself, deep sea is almost black, while snow and white clouds are very reflective. 

You can see in this figure that the snowy polar regions are much more reflective than the equatorial regions. 
Note also that albedo only occurs on the sunlit parts of the globe. This figure was taken in winter, thus there is no reflection on the north pole. 


## Planetary Radiation

Planets also emit their own radiation. This radiation is emitted in the infrared spectrum in a diffuse manner. 
The average infrared radiation for earth is 230 W/m2 (black body spectrum with a temperature of -21 deg. C, this is a spectrum with the peak between 10 and 15 µm), but can vary from 150-350 W/m2. 
The amount of infrared radiation varies based on latitude, whether it is day or night and part of the earth. 
In general the infra-red radiation is higher around the equator.

## Orbital effects

The orbit of a spacecraft also changes the thermal environment. 
- Sun synchronous dawn/dusk orbit: this orbit has no eclipse and near-constant solar flux
- Sun synchronous orbit: Sun will always come from the same general direction.
- LEO circular orbit: Can have an eclipse (max. 40 minutes), and significant impact of earth radiation.
- (Highly) Elliptical orbit: Large variation in planet fluxes, potentially very long eclipses (hours)
- Geostationary orbit: Only seasonal eclipses

The effect of the environments described in the previous sections, is dependent on the orbit of your spacecraft. 
For a typical mission of a Spacecraft in orbit, the thermal engineer will need to consider the planetary albedo and infrared radiation of the body it orbits and the solar input. 
So for example for a regular satellite orbiting the earth, the influence of earth and sun needs to be considered, but the thermal effect of the moon can be ignored. 
For a satellite on an interplanetary trajectory or in a Lagrange point, or even a trajectory between the moon and earth, only the sun can be considered. 
It is of course up to the Thermal engineer to decide whether these influences are indeed negligible. 

The orbit of a spacecraft is chosen for mission specific reasons. 
In the following paragraphs, some characteristics will be described. 

Many satellites fly in a sun-synchronous dusk dawn orbit in LEO. 
This orbit is nearly circular and praised for its constant light conditions. 
The thermal environment of a satellite in this orbit is also very constant. 
There are mostly no eclipses and hardly any orbital variation in the thermal conditions. 
The albedo and planetary radiation will also be relatively constant, as the satellite has the same altitude throughout the orbit, and the satellite (if nadir pointing) will have the same orientation with respect to the sunlit part of the planet. 

Any orbit LEO circular orbits will encounter eclipses, which vary with the season due to the solar inclination. 
The eclipse can be up to 40 minutes long. Note that these satellite will experience a lot of eclipses, and thus thermal cycles, throughout their lifetime. 
The influence of albedo and earth radiation is significant. 

A elliptical orbit, for example a molniya orbit will see more variation throughout their orbit, as the satellite travels from a low altitude in perigee to a high altitude in apogee.
As the satellite will spend a long time in apogee, the thermal engineer might want to check whether this can occur in eclipse in any season. 
With some elliptical orbits this eclipse time can reach hours, which will be a driving thermal case. 

A satellite in GEO will have significantly less influence from the planet onto its thermal environment, though it cannot entirely be ignored. 
The satellite will be illuminated from all sides, every day. It will also encounter some seasonal eclipses due to the solar inclination. 
The number of eclipses can be a lot less, compared to a LEO orbit, but can be up to 70 minutes. 

When considering orbits around other objects in our solar system, their specific constraints need to be considered. 
For example, a spacecraft in Mercury orbit needs to consider the divergence of the solar rays, due to the proximity of the sun. 
Mercury also has a very slow rotation, so the planetary radiation greatly varies between the sun facing side and the dark side. 

## Internal heat sources

The satellite has  a lot of internal heat sources. All electronics will dissipate heat. 
Dedicated heaters can raise the temperature and propulsive modules heat up. 
The plume generated by propulsive modules can also heat up other parts of the spacecraft when pointed at them. 
This might be particularly relevant for antennas and solar arrays, as they often extend from the spacecraft body

## On-Ground environments
Before the satellite reaches orbit, it will spent a considerable amount of time on the ground. 
To keep the systems safe, often the environment is controlled. Integration facilities are typically controlled at room temperature, and transportation happens in specialized containers with temperature control. 
Note that even specialized containers left out in the sun might heat up to unacceptable levels. 
The integration and many test occur also under none-vacuum conditions. 
This means convection can cause unexpected effects. 

One example of this is that convection might cool electronics during regular testing, while in space these elements might overheat due to the lack of convection. 
Once the system is integrated on the launch vehicle, it will also mostly be in a temperature controlled environment. 
Launch providers provide the temperature environment they offer in the launch manual. 
Once encapsulated and on the pad, the environment might be less controlled. 
This can be seen in the outtakes of the manuals for Ariane 5 {cite}`Ariane5` and Falcon 9 {cite}`Falcon9`. 
Ariane 5 only specifies the air temperature in the last phases, whereas the falcon 9 does not offer any temperature control for the rollout of the system. 


## Ascent environment

During ascent into orbit, the spacecraft will encounter a number of thermal effects:
- Thermal environment under the rocket fairing: 
- Aerothermal heating after fairing jettison
- Heating due to the rocket plumes


For the first minutes of a rocket flight, the satellite is under a fairing. 
This fairing will heat up significantly due to the aerodynamic friction with the atmosphere. 
The satellite is under the fairing for only a short mount of time, as a whole the satellite is unlikely to be affected, but external components can be, such as the insulation, external paint, radiators or solar panels. 
The heating under a fairing can be expressed as a infra-red flux (as done for Vega-C {cite}`VegaC` and Ariane 5 {cite}`Ariane5`), or as a temperature (As done by e.g. Falcon 9 {cite}`Falcon9` and {cite}`AtlasV`).

Vega-C and Ariane 5 manual state that the radiation due to heating of the fairing is at maximum 1000W/m2. Below is the figure from the Atlas manual, showing a peak temperature of 200 deg. C for parts of the fairing. 


After fairing jettison, the satellite itself is exposed to this aerothermal heating due to the free molecular flow. 
Generally the fairing is deployed when this effect drops below 1135 W/m2. The exact heating profile depends on the mission profile of the launcher. The effect decrease rapidly after fairing jettison, but can rise and drop during the mission. Also This will mainly affect external systems with a low thermal mass. 


In general thermal flux coming from the 1st and 2nd stage can be ignored. 
It is possible that 3rd stage engine fluxes can impinge on the spacecraft, the engine is located closer to the spacecraft, and outside the atmosphere the plume will expand a lot more. 
The Vega launcher for example can hit the “bottom” of the satellite with 1500W/m2 for a maximum of 2 minutes. 

