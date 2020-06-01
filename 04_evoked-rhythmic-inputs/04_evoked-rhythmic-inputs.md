## Exogenous Driving Inputs: Evoked and Rhythmic ##

### Proximal vs. Distal Inputs ###
At rest, the default model does not generate activity. Instead, we use exogenous inputs to drive network dynamics. We use the terms proximal and distal to refer both to the origin of the inputs as well as the laminar target within the neocortical microcircuit. Proximal inputs refers to inputs arriving from lemniscal thalamus, which primarily target the granular and infragranular layers while distal inputs arrive from non-lemniscal thalamus and cortico-cortical feedback, which primarily target the supragranular layers. These differences are illustrated below.

<div class="stylefig">
  <table>
    <tr>
    <td>
      <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/prox-drive.png?token=AFRQR6AU7A3IM2S25AL3BO262UV6A">
        <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/prox-drive.png?token=AFRQR6AU7A3IM2S25AL3BO262UV6A" alt="image25"/>
      </a>
    </td>
      <td>
        <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/dist-drive.png?token=AFRQR6HBPSOMRAOS73W5FXK62UVYC">
          <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/dist-drive.png?token=AFRQR6HBPSOMRAOS73W5FXK62UVYC" alt="image17"/>
        </a>
      </td>
    </tr>
  </table>
</div>

The left schematic here shows proximal inputs which target basal dendrites of layer 2/3 and layer 5 pyramidal neurons, and somata of layer 2/3 and layer 5 interneurons. The red arrows indicate that these proximal inputs push the current flow up the dendrites towards supragranular layers. The right schematic shows distal inputs which target the distal apical dendrites of layer 5 and layer 2/3 pyramidal neurons and the somata of layer 2/3 interneurons. The green arrows indicate that these distal inputs push the current flow down towards the infragranular layers.

### Exogenous Driving Inputs: Evoked ###

Evoked response inputs are synaptic inputs that are used to model event related potentials (ERPs). These inputs are typically super-threshold, meaning they cause neurons to fire action potentials. See Tour of the GUI for the full set of parameters modulating evoked inputs.


### Exogenous Driving Inputs: Rhythmic ###

Rhythmic Inputs are synaptic inputs that are used to model ongoing rhythms, such as alpha, beta, and gamma (see illustration below and Tour of the GUI for full set of parameters).


<br><br>
