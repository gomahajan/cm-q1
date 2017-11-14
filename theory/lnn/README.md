# Complexity of Neural Networks
## Training a 3-Node Neural Network is NP-Complete
1) Linear Neural Network. This entails that when there is no hidden layer, the problem is reduced to linear programming
2) 3-Node Linear Neural network is NP-complete.
3) Shows reduction from Set Splitting problem (NP-complete).
4) Does 2) entail 3-NN with non-linear activation is NP complete too? There proof for 3) wont work when their is non-linear functions.

## Exponentially many local minima for single neurons
1) Shows error function of a single neuron may have exponential (in number of examples) local minima
2) Can be generalised for any loss and activation function when their composition L(A) is continuous and bounded.
3) Uses input-output examples which can not be realised (zero loss is not possible).
4) Also show that if the examples are realisable, then local minima ==> global minima
5) Note: even for the non-realizable case for every activation function, there exists a loss function such that local minima ==> global minima

## Local minima and plateaus in hierarchical structures of multilayer perceptrons
1) For a function that has a optimal in H-1, shows that critical point maps to multiple (lines) critical points in H space.
2) Gives necessary and sufficient conditions for them being local minimas or saddle points
3) Do not require special properties of the target, loss functions and activation functions
4) Shows how to move from space of parameters to space of function and between parameter space of H-1 neurons and H neurons. 

## On the Computational Efficiency of Training Neural Networks
