# Binary evolution basics: solutions

## 1. Mean density of the secondary

(a) Assuming that the star is Roche-lobe filling, $R_2=R_L$ and then 

$$
\langle \rho_2\rangle = {M_2\over 4\pi R_2^3/3} = {3M_2\over 4\pi}{81\over 8}{M_\mathrm{tot}\over M_2a^3} = {243\over 32\pi} G^{-1} {GM_\mathrm{tot}\over a^3}={243\over 32\pi} G^{-1} \left({2\pi\over P_\mathrm{orb}}\right)^2={243\pi\over 8G}P_\mathrm{orb}^{-2}.
$$

Plugging in numbers gives

$$
\langle \rho_2\rangle  = 110\ {\rm g\ cm^{-3}}\ \left({P_\mathrm{orb}\over \mathrm{hr}}\right)^{-2}.
$$

(b) Assuming $M/M_\odot = R/R_\odot$, then $\langle \rho_2\rangle = \langle\rho_\odot\rangle (R/R_\odot)^{-2}=\langle\rho_\odot\rangle (M/M_\odot)^{-2}$, where the mean density of the Sun is $\langle\rho_\odot\rangle = 1.4\ {\rm g\ cm^{-3}}$. Therefore 

$$
{M\over M_\odot}\approx {R\over R_\odot}\approx 0.11 \ \left({P_\mathrm{orb}\over \mathrm{hr}}\right).
$$

The Sun will fill its Roche lobe at an orbital period of $\approx 9$ hours.

(c) For an orbital period of 5 minutes, we need $\langle\rho\rangle\approx 1.6\times 10^4\ {\rm g\ cm^{-3}}$. The companion is a low mass He or C/O white dwarf.

## 2. Conservative mass transfer with no angular momentum losses 

Since $J\propto M_1 M_2 a^{1/2}$ (with $M_{\rm tot}$ constant), then 

$$
{\dot J\over J} = {\dot M_1\over M_1} +  {\dot M_2\over M_2} + {1\over 2}{\dot a\over a}= {(-\dot M_2)\over M_1} -  {(-\dot M_2)\over M_2} + {1\over 2}{\dot a\over a}= {(-\dot M_2)\over M_2}\left({M_2\over M_1}-1\right)  + {1\over 2}{\dot a\over a}
$$

which gives the first equation. Then Paczynski's formula for $R_L$ gives $R_L\propto a M_2^{1/3}$ for $M_{\rm tot}$ constant, or

$$
{\dot R_L\over R_L} = {\dot a\over a} + -{1\over 3}{(-\dot M_2)\over M_2}.
$$

Using the first result for $\dot a/a$ to eliminate $\dot a/a$ from this equation gives the result we are looking for.
The formulae show that the orbit and Roche lobe can either shrink or expand on mass transfer depending on the value of $q$. If they shrink, that will tend to lead to an unstable mass transfer. For stable mass transfer, we want $R_L$ and $a$ to expand, so we need to transfer mass from a lighter star to a heavier star.


## 3. Accretion driven by angular momentum losses

(a) We are saying that the star/orbit always adjusts so that the star fills its Roche lobe, so then 

$$
{\dot R_L\over R_L}= {\dot R_2\over R_2} = n{\dot M_2\over M_2}.
$$

Now using Paczynski's formula, this is

$$
{\dot R_L\over R_L}= {\dot R_2\over R_2} = n{\dot M_2\over M_2} =  {\dot a\over a} + -{1\over 3}{(-\dot M_2)\over M_2}
$$

which gives the result that we are looking for.

The slope of the mass-radius relation $n=d\ln R_2/d\ln M_2$ depends on (1) the internal structure of the star (e.g. $n\approx 1$ for low mass main sequence stars but drops to $n\approx 0$ for brown dwarfs and is $\approx -1/3$ for degenerate white dwarfs) and (2) the rate at which mass loss happens because this determines whether the star is able to stay in thermal equilibrium or not. If the mass loss is very rapid, the star will respond adiabatically to the mass loss which gives $n\approx 1/3$.

A solar mass star initially filling its Roche lobe has $n\approx 1$ and so the orbit shrinks, but eventually the orbit "turns around" and starts moving to longer orbital periods because $n$ drops to the adiabatic value / degenerate value depending on the situation. To check whether the mass loss is adiabatic, you can compare the mass loss timescale $-\dot M/M$ to the Kelvin-Helmholtz (thermal) timescale $GM^2/RL$. 

(b) From question 2 we have 

$$
{\dot J\over J} =  {(-\dot M_2)\over M_2}\left(q-1\right)  + {1\over 2}{\dot a\over a}.
$$

Substituting the result from part (a) for $\dot a$ then gives

$$
-{\dot J\over J} =  {(-\dot M_2)\over M_2}\left(1-q\right)  + {1\over 2}{(-\dot M_2)\over M_2}\left(n-{1\over 3}\right)={(-\dot M_2)\over M_2}\left({5\over 6} +{n\over 2}-q\right)
$$ 

