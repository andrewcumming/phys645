# Questions on accretion: solutions


1. The black hole mass increases exponentially on the Salpeter timescale 

$$
t_S = {\kappa \epsilon c\over 4\pi G} = 45\ {\rm Myrs}\ \left({\kappa\over 0.4\ {\rm cm^2\ g^{-1}}}\right)\left({\epsilon\over 0.1}\right),
$$

where $\epsilon$ is the accretion efficiency.

2. The disk spectrum is $\propto \nu^2$ at low frequencies (Rayleigh Jeans from the outermost part of the disk), $\nu^{1/3}$ at intermediate frequencies (the sum of blackbodies across the disk), and $\propto \nu^{3}e^{-h\nu/kT}$ at high frequencies (the Wien tail of the inner disk). 

To derive the $\nu^{1/3}$, start with 

$$
F_\nu\propto \int_{r_i}^{r_o} 2\pi r \, dr\ B_\nu(T(r)),
$$

where $r_i$ is the radius of the inner edge of the disk and $r_o$ the outer edge. Change variables to $T$ using $T\propto r^{-3/4}\Rightarrow dr/dr = -(4/3)(dT/T)$, giving

$$
F_\nu\propto \int_{T_o}^{T_i} T^{-8/3} \, {dT\over T}\ B_\nu(T)\propto \int_{T_o}^{T_i} T^{-8/3} \, {dT\over T}\ \nu^3 {1\over e^{h\nu/kT}-1}
$$
 
Finally change variables to $x=h\nu/k_BT$ using $dx=-(h\nu/k_BT)(dT/T)$:

$$
F_\nu\propto \int_{x_i}^{x_o} x^{8/3}\nu^{-8/3} \, {dx\over x}\ \nu^3 {1\over e^x-1}.
$$

If we assume that the lower and upper limits of the integral can be taken to $0$ and $\infty$ respectively (so that the disk spans a large range of radii/temperatures), the integral is a constant that can be evaluated, and we are left with $F_\nu\propto \nu^{1/3}$.

3. This definition of thermal timescale comes from dividing the internal energy of the gas with the sum of the blackbody flux from the top and bottom of the disk. Simplifying we get

$$
t_\mathrm{therm}={\Sigma c_PT\over 2\sigma T_\mathrm{eff}^4} \approx  {\Sigma\over 2\sigma T_{\rm eff}^4}{k_BT\over m_p}\approx{\Sigma c_s^2\over 2\sigma T_{\rm eff}^4}\approx {4\pi \Sigma c_s^2\over \Omega^2 \dot M}\approx {H^2\over \nu}\approx \left({H\over r}\right)^2 t_{\rm visc}\approx {1\over \alpha\Omega},
$$

where $t_{\rm visc} = r^2/\nu$ and we drop factors of order unity. The thermal time is much shorter than the viscous time for a thin disk, which is consistent with the disk being thin since the gas can radiate energy and settle into lowest energy circular orbits.

4. You should find

$$
P_{\rm orb} = 2\pi \left({B_\star^2R_\star^6\over 2\dot{M}(GM)^{5/3}}\right)^{3/7}
$$

$$
= 1\,{\rm s}\ \left({B_\star\over 10^{12}\ {\rm G}}\right)^{6/7}\left({R_\star\over 10\ {\rm km}}\right)^{18/7}\left({\dot M\over 10^{18}\ {\rm g\ s^{-1}}}\right)^{-3/7}\left({M\over M_\odot}\right)^{-5/7}
$$
