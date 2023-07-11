
# Time-dependent thin disk

In this exercise, you will make a model of a time-dependent thin disk.

Consider a thin accretion disk around a star of mass $M$. If the surface density of the gas at radius $r$ is $\Sigma$ and the mid-plane temperature is $T$, we can calculate the sound speed, disk thickness and mean density as 

$$
c_s\approx \left({k_BT\over m_p}\right)^{1/2}\hspace{1cm}H = {c_s\over\Omega}\hspace{1cm}\rho\approx {\Sigma\over H}.
$$

Let's build a simple time-dependent model of an annulus in the disk at radius $r$. If the accretion rate coming into the annulus from large $r$ is $\dot M$ (e.g. set by the rate at which gas is flowing from a companion star into the accretion disk), the time evolution of $\Sigma$ can be written as

$$
{d\Sigma\over dt} = {1\over 2\pi r H}\left(\dot M - 3\pi \alpha c_s H \Sigma\right)\hspace{2cm}(*)
$$

where we've used the expression for the local accretion rate in the thin disk $3\pi \nu \Sigma = 3\pi \alpha c_s H \Sigma$. For simplicity, we've assumed that the radial extent of the annulus is $H$ (the same as the disk thickness) giving an area $2\pi r H$ in the denominator.

To calculate the evolution of temperature, we need the heating and cooling rates. The viscous heating rate is approximately $Q_+=\nu\Omega^2\Sigma$ per unit area. The cooling rate is $Q_-=\sigma_{SB}T_{\rm eff}^4$, where the effective temperature (surface temperature) of the disk is related to the central temperature by $T_\mathrm{eff}^4\approx T^4/\tau$ (assuming the disk is optically thick). The optical depth is $\tau\approx \kappa(\rho,T)\Sigma$. With specific heat capacity $C_V\approx k_B/m_P$, the temperature evolution is then given by 

$$
{dT\over dt} = {Q_+-Q_-\over \Sigma C_V}.\hspace{2cm}(\dagger)
$$

**Write a code to integrate equations (*) and ($\dagger$) in time.** To integrate you can use for example ``solve_ivp`` from ``scipy``. For the opacity, you can take free-free opacity $\kappa=6.6\times 10^{22}\ {\rm cm^2\ g^{-1}}\ \rho T^{-7/2}$ for $T>10^4\ \mathrm{K}$ when the hydrogen is ionized. For $T<10^4\ \mathrm{K}$, H$^-$ opacity is important given by approximately $\kappa\approx 2.5\times 10^{-31}\ {\rm cm^2\ g^{-1}}\ \rho^{1/2}T^9$. To model the transition to dust opacity at low temperatures, you can enforce a minimum value of opacity for $T<10^4\ {\rm K}$ (something like $0.1\ \mathrm{cm^2\ g^{-1}}$ is a good value). 

A good starting value for $r$ is $10^{11}\ {\rm cm}$, and it is usually assumed that the viscosity coefficient $\alpha$ has different values depending on temperature: at $T>10^4\ {\rm K}$, you could take $\alpha_\mathrm{hot}=0.3$ and for $T<10^4\ {\rm K}$, $\alpha_\mathrm{cold}=0.01$.

**Try different values for $\dot M$ and see what happens!** Good plots to make are $\Sigma$ and $T$ as a function of time, $\Sigma$ vs $T$ (a *phase space* plot), and $\dot M=3\pi\alpha c_sH$ as a function of time. How does the evolution change with $\dot M$? Do the starting values of $\Sigma$ and $T$ change the evolution?
