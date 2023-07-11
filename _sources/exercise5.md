# Binary evolution with MESA

In this exercise, you will analyze some results for a main sequence star that accretes mass onto a white dwarf in a binary.

We saw in the notes and questions that an important quantity that determines the outcome of accretion in binaries is the response of the star to mass loss, in particular, how the stellar radius changes as the star loses mass, 

$$
n = {d\ln R_2\over d\ln M_2}.
$$ 

The MESA stellar evolution code can calculate the evolution of a star in a binary undergoing mass loss. In this case, I started with a solar mass star in orbit with a $0.6\ M_\odot$ white dwarf, with an initial orbital period of $0.4$ days. The code follows the detailed structure of the secondary star as the orbit evolves and it loses mass (the white dwarf is treated as a point mass). 

You can find the results of the calculation here: 
https://www.hep.physics.mcgill.ca/~cumming/teaching/645/mesa_binary_results/

There are two files, ``history.data`` which has information about the star as a function of time, and ``binary_history.data`` which has information about the binary as a function of time. The files have a few lines of header information and then the data is organized into columns. One way to read in  the data is to use [``numpy.loadtxt``](https://numpy.org/doc/stable/reference/generated/numpy.loadtxt.html) using the ``skiprows`` parameter to skip the header lines and then you can specify the columns you want with ``usecols`` (or just read in the whole thing). The names of the columns are given but if you need help figuring out which column is which or the units being used, let me know.

Take a look at these files and investigate how the secondary mass $M_2$ (and mass ratio $q$), accretion rate $\dot M$, orbital period $P_{\rm orb}$ change over time. Calculate $n$ and the timescales $M/\dot{M}$ and $GM^2/RL$ for the star. 
Does the evolution of the system over time make sense given our results from the notes? For example, is the accretion rate what you expect from gravitational radiation? Does the star lose mass throughout the entire evolution? Does the orbital period increase or decrease and is that consistent with the value of $n$ that you find?
