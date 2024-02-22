---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

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
* $\sigma$ = Stephan Boltzmann’s constant = $5.67\cdot 10^{-8} W/m^2/K^4$

Note in that Planck’s law uses the Boltzmann’s constant k, and Stephan Boltzmann’s law uses the Stephan Boltzmann’s constant $\sigma$. 
While named after the same person, these are not the same constants and have vastly different values and units. 
During this course you will make a lot of use of the Stephan Boltzmann’s constant $\sigma$, the other we won’t encounter again. 

The black body radiation as function of the wavelength for several temperatures are graphed bellow.
It shows that the magnitude of the peak and total radiation changes with the temperature. Higher temperatures will emit more radiation overall, and the peak of the graph is located at lower wavelengths. 
Compare for example the sun with a glowing ember; the sun it hot white, while the relatively cooler ember glows in a deep red. 

```{code-cell} ipython3
:tags: [hide-input]

from matplotlib import pyplot as plt 
import numpy as np
import warnings

h = 6.62607015e-34 
c = 2.99792458e+8
k = 1.380649e-23 
pi = np.pi

warnings.filterwarnings('ignore')


def planck(wav, T):
    a = 2.0*pi*h*c**2
    b = h*c/(wav*k*T)
    intensity = a/((wav**5)*(np.exp(b)-1.0))
    return intensity

wavelengths = np.arange(1e-9, 3e-6, 1e-9)

temperatures = [2000, 3000, 4000, 5000, 6000]

for T in temperatures:
    intensity = planck(wavelengths, T)
    plt.plot(wavelengths*1e9, intensity*1e-12, label=f"T={T}K")

plt.xlabel("Wavelength (nm)")
plt.ylabel("Intensity (kJ/nm)")
plt.title("Planck's Law")
plt.legend()
plt.show()
```

The wavelength at which the peak of the radiation occurs is inversely proportional to the temperature of the black body. 
This effect is described by Wien’s displacement law:

$$
\lambda_{max}\, T \approx 2898 [\mu m \, K]

$$(WienLaw)

Using Wien’s displacement law, it is possible to determine the peak radiation point of any black body. 

```{list-table} Wien's Law
:header-rows: 1
:name: WienLawTable

* - 
  - Sun
  - Boiling Water
  - Earth
* - Blackbody Temperature
  - 5788 K
  - 372 K
  - 252 K
* - $\lambda_{max}$
  - 0.5 $\mu m$
  - 7.8 $\mu m$
  - 11.5 $\mu m$
```