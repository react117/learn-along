04.02.2019
 
Challenges faced by an Expert System

1. Huge amount of data to process.
2. Unknown rules.
3. Complex rules.
4. Inexplicable rules.
 
6 Jars of Machine Learning
 
1. Data
In other words information available in various format knows as data.
 
Types of data
    * Structured data [e.g. Data in form of a table]
    * Unstructured data [e.g. reviews, raw product description, user comments etc.]
    * Image data [e.g. product pictures]
    * Video data [e.g. YouTube tutorial]
    * Audio/Speech data [e.g. gaana.com]
 
All the data has to be encoded as number [Machines only understand numbers]
 
2. Tasks
The process of producing an output based on some input [in this case data] is known as tasks. e.g. curation of FAQ based on user comments on a particular product.
 
So in mathematical terms, if x is data and y is output that can be curated with x, the task can be defined as "generating y with f(x)" where f(x) being the relation between x and y.
 
Now based on a given set of x and y, one can train a machine to determine the relation i.e. f(x) and this phenomena is called Machine Learning in layman's term. 
 
Types of task
    * Supervised
        * Classification [e.g. binary classification, multi-class classification ]
        * Regression
    * Unsupervised
        * Clustering
        * Generation
 
3. Models
In the tasks section we established a relation.
 
y = f(x) where y is the output, x is the input/data and f(x) being the relation between x and y.
 
Now this f(x) can be anything. Starting from a linear equation [y = mx + c] to an n-th degree polynomial. [![equation](https://latex.codecogs.com/gif.latex?%7Ba_0%7D%7Bx%5En%7D&plus;%7Ba_1%7D%7Bx%5E%7Bn-1%7D%7D&plus;...&plus;%7Ba_n%7D%20%3D%200)]. These functions are called models as these expressions/equations are trying to model the relation between x and y.
 
The true relation between x and y is not a model. The different types of functions that are being tried in order to determine the true relation or get as close as possible is called a model.
 
One of our job is to tell the machine to determine the parameters of an equation based on a given set of x and y.
 
The Neural Network Family of Functions
    * Sigmoid function or Logistics function 
    * Deep Convolutional Deep Neural Network function 
    * Recurrent Neural Network 
    * Neural Network function [Composite function of many sigmoid function]
 
4. Loss Function
A loss function helps to determine the closest model.
 
Let's say we have proposed 5 models that we think best describes the relation between x and y [f(x)]. Now by the loss function we can determine the loss each models produced. It is pretty straight forward. The model that produces least loss is the best suitable to describe f(x).
 
The loss function can be defined as follows:
 
Where L = Loss value [Goal is to find the model which produces the least L]
            y = True value
         f^(x) = Value produced by the proposed model
 
Few example of loss function
    * Squared Error
    * Cross Entropy
    * Kullback–Leibler [KL] Divergence
 
We take square of the difference as some of the difference may be -ve and some of them my be +ve and they can cancel each other which will prevent us from getting the correct summation. So we square to make the -ve values into +ve and add them up like a boss.
 
5. Learning Algorithm
Now lets say we have an n-th degree polynomial [] as model and we have our set of x and  y. Now we have another hurdle to cross. That is to find the parameters i.e. the coefficients of x. We can use brute force method where we can fix (n-1) coefficients and vary the last coefficient and check for which value the loss is minimum. We can repeat this process for every coefficient.
 
But in real world scenario this method is absurd. Like "a man in an iron suite" absurd. 
 
So we need to find am efficient way to compute these coefficients given the data [x/y], given the model [f^(x)] and given the loss function [L] such that the L is minimized. So it can be labelled as an optimization problem.
 
Look into the way to determine minima of y = mx + c
 
Types of Learning Algorithm / Optimization Solvers
    * Gradient Descent and it's Variants
    * Adagrad
    * RMSprop
    * Adam
    * Backpropagation [Used for training DNN]
    * Backpropagation Through Time [BPTT: Used for training RNN]
 
6. Evaluation
Every program or build need to be evaluated before making it to the world. It can be viewed as scoring system based on certain tests. The score being the value on how well the program performs in real world scenario.
 
Types of  Evaluation Matrix
    * [Top-k] Accuracy
    * Precision, Recall and F1 Score

Summary: 6 Jars of Machine Learning


So here are the 6 jars of machine learning. The relation can be stated as:
* There are Data [x] 
* And there are Tasks [y]
* Based on which Models [f^(x)] can be proposed
* And a machine Learns the algorithm based on which it tries to determine the parameters of Models [f^(x)]
* And tries to determine the best Model [f^(x)] closest to the actual solution [y = f(x)]
* Such that the Loss [L] is minimum
