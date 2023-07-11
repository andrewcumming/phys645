# Lightcurve of a transient

In this exercise, you will work through a simple model of the lightcurve of a transient event that was developed for Type Ia supernovae ([Arnett 1979](https://ui.adsabs.harvard.edu/abs/1979ApJ...230L..37A/abstract)) but later used to model the expected lightcurve from neutron star mergers ([Li \& Paczynski 1998](https://ui.adsabs.harvard.edu/abs/1998ApJ...507L..59L/abstract), see also [Metzger 2019](https://ui.adsabs.harvard.edu/abs/2019LRR....23....1M/abstract)).
The idea is to consider the evolution of the mass ejected from a supernova or neutron star merger and to calculate an approximate model for the temperature and luminosity of the ejecta.

* First read section 2 of Li \& Paczynski which describes the model. Use their equations (6) and (9) to derive an equation for $dL/dt$ and compare with equation (5) of Arnett (1979).
* Implement the model numerically by integrating the equation for $dL/dt$ or $dU/dt$ in time. Calculate the lightcurve $L(t)$ and explore how it depends on the ejecta mass $M$, expansion velocity $V$, opacity $\kappa$, and radioactive heating.
* Use your model to investigate what parameters are needed to match the typical lightcurves of Type Ia supernovae and kilonovae. What are the main differences between these two kinds of transient events?
* Can you identify the different phases of the lightcurve? When is the expansion adiabatic and when do radiative cooling and radioactive heating become important for the two cases?
* Calculate the optical depth of the ejecta $\tau$ as a function of time. When does the ejecta become optically thin? Metzger (2019) equation (6) gives the time of the peak luminosity as $t=R\tau/c$, the photon diffusion timescale. Does this agree with your models? Metzger (2019) also gives "Arnett's law" that the peak luminosity is equal to the total radioactive heating rate at the time of the peak. Do you agree?