which is the result we're looking for that gives $\dot M_2$ in terms of $\dot J$.

Now we can put in the $\dot J$ from gravitational radiation:

$$
{(-\dot M_2)\over M_2} =  -{\dot J\over J}\left({5\over 6} +{n\over 2}-q\right)^{-1} = \left({5\over 6} +{n\over 2}-q\right)^{-1}{32\over 5}{G^3M_1M_2M_{\rm tot}\over c^5 a^4}
$$

$$
(-\dot M_2)=  \left({5\over 6} +{n\over 2}-q\right)^{-1}{32\over 5}{G^{5/3}M_1M_2^2\over M_{\rm tot}^{1/3} c^5}\left({P_\mathrm{orb}\over 2\pi}\right)^{-8/3}.
$$

We can write this in terms of the "chirp mass" (a quantity that comes up in gravitational radiation) 

$$
\mathcal{M} \equiv {(M_1M_2)^{3/5}\over M_{\rm tot}^{1/5}}
$$

as

$$
(-\dot M_2)=  \left({5\over 6} +{n\over 2}-q\right)^{-1}{32\over 5}
\left({G\mathcal{M}\over c^3}\right)^{5/3} M_2\left({P_\mathrm{orb}\over 2\pi}\right)^{-8/3}.
$$

Putting in some numbers assuming $q\ll 1$, $M_1\approx M_{\rm tot}=1\ M_\odot$ for simplicity gives 

$$
(-\dot M_2)=  8.1\times 10^{17}\ {\rm g\ s^{-1}}\ \left({5\over 6} +{n\over 2}\right)^{-1} \left({M_2\over M_\odot}\right)^2 \left({P_\mathrm{orb}\over \mathrm{hr}}\right)^{-8/3}.
$$

For a main sequence star $n=1$ we have the mass-orbital period relation from question 1 (b), $M_2\approx 0.11 M_\odot\, (P_\mathrm{orb}/\mathrm{hr})$, and so 

$$
(-\dot M_2)\approx 7.4\times 10^{15}\ {\rm g\ s^{-1}}\ \left({P_\mathrm{orb}\over \mathrm{hr}}\right)^{-2/3}.
$$

For a degenerate star $n=-1/3$, we can approximate $R_2\approx 10^9\ {\rm cm}\ (M/M_{\odot})^{-1/3}$, or $\langle\rho\rangle\approx 4.8\times 10^5\ {\rm g\ cm^{-3}}\ (M/M_\odot)^2$. The mean density-orbital period relation (question 1) then gives $M_2\approx 0.015\ M_\odot\ (P_\mathrm{orb}/\mathrm{hr})^{-1}$ and 

$$
(-\dot M_2) \approx 2.8\times 10^{14}\ {\rm g\ s^{-1}}\ \left({P_\mathrm{orb}\over \mathrm{hr}}\right)^{-14/3}.
$$


## 4. Common envelope

The change in the orbital separation is used to expel the envelope:

$$
\eta \left[{GM_cM_1\over 2a_f}-{GM_2M_1\over 2a_i}\right] = {GM_2M_\mathrm{env}\over \lambda R_2}
$$

