# Compact object interiors

## Neutron star outer layers

Although the core of a neutron star is made of free neutrons and protons ("one big nucleus"), the outer parts of the star are a fully-ionized plasma with nuclei and degenerate electrons. In this question, we'll look at the composition as we go from the surface deeper into the star.

The binding energy of a nucleus with $Z$ protons and $N$ neutrons (total number of nucleons $A=Z+N$) is approximately given by the [semi-empirical mass formula](https://en.wikipedia.org/wiki/Semi-empirical_mass_formula)

$$
{E_B(A,Z)\over c^2} = Zm_p + Nm_n - M(A,Z) = a_VA - a_S A^{2/3} - a_C {Z^2\over A^{1/3}} -a_A{(A-2Z)^2\over A}.
$$

Here $M(A,Z)$ is the mass of the nucleus with mass $A$ and charge $Z$. This is a physically-motivated empirical formula that is fit to nuclear data to determine the best fit constants $a_V\approx 15.8\ {\rm MeV}$, $a_S\approx 17.8\ {\rm MeV}$, $a_C\approx 0.711\ {\rm MeV}$, and $a_A\approx 23.7\ {\rm MeV}$. The proton and neutron masses are $m_p \approx  938.272\ {\rm MeV}$ and $m_n \approx 939.565\ {\rm MeV}$.  

(a) The four terms on the right hand side are the volume, surface, Coulomb, and asymmetry terms. Can you tell from the scalings with $Z$ and $A$ and the signs of the different terms why they have these names?

```{note}
A pairing term is also often added to the semi-empirical mass formula to account for the increased binding energy of nuclei with even numbers of neutrons or protons. We ignore that here for simplicity and to make the behaviour with $A$ and $Z$ continuous.
```

(b) Plot a color map of the binding energy per nucleon ($E_B/A$) as a function of $N$ on the $x$-axis and $Z$ on the $y$-axis. You should see the "stability valley", the nuclei that have the largest binding energies for each element ($Z$). How does $N$ scale with $Z$ for these most stable nuclei? Does it look as you expect? Do you recognize some of the nuclei in the stability valley? It might be helpful to add the curve showing the $N$ that maximizes the binding energy as a function of $Z$.

(c) Now consider the neutron separation energy $S_n$ which is the energy it takes to remove a neutron from a nucleus

$$
{S_n(A,Z)\over c^2} =   m_n + M(A-1,Z) - M(A,Z) = E_B(A,Z) - E_B(A-1,Z).
$$

If $S_n<0$, the nucleus will spontaneously spit out a neutron, it is neutron unbound. Plot a color map of $S_n$ and identify the **neutron drip line**, the boundary between nuclei that are neutron bound and unbound. 

(d) In a neutron star, the electrons are degenerate with energy $E_F$, so the energy we need to consider for a given nucleus is actually 

$$
Z E_F + M(A,Z).
$$

The Fermi energy for relativistic electrons is 

$$
E_F = \hbar c k_F = \hbar c (3\pi^2 n_e)^{1/3} = \hbar c \left({3\pi^2\over m_p}\right)^{1/3}Y_e^{1/3}\rho^{1/3} \approx 5.1\ {\rm MeV}\ \rho_9^{1/3}Y_e^{1/3},
$$

where $Y_e=n_em_p/\rho = Z/A$ for a single species of nucleus.

Because electrons have a large Fermi energy, they can capture onto nuclei changing the $Z$. Therefore, the $Z$ can adjust (at fixed $A$) to lower the energy.

For example, consider a nucleus with $A=56$. Find the $Z$ that minimizes the energy for that nucleus as a function of density (you can try a range of densities from $\rho = 10^8$--$10^{12}\ {\rm g\ cm^{-3}}$). Do you get the answer you expect at low density? What happens at higher densities? Check to see whether these nuclei are neutron-unbound. You should find that there is a density where neutrons start to spontaneously be released from the nuclei -- **neutron drip**. 

(e) How deep into the star is neutron drip? You can estimate this using the pressure scale height $P/\rho g$ at that depth. 



## Solid plasma?

Consider a fully-ionized plasma consisting of degenerate electrons and nuclei (ions) with charge $Z$ and mass $A$. The degenerate electrons in white dwarfs and neutron stars have such large Fermi energies that they don't really feel the electrostatic forces from the ions and so we can assume that they form a smooth background of negative charge (with $n_e$ electrons per unit volume).

The ratio of Coulomb to thermal energy for the ions is 

$$
\Gamma = {Z^2 e^2\over a k_BT},
$$ 

where $a$ is the mean separation between ions given by $(4\pi/3) n_i a^3 =1$ and $n_i = \rho/Am_p$ is the ion density. At temperatures that are low enough that $\Gamma$ becomes large, the thermal energy is negligible and then the Coulomb repulsion between ions makes the ions fall into a lattice -- the plasma forms a solid. At higher temperatures, thermal motions of the ions become significant, $\Gamma$ drops, and the ions are able to move around, becoming liquid for $\Gamma<\Gamma_{\rm melt}$ and finally gas for $\Gamma<1$. 

(a) Imagine perturbing one of the ions from its equilibrium position in the lattice by an amount $\delta r\ll a$. Estimate the restoring force it will feel from the Coulomb repulsion of its nearest neighbours, and therefore the spring constant. Next, assuming thermal equilibrium so that degrees of freedom get $(1/2)k_BT$ of energy, estimate the mean-square displacement of the ion about its equilibrium position as a function of temperature.

(b) **Lindemann's criterion** is an [empirical rule](https://en.wikipedia.org/wiki/Melting_point#Predicting_the_melting_point_of_substances_(Lindemann's_criterion)) for when a solid melts which is that the solid will melt when $\langle (\delta r)^2\rangle\sim c^2a^2$ with $c\approx 0.15$--$0.3$. Use this to estimate the value of $\Gamma_m$. Molecular dynamics simulations of these kinds of plasmas give $\Gamma_m\approx 175$. How does your answer compare? 

