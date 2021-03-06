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

![artificial-neuron](assets/artificial-neuron.PNG)

## McCulloh Pitts Neuron

This is the first computational model of an artificial neuron. This was proposed in 1943 by Warren S. McCulloch, a neuroscientist and Walter Pitts, a logician and hence the model was named after them.

#### Let's see the MP Neuron through the glass of [6 jars concepts.](https://github.com/react117/learn-along/blob/master/deep-learning/six_jars_of_ml.md)

### Model

Here the proposed model is a highly simplified computational model of a neuron.

![mp-neuron](assets/mp-neuron.PNG)

The model can be described as follows:

- The model operates on boolean data. Means both the input data and the output data has to be boolean form, else the model will reject them.
- Each model or neuron has a fixed threshold.
- There are two types inputes, excitatory and inhibitory.
- The model receives inputs from excitatory synapses.
- Inhibitory inputs holds absolute power over any or all excitatory inputs.
- The soma of this neuron can be devided into two parts or functions namely f(or dicision) and g(or aggregation).
- The function g aggretes all the inputs and the function f takes t he dicision based on the aggregation provided by g.
- The dicision is taken as if the aggregation of the excitatory inputs is greater than or equal to the threshold then the out put is 1 else the output will be 0. In otherhands, iff the aggregation crosses the threshold then the neuron will fire.
- Also if the neuron receives an inhibitory input, no matter what it will not fire.

So the model can be summarise as follows.

![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B150%7D%20y%3D0%5C%20if%5C%20any%5C%20x_i%5C%20is%5C%20inhibitory%2C%20else%5C%5C%20g%28x_1%2Cx_2%2C...%2Cx_n%29%3Dg%28x%29%3D%5Csum_%7Bi%3D1%7D%5E%7Bn%7Dx_i%5C%5C%5C%5C%20y%3Df%28g%28x%29%29%3D1%5C%20if%5C%20g%28x%29%20%5Cgeq%20b%5C%5C%5C%5C%20y%3Df%28g%28x%29%29%3D0%5C%20if%5C%20g%28x%29%20%3C%20b)

It is evident from the model that b is the threshold.

### Data

From the mp neuron model it is clear that it only accepts boolean inputs. Now the data that we will get to train this model can be of two types:

1. Naturally Bolean
2. Non-boolean

Now for the naturally boolean data, we do not have any problem. We can just set the data and start training our model. But for non-boolean data we have a problem. We need to convert the data to boolean.

### Task

#NON-BOOLEAN DATA IMG

Now our task is to predict whether someone will like a phone or dislike it based on the phone's data. Now these data are all real non-boolean data (e.g. the production year of a phone or battery capacity). Now we need to convert them into boolean so that the converted data can be applied to the MP Neuron model.

One example can be, for the production year, if we say that for every phone let's find wheather it came out in last 6 months. Then for every phone the becomes boolean as all those phones either came out in last 6 months (case: 1) or before last 6 months (case: 0).

Similarly we can make all the other boolean as well. And now our final dataset is ready to be fed into the MP Neuron model. This task can be termed as Binary Classification.

Also we need to set the thrreshold so that the aggregation of our boolean data produces a result that matches the true output.

### Loss Function

The loss function in the case of MP Neuron would be Squared Error Loss.

![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B150%7D%20L%20%3D%20%5Csum_%7Bi%3D1%7D%5E%7Bn%7D%28y_i%20-%20%5Chat%7By_i%7D%29%5E2)

Where,

L = Loss value (Goal is to find the model which produces the least L)

y = True value

![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B150%7D%20%5Chat%7By_i%7D) = Value produced by the proposed model

### Learning Algorithm

Here the parameter that we need to learn is b which is the threshold. So as we only need to learn a single parameter, we can use a straight forward wat known as the Brute Force Search.

So here we will do the following steps.

1. First we will assume that the value of b is 0.
2. Then we will plug-in the inputs to the MP Neuron and produce the output.
3. Then we will calculate the squared error loss.
4. We will increment the threshold by one.
5. We will repeat the steps 1-4 for n iterations(n being the total set of inputs) and find the least loss. Our goal is to find the threshold for which loss is 0.

### Evaluation

Here we will use a simple evaluation method which can be described as follows:

![equation](https://latex.codecogs.com/gif.latex?%5Cdpi%7B150%7D%20Accuracy%20%3D%20%5Cfrac%7BNumber%5C%20of%5C%20Correct%5C%20Prediction%7D%7BTotal%5C%20Number%5C%20of%5C%20Predictions%7D)
