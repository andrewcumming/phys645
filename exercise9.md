# Power law energy distributions

We discussed earlier in the course that both particles and photons often have power law energy distributions, $N(E)dE\propto E^{-\alpha}dE$. For example, the slope of a synchrotron spectrum can be used to infer the slope of the particle energy distribution. In this exercise, you will investigate the origin of these power laws. 

## Fermi acceleration at a shock

One way to accelerate particles is by repeatedly scattering them across a shock front. The idea is to use the jump in the gas velocity, which changes discontinuously across the shock front, to give energy to the particle. The particle crosses the shock front and scatters, gaining energy as it comes into co-motion with the fluid on the other side of the shock. Later, it crosses back to the other side and a similar process happens. Eventually, the particle moves away from the shock front -- "escapes" -- with its final energy.

## Question 1: Monte-Carlo simulation

Write a code that simulates this process using a Monte Carlo method. For $N$ particles, first choose their energies from a Maxwell-Boltzmann distribution, then have each particle undergo scattering events where the particle energy changes by a constant fractional amount $\Delta E/E$. The number of scattering events for any given particle is determined by when the particle escapes: the probability of escaping is $P_\mathrm{esc}$ at each scattering event. 

Calculate the resulting spectrum of particle energies. You should see a power law. Measure the power law index and determine how it depends on $\Delta E/E$ and $P_\mathrm{esc}$. 

Some hints:
* It's simpler to write the Maxwell-Boltzmann distribution in terms of $x=E/k_BT = mv^2/2k_BT$, which gives $f(x)\,dx = (2/\sqrt{\pi})x^{1/2}e^{-x}\,dx$. (Assume non-relativistic particles for simplicity here).
* Wherever you can avoid using for loops and write your code to use vector operations in numpy (ie. operate on all particle energies at the same time). Some useful functions are ``numpy.random.rand()`` and ``numpy.random.geometric``. You can plot a histogram of the energies using 
``plt.hist(E, density=True, bins=100, histtype = 'step')``

* One way to select samples from a distribution $f(x)$ is the *rejection method*, where you select uniform random numbers $x$ and $y$, and keep only the values of $x$ that have $y < f(x)$. The $x$-values selected in this way will have a distribution $f(x)$. 

## The magnitude of $\Delta E/E$ and $P_\mathrm{esc}$

If the shock front is moving at a speed $u_s$, there is a classic result in astrophysical fluids that in the frame moving with the shock, gas flows into the shock with speed $u_s$ and out of the shock with speed $u_s/4$. (This makes two assumptions, that $u_s\gg c_s$ so we are dealing with a *strong shock*, and that the gas is monatomic, so that $\gamma=5/3$). This means a particle always sees oncoming gas moving at $(3/4)u_s$ when it crosses the shock front, no matter which direction it moves across. This gives the same value of $\Delta E/E\approx u_s/c$ each time the particle moves across the shock (you don't need to do this, but the way this is derived is to move into the frame of the oncoming gas and use a Lorentz transformation to calculate the particle energy once it has scattered a few times and so has zero-net momentum relative to its new surroundings). Also, the probability of escape is related to how fast the particle moves relative to the shock, since this determines whether the particle can be swept away from the shock by the gas. The result is $P_\mathrm{esc}\approx u_s/c$. 

## Question 2: expected power law index

Given these results, what do you expect for the slope of the energy distribution coming from Fermi acceleration? What is your prediction for the slope of the synchrotron spectrum and how does it compare to typical values $\alpha\approx 0.7$ ($F_\nu\propto \nu^{-\alpha}$)?
