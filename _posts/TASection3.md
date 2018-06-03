---
layout: post
title:  "Hands-on session 3: Introduction to Tensorflow"
description: "Graph, Session, Nodes and variable scope"
excerpt: "Graph, Session, Nodes and variable scope"
author: "Kian Katanforoosh, Cristian Bartolome"
date:   2018-06-02
mathjax: true
published: true
tags: tensorflow
github: https://github.com/cs230-stanford/cs230-code-examples/tree/master/tensorflow
module: Tutorials
---

#CS230 Hands-on session 3: “Tensorflow Tutorial”

In this hands-on session, you will use two files:
    - Tensorflow_tutorial.py (Part I)
    - [CS230 project example code](https://github.com/cs230-stanford/cs230-code-examples) repository on github (Part II)

##Part I - Tensorflow Tutorial

The goal of this part is to quickly build a tensorflow code implementing a Neural Network to classify hand digits from the MNIST dataset.

The steps you are going to implement are:
    - Load the dataset
    - Define placeholders
    - Define parameters of your model
    - Define the model’s graph (including the cost function)
    - Define your accuracy metric
    - Define the optimization method and the training step
    - Initialize the tensorflow graph
    - Optimize (loop)
    - Compute training and testing accuracies

__**Question 1:**__​ ​Open the starter code “tensorflow_tutorial.py”. Tensorflow stores the MNIST dataset in one of its dependencies called “tensorflow.examples.tutorials.mnist”. This part is very specific to MNIST so we have coded it for you. Please read the code that loads MNIST.

__**Question 2:**__​ Define the tensorflow placeholders X (data) and Y (labels). Recall that the data is stored in 28x28 grayscale images, and the labels are between 0 and 9

__**Question 3:**__​ For now, we are going to implement a very simple 2-layer neural network *(LINEAR->RELU->LINEAR->SOFTMAX)*. Define the parameters of your model in tensorflow. Make sure your shapes match.

__**Question 4:**__​ Using the parameters defined in question (3), implement the forward propagation (from the input X to the output probabilities A). Don’t forget to reshape your input, as you are using a fully-connected neural network.

__**Question 5:**__​ Recall that this is a 10-class classification task. What cost function should you use? Implement your cost function.

__**Question 6:**__​ What accuracy metric should you use? Implement your accuracy metric.

__**Question 7:**__​ Define the tensorflow optimizer you want to use, and the tensorflow training step. Running the training step in the tensorflow graph will perform one optimization step.

__**Question 8:**__​ As usual in tensorflow, you need to initialize the variables of the graph, create the tensorflow session and run the initializer on the session. Write code to do these steps.

__**Question 9:**__​ Implement the optimization loop for 20,000 steps. At every step, have to:
    - Load the mini-batch of MNIST data (including images and labels)
    - Create a feed dictionary to assign your placeholders to the data.
    - Run the session defined above on the correct graph nodes to perform an optimization step and access the desired values of the graph.
    - Print the cost and iteration number.

__**Question 10:**__​ Using your accuracy metric, compute the accuracy and the value of the cost function both on the train and test set.

Run the code from your terminal using: *“python tensorflow_tutorial.py”* 

__**Question 11:**__​ Look at the outputs, accuracy and logs of your model. What improvements could be made? Take time at home to play with your code, and search for ideas online

##Part II - Project Code Examples

The goal of this part is to become more familiar with the [CS230 project example code](https://github.com/cs230-stanford/cs230-code-examples) that the
teaching staff has provided. It’s meant to help you prototype ideas for your projects.

__**Question 1:**__​  Please start by git cloning the “[cs230-code-examples](https://github.com/cs230-stanford/cs230-code-examples)” repository on your local computer.

This repository contains several project examples:
    - Tensorflow vision (SIGNS dataset classification)
    - Tensorflow nlp (Named Entity Recognition)
    - Pytorch vision (SIGNS dataset classification)
    - Pytorch nlp (Named Entity Recognition)

__**Question 2:**__​ You will start with the Tensorflow vision project example. On your terminal, and inside the cloned repository, navigate to *./tensorflow/vision*. Follow the instructions described in the “Requirements” section of the readme.

__**Question 3:**__​ Follow the guidelines described in the “Dowload the SIGNS dataset".

__**Question 4:**__​ Follow the guidelines described in the “Quickstart”.

__**Question 5:**__​ Read through the code and find what you could modify. All the project examples are structured the same way, we invite you to try the one that matches your needs the best. This project example code has been coded to help you insert your dataset quickly, and start prototyping some results. It is meant to be a helper code for your project and for you to learn in-depth Tensorflow/Pytorch, it is not a starter code.




