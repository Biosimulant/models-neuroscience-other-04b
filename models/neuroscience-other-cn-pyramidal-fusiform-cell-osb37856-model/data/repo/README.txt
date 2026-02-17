README.txt

The set of .mod files and the hoc file included here implement the models
described for dorsal cochlear nucleus neurons (pyramidal cells) in the series of
papers by Kanold and Manis (hereafter referred to as K&M - 1999 and 2001).
The equations for each channel type are implemented in the pyr.mod file. The
Ikif and Ikis channel type models are based on experimentally determined
parameters (K&M 1999b). The models for Ina and Ih are based on model
previously described in the literature.

The file pyr.hoc reproduces traces in Figures 2, 3, 4 and 10 of K&M, 2001. The
original figures were run by programs implemented in C++, and exectued as a MEX
file under MATLAB, and these figures are confirmed in NEURON. The small
differences in the figures may arise from the different integration methods, or
from small differences in the initial conditions for the models in the different
simulation environments. For instance, the whole cell input resistance at rest
is 284 Mohms in the MATLAB model, and 300 Mohms in the NEURON model, though it
has been rescaled in this implementation.

Any questions regarding these implementations should be directed to:
pmanis@med.unc.edu

2 April 2004
Paul B Manis, Ph.D.