$(M_2=M_c+M_\mathrm{env})$
For realistic values of $\lambda$, you can look at \href{https://ui.adsabs.harvard.edu/abs/2000A\ 26A...360.1043D/abstract}{Dewi et al.~2000}. Rearranging this gives

$$
{a_f\over a_i} = {M_c\over M_2} \left[1 + {2\over \eta\lambda}{a_i\over R_2}{M_\mathrm{env}\over M_1}   \right]^{-1}.
$$

As an example, we can think about the progenitor binary that deposits a solar mass star in an $\approx 9$ hour orbit around a white dwarf that we looked at earlier. Then we have $M_1=1\,M_\odot$ (the solar mass star), $M_c=0.6\,M_\odot$ (the core that becomes the white dwarf), and $M_2$ is the mass of the progenitor star that makes the white dwarf, we could take this to be $2\ M_\odot$ for example. Star 2 has evolved off the main sequence and is in either the RGB or AGB phase when it fills its Roche lobe. Using Paczynski's expression for the Roche lobe with $q=2$ gives $R_2/a_i\approx 0.4$. With $\lambda\approx 0.3$ as given in the question, I get

$$
{a_f\over a_i} = {0.3\over 1+23/\eta}.
$$

For a final orbital period of 9 hours, we have $a_f\approx 2.5\ R_\odot$. Therefore, when star 2 filled its Roche lobe, its radius was 

$$
R_2 \approx 3.3\ R_\odot\ (1+23/\eta).
$$

If the star was an RGB star with $R_2\lesssim 100\ R_\odot$, this implies an efficiency $\eta$ of order unity.

## 5. Time to contact

Using the expressions for the angular momentum loss rate from gravitational radiation and the orbital angular momentum $J = (M_1M_2/M_\mathrm{tot})\sqrt{GM_\mathrm{tot}a}$ gives

$$
{1\over 2}{\dot a\over a} = -{32\over 5}{G^3M_1M_2M_{\rm tot}\over c^5 a^4}
$$

$$
\int a^3 da = {a_f^4-a_i^4\over 4} = -{64\over 5}{G^3M_1M_2M_{\rm tot}\over c^5}t.
$$

Assuming $a_f\ll a_i$, the time to come into contact is therefore

$$t = {5\over 256}{c^5a_i^4\over G^3M_1M_2M_\mathrm{tot}}= {5\over 256}\left({c^3\over GM_\mathrm{tot}}\right)^{5/3}{M_\mathrm{tot}^2\over M_1M_2}\left({P_\mathrm{orb}\over 2\pi}\right)^{8/3}
$$

$$
t=3.1\ \mathrm{Myr}\ \left({P_\mathrm{orb}\over 1\,\mathrm{hr}}\right)^{8/3}{M_\mathrm{tot}^2\over M_1M_2}\left({M_\mathrm{tot}\over 2\,M_\odot}\right)^{-5/3}
$$

[Peters (1974)](https://journals.aps.org/pr/abstract/10.1103/PhysRev.136.B1224) derives expressions that include eccentricity.

For a binary neutron star system with two $1.4\ M_\odot$ neutron stars, setting $t=10\ {\rm Gyr}$ gives $P_\mathrm{orb}=25.6\ \mathrm{hours}$.  The [Hulse-Taylor binary](https://en.wikipedia.org/wiki/Hulse–Taylor_binary) (that gave the first evidence for orbital decay from gravitational radiation) has $P_\mathrm{orb}=7.5\ {\rm h}$ and will decay in $\approx 300$ Myr. For the second example, take a $1\,M_\odot$ star with a $0.6\,M_\odot$ white dwarf, and again set the time to be 10 Gyr: this gives $P_\mathrm{orb}=10.4\ {\rm h}$. If the common envelope leaves the binary with a smaller orbital period than this, then contact will be reached. In the MESA calculation we looked at, we started the binary with a period of 0.4 days. You could check the time the system evolved before accretion started.

## 6. Making a neutron star in a binary

(1) Immediately after the mass has been ejected, the total energy is

$$
-{GM_2(M_1-\Delta M)\over a_i} + {(M_1-\Delta M)M_2\over M_\mathrm{tot}-\Delta M}\cdot {1\over 2}\left({GM_\mathrm{tot}\over a_i}\right) = -{G(M_1-\Delta M)M_2\over 2a_f}.
$$

On the left hand side is potential plus kinetic energy, where we've used the fact that the relative velocity of the two stars is given by $v_\mathrm{rel}^2 = GM_\mathrm{tot}/a_i$, and on the right hand side is the orbital energy written in terms of the new semi-major axis $a_f$. The total mass $M_\mathrm{tot}$ is the total mass before the supernova ($=M_1+M_2$). This simplifies to 

$$
{a_f\over a_i} = {M_\mathrm{tot}-\Delta M\over M_\mathrm{tot}-2\Delta M},
$$

which shows that $a_f\rightarrow \infty$ when $\Delta M/M_\mathrm{tot}\rightarrow 1/2$.

(2) If we assume the ejected mass takes away its angular momentum, then the angular momentum per unit mass ($J/\mu=\sqrt{a(1-e^2)(M_1+M_2)}$ remains the same, giving 

$$
(1-e^2)a_f(M_\mathrm{tot}-\Delta M) = a_i M_\mathrm{tot},
$$

which simplifies to

$$
1-e^2 = {1-2\Delta M/M_\mathrm{tot}\over (1-\Delta M/M_\mathrm{tot})^2}.
$$

We see that ejecting half the mass also corresponds to $e\rightarrow 1$, further indicating that the orbit becomes unbound. (Physically what is happening here is related to the fact that a circular orbit has a specific ratio of energy to angular momentum -- the lowest energy orbit for a given angular momentum is a circular orbit. After the supernova, this ratio is changed and the orbit is eccentric).

(3) This part was worked out by \href{https://ui.adsabs.harvard.edu/abs/1983ApJ...267..322H/abstract}{Hills 1983}. If we write the relative velocity after the explosion explicitly in the kinetic energy term in the formula for the total energy from part (1),  we get (cancelling out factors of $GM_2(M_1-\Delta M)$)

$$
-{1\over a_i} + {1\over G(M_\mathrm{tot}-\Delta M)}\cdot {1\over 2}V_\mathrm{rel}^2 = -{1\over 2a_f}.
$$

Rearranging into a similar form as before but with a correction term, we get

$$
{a_f\over a_i} = {M_\mathrm{tot}-\Delta M\over M_\mathrm{tot}-2\Delta M-a_i \Delta V^2/G},
$$

where 

$$
\Delta V^2 = V^2_\mathrm{rel} - {GM_\mathrm{tot}\over a_i}.
$$

We see that if the kick is in a direction against the motion, so that $\Delta V^2<0$, then we can keep the binary bound even when more than half the mass is ejected. If the kick is aligned with the motion, $\Delta V^2>0$, then it actually helps to unbind the binary. See Hills' paper for more details.
