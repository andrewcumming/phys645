# Black hole accretion

## 1. Efficient accretion onto a black hole

Do some research into the energy of particle orbits around non-rotating and rotating black holes, in particular the innermost stable orbit (ISCO). How do the expressions for orbital energy compare to the Newtonian case? Can you confirm the values I gave in class $\eta=0.057$ for a Schwarzschild black hole and $\eta=0.42$ for a maximally-rotating Kerr black hole?

## 2. The accretion rate onto Sgr A$^\star$

Do some research into the black hole at the Galactic centre Sgr A$^\star$. What we know about the environment around Sgr A$^\star$ and the accretion rate onto the black hole and the accretion efficiency?

## 3. Radiation efficiency of a spherical flow 

Consider a spherical accretion flow onto a black hole of mass $M$ from surrounding gas which has density $\rho_\infty,$ temperature  $T_\infty$, and sound speed $c_\infty$. Gas flows from the Bondi radius ("capture radius") $r_\mathrm{accr}=GM/2c_\infty^2$ to the Schwarzschild radius $R_s\ll r_\mathrm{accr}$ at a rate given by the Bondi rate $\dot M = \pi (GM)^2 \rho_\infty/c_\infty^3$.

Assume that (1) the flow is optically thin and (2) that cooling is negligible so that the flow is adiabatic. Derive an expression for the total Bremsstrahlung luminosity from the accretion flow and use it to calculate the accretion efficiency $\eta$. You should find that $\eta$ depends only on the accretion timescale $M/\dot M$. Using $M=2.4\times 10^6\ M_\odot$ and $\dot M=10^{-5}\ M_\odot\ \mathrm{yr^{-1}}$ for Sgr A$^\star$, what do you find for $\eta$?

## 4. Two temperature plasma

A black hole accretes from surrounding gas with density $\rho_\infty$ and sound speed $c_\infty$ at a rate given by the Bondi rate $\dot M = \pi (GM)^2 \rho_\infty/c_\infty^3$. Assume the flow is adiabatic ($T\propto \rho^{2/3}$). Investigate whether Coulomb collisions can effectively couple electrons and protons in the flow.

The following results will be useful:
* The collision rate between electrons and protons is $n\sigma v_e=1/t_\mathrm{coll}$, where $n$ is the proton density, $v_e$ is the electron velocity, and $\sigma$ is the Coulomb cross-section, roughly given by  $$\sigma\approx {e^4\over (k_BT)^2}$$ (there is a Coulomb logarithm which I've set to 1 here). 
* The timescale to transfer energy from protons to electrons is 

$$
t_E\approx \left({m_p\over m_e}\right)t_\mathrm{coll}
$$ 

(can you see why this is true?)
* To assess whether electrons and protons couple to each other, you can compare the timescale $t_E$ with the free-fall timescale $t_{ff} = r^{3/2}/(GM)^{1/2}$. 

## 5. Photon trapping

Consider a spherical accretion flow onto a black hole of mass $M$ from surrounding gas which has density $\rho_\infty$ and sound speed $c_\infty$. If the flow is steady, mass conservation gives $\dot M = 4\pi r^2\rho(r) v(r)=\,$constant, and you can assume that the velocity is given by the free-fall velocity $v(r)=(2GM/r)^{1/2}$. The accretion rate is given by the Bondi rate $\dot M = \pi (GM)^2 \rho_\infty/c_\infty^3$ which we saw in class last time.

(a) Derive an expression for the optical depth $\tau = \int n\sigma dr$ from the Bondi radius ("capture radius") $r_\mathrm{accr}=GM/2c_\infty^2$ to an inner radius $r\ll r_\mathrm{accr}$ close to the black hole. You should be able to write your answer in terms of the accretion efficiency $\eta$, the ratio of the accretion luminosity $L_\mathrm{accr}=\eta \dot M c^2$ to the Eddington luminosity $L_{\rm Edd}$, and the ratio $R_s/r$, where $R_s$ is the Schwarzschild radius. You can assume the opacity is from electron scattering (Thomson cross-section) ($\sigma=\sigma_T$).

(b) You should have found in (a) that the inner parts of the flow are optically thick for large enough $L_\mathrm{accr}$. In this case, photons random walk. What is the outwards velocity $dr/dt$ of a random-walking photon? (You should find a simple answer in terms of the speed of light and the optical depth). Show that there is a radius $r_t$ (the "trapping radius") within which this outwards velocity is smaller than the inwards flow speed. You should find that $r_t$ can be written in terms of $\eta$, $R_s$ and $L_\mathrm{accr}/L_\mathrm{Edd}$. 