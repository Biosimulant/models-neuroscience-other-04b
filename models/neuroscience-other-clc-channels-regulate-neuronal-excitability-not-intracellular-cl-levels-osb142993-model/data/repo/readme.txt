This is the readme for the model files for the paper:

Ratte S, Prescott SA (2011) ClC-2 Channels Regulate Neuronal
Excitability, Not Intracellular Chloride Levels J Neurosci
31(44):15838-15843

These model files were supplied by Dr Steve Prescott.

ClC2-VClamp-Prescott.ode implements simulations in voltage clamp.
Data presented in Figure 1 of the paper can be reproduced using this
model

ClC2-IClamp-Prescott.ode implements simulations in current clamp.
Data presented in Figures 2 and 3 of the paper can be reproduced using
this model.

The model is for a generic, single compartment neuron with multiple
ion currents. The most notable mechanisms include ClC-2 (a rectifying
chloride-leak channel) and KCC2 (potassium chloride co-transporter 2).
A significant feature of the model is that it tracks intracellular
chloride concentration. Moreover, the GABA-A receptor is modeled as
passing both chloride and bicarbonate ions, which is important for
proper calculation of the GABA reversal potential. Ornstein-Unlenbeck
processes to simulate synaptic inhibition and excitation are also
included.
