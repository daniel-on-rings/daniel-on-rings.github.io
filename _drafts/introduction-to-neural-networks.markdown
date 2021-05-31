---
layout: post
title:  "Introduction to neural networks"
categories: machine learning intro
---

## The Activation Function

Now, the implementation of forwarding signals is not yet very useful.
Remember, when were doing Matrix Vector multiplication, what were doing is essentially [Linear Combination](https://en.wikipedia.org/wiki/Linear_combination). 
Thus, the output of our network is always linear dependant of our input.
The [Universal Approximation Theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem) however states that we can essentially approximate [any function with an Artificial Neural Network (ANN)](https://towardsdatascience.com/can-neural-networks-really-learn-any-function-65e106617fc6)
Our current output however would not even be able to learn a term like $$xˆ2$$

Here, another idea from our original model of Neural Network comes to mind.
When the dendrites of a neuron register an amount of chemicals surpassing a certain threshhold, the neuron "fires".
Not any amount of "Signal intensity" will trigger the neuron to transmit a signal 

We may use this to introduce nonlinearity to our model.
We will put each neurons output through an [Activation Function](https://en.wikipedia.org/wiki/Activation_function) such that
the neuron $$nˆ{m}$$'s activation will be $$Act_function(signal * weight)$$

$$n_{m}ˆ{L} = ActivationFunction( \sum_{a=1}ˆ{o} n_{a}ˆ{L-1} * w_{n_{a},n_{m}} )$$