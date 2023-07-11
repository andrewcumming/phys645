# Black hole imaging

You have probably seen the amazing images of the black holes in M87 and Sgr A$^\star$ from the [Event Horizon Telescope](https://eventhorizontelescope.org). The idea in this exercise is to investigate photon trajectories near black holes to understand the role of light bending in these images. Light bending is also important for neutron stars because it sets their apparent size and limits the modulation amplitude that can be achieved from a hot spot on the surface of a rotating neutron star. 

[Luminet et al. 1979](https://ui.adsabs.harvard.edu/abs/1979A\%26A....75..228L/abstract) first calculated what the image of a black hole would look like, assuming a non-rotating (Schwarzschild) black hole surrounded by a thin accretion disk. This kind of image --- with much more detail and for a rotating black hole --- appeared famously in the movie [Interstellar](https://www.wired.com/2014/10/astrophysics-interstellar-black-hole/) (see [Oliver et al. 2015](https://iopscience.iop.org/article/10.1088/0264-9381/32/6/065001)).

The trajectory of a photon near a Schwarzschild black hole is given by

$$
{d\phi\over dr} = \pm {1\over r^2} \left[{1\over b^2} - {1\over r^2}\left(1-{2GM\over rc^2}\right)\right]^{-1/2} \hspace{2cm} (*)
$$

(e.g. equation 2 of [Luminet 1979](https://ui.adsabs.harvard.edu/abs/1979A\%26A....75..228L/abstract)). The trajectory is written in terms of the radial $r$ and azimuthal $\phi$ coordinates (because of the spherical symmetry, the photon orbit is confined to a plane, so we can always choose this to be the equatorial plane $\theta=\pi/2$). The constant $b$ is the impact parameter, the ratio $L/E$ of angular momentum to energy of the orbit. In the Newtonian case where photons travel in straight lines, the impact parameter is the distance of closest approach. For the general case including black hole rotation, you can look at [Bardeen, Press \& Teukolsky 1972](https://ui.adsabs.harvard.edu/abs/1972ApJ...178..347B/abstract) (see their equations 2.9a--d).

## Part 1: Photon deflection

Use equation (*) to calculate the trajectories of photons travelling from a large distance towards a black hole with different impact parameters $b$. In Newtonian physics, the photons would travel in a straight line, but in general relativity you should find that they are deflected by the black hole. Make a plot that shows the paths of photons with different impact parameters. 

Some hints:

* It makes it easier to use units of Schwarzschild radius $r_S=2GM/c^2$ for length and then the GR term in equation (*) is just $1-1/r$. 
* The distance of closest approach $r_c$ (periastron) of the orbit is the value of $r$ that makes the square bracket in equation (*) vanish. So before you integrate the orbit, you can solve for $r_c$. (Find the root numerically, e.g. you can use ``scipy.optimize.brentq``.
* You will need to choose a plus or minus sign on the right hand side of equation (\ref{eq:drdphi}) for different parts of the orbit. One approach is to integrate $d\phi/dr$ from large $r$ down to $r_c$ with one sign for the inwards part of the trajectory, and then integrate out again from $r_c$ to large $r$ with the opposite sign for the outwards part. 
* You can plot the resulting $r(\phi)$ using a polar plot (e.g. ``plt.subplots(subplot_kw={'projection': 'polar'})`` in ``matplotlib``). 
* For large impact parameters, you should see the analytic result that the deflection angle is $2r_s/b$. As you reduce the impact parameter, you should find a value of impact parameter where the photon is deflected back in the direction it came from (see Figure 2 of [Luminet 1979](https://ui.adsabs.harvard.edu/abs/1979A\%26A....75..228L/abstract)). For (slightly) smaller values $b$ the photons have even larger deflection angles and begin to loop around the black hole.

## Part 2: Imaging black holes and neutron stars

(a) Now consider observing a thin disk around a black hole from an angle $\theta_d$ above the disk plane ($\theta_d=\pi/2$ corresponds to the disk being face on; $\theta_d=0$ edge on). Figure 6 of [Luminet 1979](https://ui.adsabs.harvard.edu/abs/1979A\%26A....75..228L/abstract) shows what the disk would look like in terms of contours of constant radial distance from the black hole. Use your calculation to check these figures along the vertical and horizontal axes (i.e. do you agree with the vertical and horizontal offsets of these curves?). 

```{note}
An extension of this question would be to figure out the angles and make your own version of Figure 6, but it's complicated, so for simplicity here we can restrict ourselves to looking at the vertical and horizontal parts only.
```

(b) Use your calculation to calculate the apparent size of a neutron star with radius $r=R$ (the neutron star looks larger to a distant observer because light from the back side of the neutron star bends around and can reach the observer). Check that your answer is consistent with $L=4\pi R^2\sigma T^4$ given that the temperature redshifts by one power of $1+z$ and luminosity by two powers of $1+z$, where $1+z = (1-2GM/Rc^2)^{-1/2}$. 

```{note}
An extension of this problem would be to consider a ``hot spot'' on the surface of a neutron star and calculate the observed flux as the neutron star rotates and the hot spot travels into and out of the line of sight. Light bending means that you can see some of the hot spot even when it is on the back side of the star relative to the line of sight, reducing the luminosity amplitude variation that can be achieved.
```
