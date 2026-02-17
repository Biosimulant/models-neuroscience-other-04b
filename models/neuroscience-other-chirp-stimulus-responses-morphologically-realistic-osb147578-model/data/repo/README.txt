
This directory contains NEURON files associated with computing
neuronal responses to a Chirp stimulus in a morphologically realistic
model of a CA1 pyramidal neuron. These files, and the functions
there in, could be used to compute input resistance and to generate
voltage traces in response to a local Chirp current stimulus, along
various trunk locations of the model. The only channel in the model
is the h channel which has a conductance gradient, and increases
with distance from the soma. These files will help recreate results
presented in Fig. 8C of the paper referenced below.

Rishikesh Narayanan and Daniel Johnston, Long-term potentiation
in rat hippocampal neurons is accompanied by spatially widespread
changes in intrinsic oscillatory dynamics and excitability, Neuron,
56(6), pp. 1061-1075, December 2007.

If you choose to save input resistances, the input resistances along
with the corresponding radial distances of the trunk compartment
under consideration  will be saved in a file named "Trunk_RN.txt".
The actual output that you obtain by running the RN_Trunk() function
is attached.

If you choose to save responses to a Chirp stimulus, the files will
be saved in the Output directory. The traces that one will obtain
by running the "Chirp_Gh()" function are attached in the Output
directory. Only two representative traces corresponding to the first
("ChirpOutput_0.txt") and the last ("ChirpOutput_61.txt") trunk
compartments are attached. Once you run the "Chirp_Gh()", you should
get all 62 files in the Output directory. The corresponding current
values are in the file "ChirpI.txt". All these files contain 1002000
points, corresponding to a time period of 25050 ms, with 40 points
per ms.  If impedance analyses were to be performed with values
from saved files in the Output directory as voltage responses, and
values in the file "ChirpI.txt" as the current input, then the
measurements should read as in the file named "Trunk_Z.txt". It may
be noted that the distances here are the same as those in the
"Trunk_RN.txt" file, as the compartment order is the same.

For details about each of the measurements in these files and on the
gradient in the h channels, refer to the paper mentioned above.

Written by Rishikesh Narayanan. Contact: rishi.n@gmail.com
