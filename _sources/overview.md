# Overview of high energy astrophysics

We start the course by thinking about what physics might be relevant for sources that emit high energy photons and sources in which high energy processes are relevant. This will set us up for the rest of the course by highlighting some questions we will need to address and the kinds of astrophysical sources we should look at. This discussion will also serve to introduce some of the notation and units that we'll be using.

## What is High Energy Astrophysics and why is it interesting?

If you start to look at some of the textbooks, you'll see that they often begin with some discussion of the scope of high energy astrophysics. Many different types of astrophysical source show high energy emission, for example, the giant planets of our Solar System emit X-rays! Moreover, sources that are traditionally included in high energy astrophysics are often bright at other wavelengths. Classic examples are radio galaxies, discovered with first radio telescopes well before the detection of AGN in X-rays, or radio pulsars, many of which do not have detectable X-ray or gamma-ray emission.

This fits with the history of the field, which began with the development of multi-wavelength astronomy in the mid-20th century, first with radio telescopes and then later X-ray and gamma-ray observations from space.  Today, high energy astrophysics is at the heart of multi-messenger astronomy involving neutrino and gravitational wave observatories. 

A general definition of High Energy Astrophysics is the study of astronomical sources in which high energy processes play a role. We shall see that leads naturally to extreme environments, with some combination of high densities or temperatures, relativistic velocities or particle energies, high luminosities, rapid variability, or strong gravitational or magnetic fields. This leads to a surprising range of astronomical sources falling under the umbrella of High Energy Astrophysics, from accreting supermassive black holes to radio pulsars, from supernova remnants to galaxy clusters, and more. We want to understand how these sources work and explain observations of them, but also in turn they offer the opportunity to study properties of matter under conditions that cannot be reproduced in laboratories on Earth.

## Thermal emission as a source of high energy photons

When would we expect an astrophysical source to emit high energy photons (X-rays or gamma-rays)? Perhaps the simplest place to start is thermal emission, ie.~radiation from a gas in thermal equilibrium at temperature $T$. 

### Optically-thick source

For an optically-thick source at temperature $T$, the photons interact with the plasma many times before they leave and the spectrum is a Planck or blackbody spectrum ($B_\nu(T)$ or $B_\lambda(T)$). The peak of the spectrum is given in terms of $T$ by 

$$
\nu_\mathrm{max}=5.88\times 10^{10}\ {\rm Hz}\ \left({T\over \mathrm{K}}\right)
$$

or

$$
\lambda_\mathrm{max} T =0.290\ {\rm cm\ K}
$$

