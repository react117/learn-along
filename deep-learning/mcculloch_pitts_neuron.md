## Neuron

A neuron is an electrically excitable cell that receives, processes and transmits information through electrical and chemical signals. They are the primary components of the central nervous system.

![biological-neuron-model](assets/biological-neuron-model.png)

A typical neuron consists of a cell body called soma, dendrites, and an axon.

### Dendrite
It is a branched protoplasmic extensions of a nerve cell that propagates the electrochemical stimulation received from other neural cells to the cell body, or soma, of the neuron.

### Soma
It is the heart of a neuron, containing the cell nucleus. The word 'soma' comes from the Greek 'σῶμα', meaning 'body'. This actually processes the input brought in by dendrite.

### Axon
An axon (from Greek ἄξων áxōn, axis), or nerve fiber, is a long, slender projection of a neuron, that typically conducts electrical impulses known as action potentials away from the soma. The function of the axon is to transmit information to different neurons, muscles, and glands.

### Synapse
It is a structure that permits a neuron to pass an electrical or chemical signal to another neuron or to the target effector cell. In other words this is the point of connection between two neurons.

## Artificial Neuron

An artificial neuron is a mathematical function conceived as a model of biological neurons described above. These are elementary units in an artificial neural network. It receives one or more inputs (via dendrite) and sums them to produce an output (takes place in soma). The output can be represented as an activation which is transmitted along its axon. 

#ART NEURON IMG

## McCulloh Pitts Neuron

This is the first computational model of an artificial neuron. This was proposed in 1943 by Warren S. McCulloch, a neuroscientist and Walter Pitts, a logician and hence the model was named after them.

#### Let's see the MP Neuron through the glass of 6 jars concepts.

### The Model

Here the proposed model is a highly simplified computational model of a neuron.

#MP NEURON IMG

The model can be described as follows:

- The model operates on boolean data. Means both the input data and the output data has to be boolean form, else the model will reject them.
- Each model or neuron has a fixed threshold.
- There are two types inputes, excitatory and inhibitory.
- The model receives inputs from excitatory synapses.
- Inhibitory inputs holds absolute power over any or all excitatory inputs.
- The soma of this neuron can be devided into two functions namely f and g.
- The function g aggretes all the inputs and the function f takes t he dicision based on the aggregarion provided by g.
- The dicision is taken as if the aggregation of the excitatory inputs is greater than or equal to the threshold then the out put is 1 else the output will be 0. In otherhands, iff the aggregation crosses the threshold then the neuron will fire.
- Also if the neuron receives an inhibitory input, no matter what it will not fire.
