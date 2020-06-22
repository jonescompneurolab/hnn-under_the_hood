## Neurons:  Morphology and Physiology ##

The template cortical column model contains the following types of neurons:

1. L2/3 multi-compartment pyramidal neurons (PN)
2. L2/3 single compartment inhibitory neurons
3. L5 multi-compartment pyramidal neurons
4. L5 single compartment inhibitory neurons

Membrane voltages in each simulated compartment are calculated using the standard Hodgkin-Huxley parallel conductance equations. Current flow between compartments are calculated using properties of the cable equation<sup>1</sup>.

### Morphology ###

Layer 2/3
- PN: 7 compartments including 3 apical dendrites, 3 basal dendrites, 1 soma
- Inhibitory basket neurons: single compartment (soma)

Layer 5
- PN: 9 compartments including 5 apical dendrites, 3 basal dendrites, 1 soma.
- As shown below, L5 PNs have longer dendrites than L2/3 PNs. L5 PN somas based in L5 with long apical dendrites reaching into L2/3.
- Inhibitory Basket neurons: single compartment (soma).
- L2/3 and L5 basket interneurons are identical but their synaptic parameters and local circuit connectivity differs.

<div class="stylefig">
<a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/detailed-connectivity">
  <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/detailed-connectivity.png" alt="detailed-connectivity" style="max-width:300px" />
</a>
</div>

<div class="stylefig">
<table style="border:none">
  <tr>
    <td style="border:none" width=>
        <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/morph-params-01.png">
          <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/morph-params-01.png" alt="morph-params-01" />
        </a>
    </td>
    <td style="border:none; vertical-align:middle;">
      <a href="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/morph-params-02.png">
        <img class="imgcenter100" src="https://raw.githubusercontent.com/jonescompneurolab/hnn-under_the_hood/master/html-styling/images/morph-params-02.png" alt="morph-params-02" />
      </a>
    </td>
  </tr>
</table>
</div>

### Physiology ###

The following table displays the ion channels and mechanisms in each cell type in the model (**X** indicates the presence of the channel/mechanism in the cell type; for advanced modelers: to see the NEURON simulator equations used in the channel/mechanism, click on the links in the table).

<table class="custom" style="border:2px !important;border-color:black !important;">
  <tr>
    <td>
      Cell Type (rows) Channel/ mechanism Type (columns)
    </td>
    <td>
      Na (fast)
    </td>
    <td>
      K (fast)
    </td>
    <td>
      Km
    </td>
    <td>
      KCa
    </td>
    <td>
      Ca (L-type)
    </td>
    <td>
      Ca (T-type)
    </td>
    <td>
      Ca (decay)
    </td>
    <td>
      HCN
    </td>
    <td>
      Leak
    </td>
    <td>
      Dipole
    </td>
  </tr>
    <td>
      Basket
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    X
    </td>
    <td>
    </td>
  <tr>
    <td>
      L2/3 Pyramidal
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
  </tr>
  <tr>
    <td>
      P5 Pyramidal
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
    <td>
    X
    </td>
  </tr>
</table>

In the table above, Na (fast) / K (fast) are the fast sodium and potassium channels responsible for generating action potentials. Km is the muscarine sensitive potassium channel, with a relatively slow time-constant and KCa is the calcium-dependent potassium channel, which contributes to hyperpolarization after calcium influx into the cell. The L- and T-type calcium (Ca) channels represent the high-threshold and low-threshold activated calcium channels which together with the hyperpolarization-activated cyclic nucleotide gated channel (HCN) contribute to bursting. Ca decay represents the calcium extrusion pump, which causes intracellular calcium to decay towards a baseline level. Leak represents the passive channel, with constant conductance. Dipole represents the mechanism that takes into account the primary axial current flow within pyramidal neuron dendrites, responsible for the generation of simulated signals comparable to MEG/EEG recordings. For more details see <sup>2</sup>.

## Tutorial References ##

1. Dayan, P. & Abbott, L. F. Theoretical neuroscience. 806, (Cambridge, MA: MIT Press, 2001).

2. Jones, S. R. et al. Quantitative analysis and biophysically realistic neural modeling of the MEG mu rhythm: rhythmogenesis and modulation of sensory-evoked responses. J. Neurophysiol. 102, 3554–3572 (2009).

<br><br>
