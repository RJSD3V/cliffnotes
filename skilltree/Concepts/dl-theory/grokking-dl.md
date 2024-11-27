
 Interesting problem to solve: Get an algorithm to understand emotions and react in "Nods" or head shakes. 

On a higher level, every model basically transforms a dataset into a different dataset. The way it does it is attributed to what kind of model is used to understand the data. 
### Parametric Vs. Non -Parametric Learning

How the learning is stored or Method for Learning. 

**parametric** : 
- Characterised by having a fixed number of parameters - Trial and Error.
- The entirety of what the model has learned can be captured in the state of the parameters at a given time. 

**non-parametric** : 
 - The model's number of parameters are infinite.  (determined by the data. ) - Counting and Probability.
 - The number of parameters or "knobs" depends on the data. 
 - There is counting involved in some way, where the model counts distinct examples to determine the number of "classes" as opposed to parametric learning, where the classes are predetermined. 

### How to design a Neural Network for Prediction - Forward Pass

"How do I choose how many data points to propogate at a time" - Can the Neural Network be accurate with the data you give it?

Alwasys present enough information to the neural network. Enough information is defined by how much a human might need to a make the same prediction. 

Basic of a Neural network 

```
def neural_network(inputs, weight, bias):

	predictions = map(lambda x: (x * weight) + bias, inputs)
	return predictions
```

Neural Network with Multiple Inputs:

```
def neural_networks(inputs, weights, bias):

```


At the most basic level, weights are multiplied by respective inputs and summed up together. these are called **weighted sums** (dot products): 

` prediction = w (knowledge) * ni (information) # element-wise multiplication of vectors. 


