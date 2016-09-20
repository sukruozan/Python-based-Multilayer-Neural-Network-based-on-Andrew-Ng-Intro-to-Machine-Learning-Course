This was my attempt at putting many of the neural network concepts and machine learning best practices into a Jupyter notebook that I learned in Andrew Ng's Coursera Intro to Machine Learning Course.  It goes beyond a simple port of the Octave code in several ways:

* It utilizes dicts for each of its data structures, I would like to say I had some grand design for this but really it just made it easier to debug in terms of keeping the code and the equations consistent in terms of the summations and naming conventions used in the course.
* It allows the user to define the number of nodes in a user-defined number of layers by specifying a shape dict.  For example, using an nn_shape={1:400,2:50,3:50,4:10} allows for the training and testing of a 400 node input fed into 2 50 node hidden layers, with a 10 node output.
* I've noticed that if you go beyond 4 or 5 hidden layers, convergance to a local optima becomes very hit or miss.  I'm honestly not sure this is because i've got some small, terrible bug in the code or because of some fundamental constraint with my strategy for back propagation.
* It allows for regularization, implemented both in back propogation and the cost function
* It allows for partial visualization of theta matrices and defines a few functions to operate on theta matrices in a way that simplifies visualization, troubleshooting, and working with SciPy.optimize.minimize params expectations.
* It defines an easy way of breaking up the 5000 example set into a training and a test set. You can simply define a % and the code will break up the data into randomized test and training sets. It is kind of fun try different strategies for various NN shapes along with different regularization coefficients to try to get the best test set accuracy score.  I once got a 94.88% with a 20% test set breakout!
* I put in some vizualization code that shows the handwritten digit at a few different angles, along with the label and prediction data to get a feel for how the neural network reacts to different situations.
* It *seems* to be error free at this point, but please feel free to issue a push request if you find any errors in my implementation of the algorithms.

If you enjoyed this notebook, learned anything from it,  have any feedback, or comments,  I'd love to hear them! Thanks, Jason.
