## Network Architecture: Synaptic Connectivity ##

<div class="stylefig">
<table style="border:none">
  <tr>
    <td style="border:none" width=>
        <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/synaptic-connectivity.png">
          <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/synaptic-connectivity.png" alt="synaptic-connectivity" />
        </a>
    </td>
    <td style="border:none; vertical-align:middle;">
      <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/3d-column-model.png">
        <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/3d-column-model.png" alt="3d-column-model" />
      </a>
    </td>
  </tr>
  <tr>
    <td style="border:none">
      <p style="text-align:justify;">
        Computational neural model written in NEURON-Python simulates the direction and time-course of the primary electrical currents (Jp; indicated via red arrows) via intracellular electrical currents in cortical pyramidal neuron dendrites (units: nano-Ampere-meters).
      </p>
    </td>
    <td style="border:none">
      <p style="text-align:justify;">
        Model of cortical column includes 100s to 1000s (scalable) of multicompartment pyramidal neurons and single compartment interneurons (model source code)
      </p>
    </td>
  </tr>
</table>
</div>

Neurons in the model are arranged in three dimensions. The XY plane is used to array cells on a regular grid while the Z-axis specifies cortical layer. HNN’s default model contains a regular 10 x 10 grid (arbitrary units) of pyramidal neurons in layer 2/3 and layer 5 for a total of 200 pyramidal neurons. There are also 35 interneurons per cortical layer, interspersed between the pyramidal neurons. In total, the default model therefore contains 270 neurons. The 3D visualization below shows the neurons, rotated to allow easier viewing. The top and bottom represent cortical layer 2/3 and layer 5. In the visualization, the following color code is used for the different cell types in the model– red: layer 5 pyramidal neurons; green: layer 2/3 pyramidal neurons; white: layer 2/3 interneurons; blue: layer 5 interneurons.

<div class="stylefig">
  <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/colored-column-model.png">
    <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/colored-column-model.png" alt="colored-column-model" style="max-width:200px"/>
  </a>
</div>

The illustration below shows a schematic of local network connectivity. The blue cells are pyramidal cells, while the orange circles represent the interneurons. The lines between neurons represent local synaptic connections. Lines ending with a circle are excitatory (AMPA/NMDA) synapses, while lines ending with a line are inhibitory (GABAA/GABAB) synapses. Note that within a cortical layer there is recurrent connectivity between neurons of a given type (Pyramidal neuron to Pyramidal neuron, interneuron to interneuron), Pyramidal neuron to interneuron connectivity, and synaptic inhibition from interneurons onto pyramidal neurons. The following synaptic connections are present across cortical layers: layer 2/3 pyramidal neurons to layer 5 pyramidal neurons, layer 2/3 interneurons to layer 5 pyramidal neurons, layer 2/3 pyramidal neurons to layer 5 interneurons. Note that although not shown in the figure, there are also inhibitory synaptic connections between interneurons within a layer. The connectivity details are based on the neocortical microcircuit wiring patterns determined in experiments.

<div class="stylefig">
  <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/detailed-connectivity.png">
    <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/detailed-connectivity.png" alt="detailed-connectivity" style="max-width:200px"/>
  </a>
</div>

Note that in the default model, within a layer, there is all-to-all connectivity between pyramidal neurons. The synaptic weights between neurons are scaled inversely by the distance in the XY plane (arbitrary units) between the neurons (d) using exponential fall-off following , and space constant . The synaptic delays are scaled in proportion to the XY plane distance (d) between the neurons following , to account for the larger propagation. This scaling is illustrated in the figure below, with  of 3. The figure below represents one neuron located at the center (x=0, y=0), with other neurons positioned relative to that neuron (neuron positions indicated with black dots). As shown, with increasing distance from the center, the synaptic weights decay, while the synaptic delays increase.

<div class="stylefig">
  <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/weight-scaling.png">
    <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/weight-scaling.png" alt="weight-scaling" style="max-width:500px"/>
  </a>
</div>
<br>
In future versions of HNN, we will allow adjustments to the local circuit architecture and connection profiles. For more details of the default model see Jones et al., 2009<sup>1</sup>.

## Tutorial References ##

1. Jones, S. R. et al. Quantitative analysis and biophysically realistic neural modeling of the MEG mu rhythm: rhythmogenesis and modulation of sensory-evoked responses. J. Neurophysiol. 102, 3554–3572 (2009).

<br><br>