(Wien's displacement law).

```{note}
Note that $\lambda_\mathrm{max}$ is close to but not equal to $c/\nu_\mathrm{max}$. Why not? 
```

For example, the Sun has $T_\mathrm{eff}\approx 5800\ \mathrm{K}$ which gives $\nu_\mathrm{max}=3\times 10^{14}\ \mathrm{Hz}$ and $\lambda_\mathrm{max}\approx 5\times 10^{-5}\ \mathrm{cm}$ $\approx 5000\ $ $\mathring A$. If we want X-ray wavelengths, let's say 

$$
\lambda\sim 1\ \mathring A = 10^{-8}\ \mathrm{cm};\hspace{1cm}  \nu = {c\over\lambda} = 3\times 10^{18}\ \mathrm{Hz},
$$

we need 

$$
T\approx 3\times 10^7\ \mathrm{K}
$$

or 30 million degrees! This is obviously much larger than the effective temperature of the Sun, in fact it is more like the temperature at the centre of the Sun, which is $\approx 2\times 10^7\ \mathrm{K}$. Thermal photons in the centre of the Sun are X-ray photons, but they are at such high density that they can't escape; we see only the much lower energy photons from the low density regions at the surface (photosphere).

```{note}
In fact, the Sun *is* a source of X-rays. The tenuous solar corona consists of $\sim 10^6\ \mathrm{K}$ gas that is detectable in X-rays. But the X-ray luminosity is a small fraction of the luminosity, $L_X\sim 10^{-5}\,L_\odot$.
```

At high energy, it's useful to think about temperature in units of eV as well as K. In cgs units, $1\ \mathrm{eV}=1.6\times 10^{-12}\ \mathrm{erg}$ (where $1\ \mathrm{erg} = 10^{-7}\ \mathrm{J}$ is the cgs unit of energy). Setting $k_BT = 1\ \mathrm{eV}$ gives 

$$
T = 1.16\times 10^4\ \mathrm{K}\ \left({E\over 1\ \mathrm{eV}}\right) = 1.16\times 10^7\ \mathrm{K}\ \left({E\over 1\ \mathrm{keV}}\right).
$$

So the blackbody temperature we need to get X-rays is $\sim \mathrm{keV}$ (which is another way of saying that the energies of X-ray photons are of order $\mathrm{keV}$). Wikipedia gives a range $\approx 100\ \mathrm{eV}$ to $\approx 100\ \mathrm{keV}$ for the X-ray band, corresponding to temperatures between $\approx 10^6$ and $10^9\ {\rm K}$. 

A smaller star has to have a higher temperature to emit the same luminosity.
As a thought experiment, let's estimate the size of a star with solar luminosity that would emit in X-rays. Using $L=4\pi R^2\sigma T_\mathrm{eff}^4$ for a blackbody gives 

$$
R=3\ \mathrm{km}\ \left({T_\mathrm{eff}\over 3\times 10^6\ {\rm K}}\right)^{-2}\left({L\over L_\odot}\right)^{1/2}.
$$ 

You might remember that $3\ \mathrm{km}$ is the Schwarschild radius ($R_S=2GM/c^2$) for a solar mass black hole, it's also not far off a neutron star radius of $\approx 10\ {\rm km}$. Young cooling neutron stars have $L\sim L_\odot$ ($L\sim 100 L_\odot$ for bright magnetars), and are seen as thermal X-ray emitters. Turning this around, taking radii corresponding to neutron stars or white dwarfs gives 

$$
\mathrm{NS}\hspace{1cm}R=10\ \mathrm{km}\hspace{1cm}T = 0.13\ \mathrm{keV}\ \left({L\over L_\odot}\right)^{1/4}
$$

$$
\mathrm{WD}\hspace{1cm}R=10^4\ \mathrm{km}\hspace{1cm}T = 4.1\ \mathrm{eV}\ \left({L\over L_\odot}\right)^{1/4}.
$$

This shows that neutron stars should be good sources of thermal X-rays, although white dwarfs with roughly the same radius as Earth already have their emission pushed into the UV/optical range.

### Eddington luminosity

Since the temperature depends on the luminosity, we should ask how large the luminosity could potentially be. In fact, there is a natural upper limit to luminosity, the Eddington luminosity $L_\mathrm{Edd}$. This corresponds to the luminosity where the outwards radiation force on electron begins to exceed the inwards gravitational pull of the star. Assuming the Thomson electron-scattering cross-section $\sigma_T$ for photon scattering, this balance can be written $\sigma_T F_\mathrm{Edd}\approx m_p g$, where $F_\mathrm{Edd}= L_\mathrm{Edd}/4\pi R^2$ is the radiation flux, giving

$$L_\mathrm{Edd}={4\pi GMm_p\over \sigma_T}=1.26\times 10^{38}\ \mathrm{erg\ s^{-1}} \left({M\over M_\odot}\right) \approx 3\times 10^4\ L_\odot\ \left({M\over M_\odot}\right).
$$

In fact, you see this even in the HR diagram for stars: giant stars have luminosities that extend up to $\sim 10^6\ L_\odot$ but no more. Compact objects can easily reach $L_\mathrm{Edd}$ if they are accreting, e.g.~from a companion star in a close binary system, or in AGN where gas accretes onto a supermassive black hole. The accretion luminosity

$$
L_\mathrm{accr}\approx {GM\over R}\dot M
$$

can often reach $L_\mathrm{Edd}$ in these cases. However, note that even at $L_\mathrm{Edd}$, the temperature of a neutron star is $\approx 2\ {\rm keV}$, firmly in the X-ray band. We don't have any hope of making very hard X-rays or gamma-rays in this way.
 
### Optically-thin source

This shows that thermal processes are limited in the photon energies that they can produce. We can do a little better if we think about optically-thin gas rather than optically-thick. In optically-thin gas, radiated photons mostly leave without further interaction with the plasma. Instead of the thermal equilibrium Planck or blackbody spectrum, in this case the emission has a Bremsstrahlung spectrum with photon energies that extend up to $E_\gamma\sim k_BT$ where $T$ is the temperature of the gas. An important example of optically-thin thermal emission is X-ray emission from galaxy clusters. The baryonic mass of galaxy clusters is dominated by hot gas that sits in the dark matter potential with temperature 

$$
k_BT \approx {GM m_p\over R}.
$$

Taking typical values $M\sim 10^{14}\ M_\odot$ and $R\sim \mathrm{Mpc}\approx 3\times 10^{24}\ \mathrm{cm}$ gives a temperature $T\approx 5\times 10^7\ {\rm K}\approx 5\ {\rm keV}$. This is the same order of magnitude as the temperature at the centre of the Sun, but with the crucial difference that the object is optically-thin so these photons can leave, whereas the Sun is extremely optically thick at its centre and the photons are re-absorbed.
 
Another example is accretion onto white dwarfs in compact binaries ("cataclysmic variables"). At some accretion rates, the boundary layer where inflowing matter transitions from the accretion disk to the star is optically thin; the temperature of the plasma is $k_BT\sim  m_pGM/R\sim 100\ {\rm keV}$ giving rise to hard X-ray emission.

### The limits of thermal emission

We see that thermal emission from hot plasma can generate X-rays in a number of different scenarios. However, it is difficult to go much beyond hard X-rays $\sim 100\ {\rm keV}$ ($T\sim 10^9\ {\rm K}$). Note that at high energies, thermal spectra fall off $\propto e^{-h\nu/k_BT}$, so very few photons are emitted at energies substantially above $k_BT$. At low frequencies, thermal emission falls off as $\propto \nu^2$ (Rayleigh-Jeans limit), and so in the radio in particular non-thermal processes are needed to explain observed sources.

```{note}
Even taking the coldest astrophysical blackbody spectrum we could think of, the CMB with $T\approx 3\ {\rm K}$, radio waves are long wavelength compared to the peak, which is around a wavelength of 1 mm for the CMB.
```
 
## Energy scales; how to get to higher photon energies

To explain gamma-rays, we clearly need to go to non-thermal processes. To try to understand how we could generate photons with gamma-ray energies, let's think about different energy scales. We'll see that neutrinos are also a natural consequence of going to higher energies.

### Atomic energy scale

The binding energy of H-like atoms is $13.6\ {\rm eV}\ Z^2$ where $Z$ is the charge of the nucleus (number of protons). For iron ($Z=26$) this is $9.2\ {\rm keV}$ which is in the X-ray range. Indeed, an important emission line is Fe K$\alpha$, in which an electron moves from the 2s to 1s shells. The transition energy is $\approx (3/4) (13.6\ {\rm eV})(Z-1)^2$ (Moseley's law) or $\approx 6.4\ {\rm keV}$ for iron. The shape of this spectral line from black hole accretion disks is used to constrain the black hole spin.

### Nuclear energy scale: gamma-rays and neutrinos

To get to an energy scale corresponding to gamma-ray photons, we must go beyond the atomic scale to nuclear. The scale of nuclear energies is of order MeV and therefore we would expect transitions between internal levels in a nucleus or nuclear reactions will lead to gamma-ray emission.

```{note}
You may have seen the plot of nuclear binding energy for different elements (e.g.~[this version on wikipedia](https://en.wikipedia.org/wiki/Nuclear_binding_energy\#/media/File:Binding_energy_curve_-_common_isotopes.svg)). This shows that the binding energy difference between He and H is $\approx 7\ {\rm MeV}$ per nucleon (this energy is released in H burning in the Sun). Burning He to carbon gives another $0.6\ \mathrm{MeV}$ per nucleon, and then a further $\approx 1\ {\rm MeV}$ per nucleon to the iron group elements. Heavier nuclei are less bound per nucleon compared to iron by an increasing amount as mass increases, up to of order $\sim 1\ {\rm MeV}$. This is why nuclear fission releases energy, as nuclei break apart to form smaller nuclei that are closer to the iron peak and therefore more bound.
```
 
Nuclear reactions are usually happening in very optically-thick environments, so these photons are absorbed by the gas and we don't get to see them. However, many nuclear reactions generate neutrinos that can escape. Solar neutrinos are generated by reactions involved in H burning that convert neutrons to protons inside the nucleus or vice versa (involving weak processes and therefore producing neutrinos or anti-neutrinos). 

### Rest mass

You might imagine that the most efficient means of producing high energy photons would be to use the rest mass of particles. For example, in situations where positrons are produced, they can annihilate with electrons, giving photons with $E_\gamma\approx m_ec^2=0.511\ {\rm MeV}$ (this annhilation line has been detected for example in INTEGRAL observations of the Galactic centre). Another example is pion decay, eg. $\pi^+\rightarrow \mu^+ + \nu_\mu$, with a scale $m_\pi\approx 140\ {\rm MeV}$.  It is worth noting that accretion onto neutron stars and black holes reaches close to the efficiency of rest mass conversion, i.e. $GM/Rc^2\gtrsim 0.1$ for these compact objects, so that $L_\mathrm{accr}\gtrsim 0.1 \dot{M} c^2$ (as we saw earlier, the neutron star has $GMm_p/R\approx 200\ {\rm MeV}$ compared to $m_pc^2\approx 1\ {\rm GeV}$). 

### The Fermi energy in white dwarf and neutron star interiors

White dwarfs and neutron stars are degenerate stars, so the particle energy is set by the Fermi energy which is $\gg k_BT$. Assuming $E_F=p_F^2/2m_e$ $=(\hbar k_F)^2/2m_e$ and $k_F=(3\pi^2 n_e)^{1/3}$, we find $E_F=0.26\ {\rm MeV} (\rho_6Y_e)^{2/3}$ (low mass white dwarf conditions) or $26\ {\rm MeV} (\rho_9Y_e)^{2/3}$ (high mass white dwarf, neutron star envelope). Here, $Y_e$ is the number of electrons per baryon. With such large Fermi energies inside neutron stars, rising to $\sim 200\ {\rm MeV}$ in the interior, nuclear transformations can occur and even the production of "exotic" particles in neutron star cores. High energy physics is crucial to understand what is happening in these dense environments. Young neutron stars cool primarily by emitting neutrinos as nuclear reactions occur in the neutron star core.

```{note}
The value of Fermi energy we got for neutron star envelope densities is much larger than the electron rest mass, so we should really use the relativistic formula $E_F=p_F c$ to calculate the Fermi energy. Try it! How does Fermi energy scale with density once the electrons become relativistic?
```

### Relativistic boosting, inverse Compton scattering

Relativity is key to making photons with even higher energies. For example, a photon scattering from a fast moving electron increases its energy by a factor $\sim \gamma^2$ (where $\gamma^2=1/(1-\beta^2)$; $\beta=v_e/c$) (inverse Compton or IC scattering). Consider a relativistic jet launched from an accreting black hole in which the Lorentz factor is $\gamma\sim 1000$. If we want to make X-ray photons with energy $\approx $keV, the seed photons need only have energies of $10^{-3}\ {\rm eV}$ which corresponds to $\lambda\approx 0.1\ {\rm cm}$ (far infrared). With seed photons in the optical (e.g. from the accretion disk), the energy is boosted from $\sim 1\ {\rm eV}$ to $\sim 1\ {\rm MeV}$ (gamma rays). IC scattering of a 10 keV X-ray photon would boost the photon energy to 10 GeV! 

Relativistic boosting of energies is key to making gamma-rays. The highest energy photon that has been detected has $E_\gamma>100\ {\rm TeV}=10^{14}\ {\rm eV}$ from the Crab nebula (Amenomori et al. 2019; Tibet air shower array). A possible source of these photons is scattering of CMB photons (3K; $3\times 10^{-4}\ {\rm eV}$) by PeV electrons (1 PeV$=10^{15}\ {\rm eV}$, $\gamma\sim 10^9$) accelerated at shock fronts in the nebula. Relativity also sets the photon energy in synchrotron radiation, which involves Lorentz boosted and beamed radiation from electrons spiralling in a magnetic field; the characteristic frequency is $\omega\sim \gamma^2 (eB/m_e c)$ as we'll see more of later. 

The key thing is then to understand particle acceleration -- what sets the distribution of particle energies as a function of $\gamma$? Non-thermal radiation like this from Compton scattering or synchrotron is an important source of high energy photons. It also leaves a signature at low photon energies. Synchrotron emission is a common source of radio emission. As we noted earlier, many radio sources have brightness temperatures much larger than the plasma temperature; thermal radiation is not an efficient radio source. We need high energy astrophysics to understand even low energy photons! 


## Summary

Hopefully this discussion motivates some of the topics that we'll cover in the course, specifically:

* How are particles accelerated in astrophysical environments and what does their energy spectrum look like?
* How do non-thermal particles radiate and how can we distinguish observationally between different radiation mechanisms such as inverse-Compton scattering or synchrotron?
* How do we make binary systems in which compact objects accrete from a companion star, and related is the question of how do we make compact object binaries that can merge and produce gravitational waves?

We'll start next week by looking in more detail at what different forms of EM radiation as well as neutrinos and GWs should look like. 

 
