# Radiation and Heat Balance

## Black Body Radiation

A perfect body emits and absorbs the maximum amount of radiation at all wavelengths only as a function of the temperature of that body. 
The spectral of a black body at a given wavelength and temperature can be described by Planck’s law:

$$
\Phi_b(\lambda, T)=\frac{2\pi h c^2}{\lambda^2} \frac{1}{e^{\frac{h\cdot c}{k\cdot T \lambda}}-1}

$$(PlanckLaw)

Where:
* $\lambda$ = wavelength
* T = absolute temperature
* k = Boltzmann’s constant = $1.4\cdot 10^{-23} kg \cdot m^2/s^2/K$
* h = Planck’s constant = $6.6\cdot 10^{-34} kg \cdot m^2/s$
* c = velocity of light in vacuum = $3 \cdot 10^{8} m/s$

Integrating over the wavelength spectrums, results in Stephan Boltzmann’s law, the total flux emitted per unit area as a function of only temperature. 

$$
\Phi_{total}(T)= \int \Phi_b(\lambda, T) d\lambda = \sigma T^{4} [\frac{W}{m^2}]

$$(StephanBoltzmann)

Where
*$\sigma$ = Stephan Boltzmann’s constant = $5.67\cdot 10^{8} W/m^2/K^4$

Note in that Planck’s law uses the Boltzmann’s constant k, and Stephan Boltzmann’s law uses the Stephan Boltzmann’s constant $\sigma$. 
While named after the same person, these are not the same constants and have vastly different values and units. 
During this course you will make a lot of use of the Stephan Boltzmann’s constant $\sigma$, the other we won’t encounter again. 

The black body radiation as function of the wavelength for several temperatures are graphed in Figure 3. 
It shows that the magnitude of the peak and total radiation changes with the temperature. Higher temperatures will emit more radiation overall, and the peak of the graph is located at lower wavelengths. 
Compare for example the sun with a glowing ember; the sun it hot white, while the relatively cooler ember glows in a deep red. 

The wavelength at which the peak of the radiation occurs is inversely proportional to the temperature of the black body. 
This effect is described by Wien’s displacement law:. 