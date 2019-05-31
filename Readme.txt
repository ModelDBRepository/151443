Readme file

The present files complement the paper:

Balbi P., Martinoia S., Colombo R., Massobrio P. Modelling the spinal
alfa-motoneuron recurrent discharge: Reappraisal of the F wave. Clin
Neurophysiol, published online 25 October 2013, DOI:
http://dx.doi.org/10.1016/j.clinph.2013.09.025

Pietro Balbi, 22/4/2012 - 2/11/2013

A cat spinal alpha-motoneuron model. With the present implementation one
can directly vary through Neuron GUI (some of the)geometric and
biophysical (i.e. conductances) parameters of soma and axon initial
segment. This is recommended, rather than using the Neuron interpreter,
because some parameter changes together affect more than one section.

'initSS.hoc' loads in sequence the other files and initializes the
system to a previously saved steady-state (file 'states.dat').

'cat_alfa_mn.hoc' contains the topology, the geometry and the biophysics
of the model. The neuron model is represented as a nonuniform cylinder,
divided in different segments: distal, middle and proximal dendrites
(dend[0-2]), a soma, an axon hillock (frustum-shaped), an initial
segment, fourty alternating myelinated internodal segments (myel[0-39])
and nodes of Ranvier (node[0-39]).

'gr.ses' displays four graphics for different variables plotting, the
StandardRun Panel,a stimulating electrode onto the soma.

'change_param' adds a panel for changing on-line different geometric
parameters: soma diameter and lenght, initial segment diameter and
lenght, axon hillock lenght.

'change_cond.hoc' adds two more panels for changing the density of
different active conductances inserted onto the sections of the model.
For details, see also the main paper.

The directory 'channels' contains the .mod files for instantiating the
mechanisms of passive and active channels of the model.

Use of the model: Click Init & Run to display an ortodromic action
potential. Insert IClamp[0] into a distal node (from interpreter:
node[35] IClamp[0].loc(.5), for example), and see whether antidromic
soma invasion occurs (you would also reduce the intensity of IClamp[0]
when stimulating at the nodes). Then change the soma.diam to 35 um and
to 39 um and see what happens. Also try changing various geometric and
biophysical parameters.