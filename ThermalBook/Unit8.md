# Thermal Verification and Testing



## Thermal Tests
 
 Thermal Management Hardware
In general 25% of margin is used. This means that the heater should be oversized to 25%. Temperature margin of 11 degrees for passive methods. 
This value comes from the Spacecraft thermal control handbook reference. 

- Pasive 
- Active
Heaters
- Test heaters
- Survival heaters


3 types of TV temperature sensors: 

Thermocouples(TC), uses two wires to produce a voltage relative to the temperature present in the junction between them. 
Temperature range is 200 to 1750 degrees
TC are the most popular. There is some types within as well. 
The most popular is K type. Other types as J, E, and T. 


Accuracy (needs calibration) can be 0.5 to 5 degree 
Resistance Temperature Detector(RTD)
Very slow, the typical response time is 1 to 50 seconds. 
High cost
Thermistor. Mostly used in flight.

How do you attach the temperature sensor to the test equipment? 
Glue: thermally conductive epoxy. Issue is that is difficult to remove.

Screw: don't want to do in flight hardware.

Tape: very popular, most recommended method for thermal vacuum tests

Where to place the sensor is critical, especially if large thermal gradients are needed. 


 
### Thermal Cycle Tests

Thermal cycling subjects the test article to a number of cycles of hot and cold temperature plateaus in an ambient air or gaseous nitrogen environment. 
Convective heat transfer is enhanced such that the cycling can be relatively rapid. 
Cycling serves primarily as an environmental stress screen by revealing latent workmanship or material defects. Performance verification is a secondary objective accomplished through functional tests performed at hot and cold temperature plateaus.

Prior to the test, a test plan must be available describing the procedures and the 
functional testing to be performed. 

Where practical, functional testing described in the test plan should be rehearsed with the unit at ambient temperature. 
The functional tests performed prior to (and following) the thermal cycle test should be identical to the functional tests that will be performed during the test. 

Unit thermal cycling is typically performed in a thermal cycling chamber, where 
temperature-controlled dry air or gaseous nitrogen is used to heat or cool the unit.
 
The nitrogen or dry air is used instead of ambient air to prevent moisture conden- 
sation on electronic parts or circuitry. 

During the heating cycle, the dry air or 
nitrogen is heated from the walls of the chamber. Usually direct heating need not 
be applied to the test article or to the mounting shelf. 

Cooling is accomplished by 
pumping liquid nitrogen through cooling tubes or coils mounted to the chamber 
baseplate. 

The baseplate is usually made of copper to provide good conduction 
over the interface with the test article. 

The environment is circulated with fans to prevent temperature gradients on the test article and to speed transitions in temperature. 

Baffles or flow directors are sometimes employed to better direct the circulating environment. 

When selecting a thermal chamber for a particular test, keep in mind that if relatively little room separates the internal walls of the chamber and the unit itself, air or gaseous nitrogen movement around the unit will be reduced. 

This may result in thermal gradients in the unit and a temperature-transition rate of change that is lower than desired. 



### Thermal Vaccum Tests
Thermal vacuum tests subject the test article to a number of cycles of hot and cold 
temperatures in a vacuum environment. Because it is conducted without convec- 
tive heat transfer, this test is the most realistic ground simulation of the flight envi- 
ronment. Therefore its primary purpose is performance verification through 
functional testing. Temperature transition is slower than in the thermal cycling 
test, so stress screening is of secondary importance. 

The temperature range and extremes in the unit thermal vacuum test are identical to the thermal cycle test parameter requirements. 

Acceptance tests are performed at minimum and maximum expected temperatures, or at least-24 to +6 I°C, and qualification tests are performed at minimum and maximum expected temperature +_10°C, or at least-34 to +71°C


### Thermal Balance Test
Thermal balance tests, usually performed as part of subsystem or space vehicle 
thermal vacuum testing, have two purposes: verification of the thermal control subsystem and correlation of thermal analytic models. Dedicated test phases that 
simulate flight conditions are used to gather steady-state temperature data that are 
compared to model predictions. Test phases also simulate cold and hot conditions 
to verify all aspects of the thermal hardware and software, including heater opera- 
tion, radiator sizing, and critical heat transfer paths. 

### Burn-In Tests
Burn-in tests are typically part of unit thermal cycle tests in which additional test 
time is accrued to meet a set requirement. The unit is either cycled or held at an 
elevated hot temperature during the burn-in test, and the unit is operational, 
although functional tests are not performed. 

## Images

```{figure} images/CleanRoom.png
:height: 500px
:name: CleanRoom

```

```{figure} images/VaccumChamber.png
:height: 500px
:name: VaccumChamber

```

```{figure} images/JuicePanels.png
:height: 500px
:name: JuicePanels

```

```{figure} images/HalogenLamps.png
:height: 500px
:name: HalogenLamps

```