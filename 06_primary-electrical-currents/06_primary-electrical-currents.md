## Calculation of Primary Electrical Currents ##

Axial current flow between any two neighboring model compartments i,j is defined as iaxial = (vi - vj) / raxial , where vi , vj , and raxial are the voltages in compartment i, j, and the resistance between the compartments, respectively. In order to convert this axial current into a dipole signal, we apply a length scaling where the axial current is scaled by the inter-compartment distance along the vertical axis. The length scaling means that for the longer apical dendrites of layer 5 pyramidal neurons, the contribution will be larger than from the shorter layer 2/3 pyramidal neuron apical dendrites. Note that the orientation of the dendrites relative to the vertical axis also influences the contribution to the dipole signal. For example, the horizontally-oriented oblique dendrites which do not have any vertical length component, do not contribute to the dipole signal, whereas for basal dendrites oriented at 45 degrees from the vertical axis, the scaling is $-\sqrt{2}/2$ (note the negative sign is because these dendrites are pointing downward). The contribution from all neighboring compartments within a neuron is integrated and then added to a value across the set of all pyramidal neurons. As a result of the multiplication between axial current and length, the model dipole output signal has the same units of measure as the experimental data (in units of nano-Ampere-meters) and we are then able to directly compare the two signals, as well as precisely tune model parameters to match characteristics of recorded signals (Okada, Wu, and Kyuhou 1997).


## Tutorial References ##

Okada, Y. C., J. Wu, and S. Kyuhou. 1997. “Genesis of MEG Signals in a Mammalian CNS Structure.” Electroencephalography and Clinical Neurophysiology 103 (4): 474–85.

<br><br>