(c) Using the more accurate value for $\Gamma_m\approx 175$, calculate the melting temperature as a function of density, $Z$, and $A$. Make a plot showing the melting curve in the $\rho$--$T$ plane for different nuclei $(Z,A)$. Apply your formula to white dwarfs and neutron star envelopes. Do we expect to find solid plasmas in nature? Are white dwarfs gas, liquid, or solid inside?

## White dwarf cooling

The degenerate electrons inside white dwarfs are excellent conductors of heat, so white dwarfs are expected to be isothermal except for the outermost lower density layers. This means that the thermal content of the white dwarf is approximately $E = M c_V T_c$ where $M$ is the mass of the star, $c_V\approx 3k_B$ per nucleus is the specific heat, and $T_c$ is the internal temperature (core temperature).

The rate at which the white dwarf cools is set by the surface luminosity 

$$
L = 4\pi R^2 \sigma T_s^4,\hspace{2cm} (*)
$$

where $T_s$ is the surface temperature. If we knew how the surface temperature depended on the core temperature $T_s(T_c)$, we could then calculate the cooling rate 

$$
M c_V{dT_c\over dt} = -L = -4\pi R^2\sigma \left[T_s(T_c)\right]^4.
$$

There is a famous argument by Mestel that gives an estimate for $T_s(T_c)$ and allows us to predict the temperature history of white dwarfs. 

(a) To find the relation between surface and core temperatures, we need the temperature gradient in the thin low density outer layers (these layers are sometimes discussed as being a "blanket" over the core and controlling how quickly it can cool down). The thermal diffusion equation is

$$
L = -4\pi R^2 {4acT^3\over 3\kappa\rho}{dT\over dr},
$$

where $\kappa$ is the radiative opacity. Replace $L$ with $T_s$ using equation (*), assuming an opacity of the form $\kappa=\kappa_0 \rho T^{-7/2}$, ideal gas $P=\rho k_BT/\mu m_p$, and using hydrostatic balance $dP/dr=-\rho g$ to change variables from $r$ to $P$ (in this thin surface layer $g=GM/R^2$ is a constant), integrate this equation and show that $T_s$ and $T_c$ are related by

$$
T_s^4\approx {64\over 51} {gk_B\over \kappa_0\mu m_p}{T_c^{17/2}\over P_b^2} ,
$$

where $P_b$ is the pressure at the base of the layer.

(b) The key insight of Mestel is that the base pressure $P_b$ where the temperature becomes isothermal corresponds to the transition from ideal gas to degeneracy pressure. Show first that for non-relativistic degenerate electrons, $P_e\propto E_F^{5/2}$ with a proportionality constant that you can derive. Now set $E_F=k_BT_c$ at $P_e=P_b$ gives $P_b\propto T_c^{5/2}$, again with a proportionality constant that you can derive.

(c) Use the results of parts (a) and (b) to derive an equation for the cooling luminosity as a function of the white dwarf mass $M$ and the core temperature $T_c$. Put numbers into your answer.

(d) Use your answers so far to derive an expression for $T_c$ as a function of time for white dwarfs. Put numbers into your answer. How should $T_s$ or $L$ depend on time for white dwarfs of different masses?



