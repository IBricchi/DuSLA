# Dual System Learning Algorithm (DuSLA)

DuSLA is a learning algorithm designed to run on continuous input. Neural networks are designed to resemble the brain, for the most part, they miss a lot of the normal functions of the brain. The two main points DuSLA tries to change are:

* Fully connected aspect of brains
* Memory

To accomplish both of these sections I thought it might be useful to connect each node to each other node. By doing this not only would the neural network be able to resemble a brain more closely structure wise but would also allow for past inputs to affect current inputs. Let me explain.

Firstly current networks, to the best of my knowledge work on a foundation of levels. The first network takes in information, passes it on to the second layer, which then passes it on to the third, and so on until there is an output. This, of course, is the simple version, there are dozens of models which expand on this concept, but overall this is the standard. The brain is not a layered network, it's an intricate connection between different neurons each which connect to a bunch of other neurons. Eventually, the whole brain in some manner is connected, any neuron can in some form receive information that originated from any other neuron, and hence can also send information that will affect any other neuron. Each neuron has different effects on the information it receives, hence allowing for an amazing amount of complexity which creates the marvel of the brain. Some of these neurons simply process data and pass it on, however a few of these act as inputs and outputs.

On top of full connectivity, the brain also has two main systems, the conscious and the subconscious. The subconscious, as I'm going to be using it is going to be what controls the autonomic nervous system, that's to say it is the system the body uses to react almost instantly to input. Basically, it is a hardcoded response the body has to information, it's purely led by genetics and for the purpose of the first model will not change.

The third aspect that DuSLA uses as inspiration is the way the brain learns. The brain is basically an amazing algorithm, it takes inputs and produces outputs. One of these inputs would be feel-good hormone receptors (not sure how else to put it really). Basically, we humans only really do things because it feels good to do it, and don't do things because things feel bad. This is obviously oversimplified but overall it describes it well enough for the purposes of this project. 

## Structure

Taking these ideas into account DuSLA has two main units:

* Processing unit
* Automatic unit

### The Processing Unit

The processing unit represents the conscious part of the brain. Every neuron in this system would be fully connected to start with, however through training, the system would find ways to limit and adjust these connections, but this will be discussed later on. There would be three main types of neurons in this sector:

* Inputs
* Processors
* Outputs

Inputs would be just that really, inputs, they would only relay the information they received. Processors and outputs would be different. Just like neurons each could have a  different algorithm to process data, outputting the results either to a net of other neurons or in the case of the output neurons as the output of the system.

Based on this structure inputs would never truly leave the system, they would in a way affect how information is processed, in this way there would be a sort of memory, past events would remain in the system forever. This system would hence be able to in some manner learn and remember, obviously this wouldn't be perfect, but as the system was trained these memories of sorts just like in normal brains time improve the way it handles data.

### The Automatic Unit

This part of the algorithm is inspired by the autonomic system of the body. Although it isn't quite the same. The first thing to take into account is that at least for the first implementation this section of the DuSLA would be hard coded, eventually, it could be expanded to evolve but for the moment the idea is to have a pre-made system.

All inputs would be used in this system, each type of input would, just like in the human body, each input type causes different effects on the brain, pain is bad, eating is good. Basically, based on the inputs the system creates a simple good or bad system, based on this, and the current state of the processing system the Automatic system would act as the training algorithm of sorts. If the system is receiving negative inputs it'll try to change the system to change the way information is processed. And if it's receiving positive feelings it'll train to produce the same results.

## Information Processing

Training algorithms normally use backpropagation to train systems, these need structured systems, something which clearly doesn't work in this program. As so I tried to come up with a new system to not only train the programme but also to process data. Normal systems use weights with which they take weighted averages to decide how information is processed. However instead of each neuron deciding how data is processed this system would instead have each neuron decide what other neurons to send data to. The way I propose for this to work would be what I'm calling thresholds. These would replace the weights, each neuron would have a threshold for every other neuron. 

For this to work properly, there would have to be an equal distribution of neurons with upper and lower thresholds. The reason for this is that if all of the thresholds were of one type the output would always tend towards either the lowest input or the highest input.

Each neuron would hence only apply a function to whatever input it received, these functions could be averages or otherwise, however just like with any other algorithm used in machine learning, it would have to take each input into account equally.

One concern I have which I haven't been able to account for in mental models is whether or not the results would always lean towards the middle of the highest and lowest inputs. If so maybe just like in normal brains, neurons could be designed to randomly send values. This could take two forms:

* Random values
* Send to random nodes

The random values are as the name explains the production of random values within individual neurons which then are sent according to the normal rules.

Send to random nodes, would allow for neurons to randomly send values to nodes which would normally fall to high or too low for the threshold.

Until a model is built I don't know if the problem would arise or not, or even if my solutions would even work.

## Training

Training would be difficult, I don't actually know exactly how it would work, but in short, since the thresholds in a way could be used as probabilities, matrices with probabilities to be sent to other nodes would be easy to create. This matrix could be put through something similar to a Markov chain, however, these chains would not necessarily be the same as Markov chains however the concept of a Markov chain could allow for calculation of specific probabilities. Of inputs causing outputs, which in turn could be used to adjust the thresholds.

The specifics of this would still have to be worked out, but I think that this could definitely be a starting point.

## Uses

Since just as in real life processing through the autonomic system is significantly faster than the conscious mind, so too will the processing of the automatic unit be faster than processing unit. For that reason just as in real life, the input of the system would have to be continuous, since training is based on inputs and outputs, if inputs change too quickly the autonomic unit would adjust thresholds of the processing unit based on faulty input-output links. This could be accounted for slightly but ultimately the best solution I could think is having continuous inputs.

As the whole system is based on DuSLA avoiding negative input and trying to improve positive inputs, DuSLA would have to in some way be able to manipulate its inputs. This could be good for creating media, playing games, and anything which allows for DuSLA to manipulate what could be considered it's environment.
