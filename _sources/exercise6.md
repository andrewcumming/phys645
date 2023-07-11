# Making gravitational wave sources

Many examples of black hole mergers have now been seen in gravitational waves by LIGO (and to a lesser extent black hole-neutron star and neutron star-neutron star mergers) --- e.g. see the famous plot of the "[stellar graveyard](https://www.ligo.caltech.edu/image/ligo20211107a)".  For a merger to happen, the two compact objects must be brought into a close enough orbit that gravitational radiation can take over and drive them together on a timescale less than a Hubble time. It is not obvious how to do this since we need to put the compact objects into an orbit that is physically smaller than their progenitor stars! We saw in the questions this week how a common envelope phase can help to do this. We also have the problem that neutron stars and black holes are born in supernovae that eject most of the mass of the progenitor star, potentially disrupting the binary. 

The idea in this exercise is to use the binary evolution code [COSMIC](https://cosmic-popsynth.github.io) to investigate how these sources are made.

First install the code following these [instructions](https://cosmic-popsynth.github.io/docs/stable/install/).

Once you have the code installed, work through [this page](https://cosmic-popsynth.github.io/docs/stable/examples/index.html) that gives examples of how to make GW150914-like and GW170817-like binaries. GW150914 was the first merging black hole seen by LIGO and GW170817 the neutron-star merger that was associated with a kilonova (more on that later in the course!). 

Choose either the binary black hole or neutron star system. Use the results from the code to draw a diagram that illustrates and explains the different stages that lead from the initial binary to the final merger of the two compact objects.

**Comments:**
* If you are running in a notebook, you can use 
``import pandas as pd`` and 
``pd.set_option('display.max_columns', 500)``
so that all the columns of the output data frames are shown when you print them (by default some of them are not shown if there are a lot of columns).
* What are the differences between the two systems that cause one to make binary BHs and the other NSs? Compare your results with someone else in the class and see if you can see the differences.
* If you are interested in reading more about the physics prescriptions in the code you can look at [Breivik et al. 2020](https://ui.adsabs.harvard.edu/abs/2020ApJ...898...71B/abstract) which describes the code, and the two papers [Hurley et al. 2000](https://ui.adsabs.harvard.edu/abs/2000MNRAS.315..543H/abstract) and [Hurley et al. 2002](https://ui.adsabs.harvard.edu/abs/2002MNRAS.329..897H/abstract) that lay out the analytic formulae for approximating the different stages of stellar and binary evolution.
* You might notice that in both cases, the binary is left with an orbit too wide to merge on Gyr timescales. The black hole masses are also smaller than inferred for GW150914 (29 and 36$M_\odot$) in the black hole example. One challenge is to try to make adjustments to the parameters to find a case that merges.
