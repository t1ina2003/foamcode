# NeuralNetwork

- weight, neurons
- output layer, hidden layer
- many (input*weight) + bais = output
- activation function: make it 0~1
  - Sigmoid: f(outputValue) = 1/1+e^(-x)
  - REctified Linear Unit (RELU) = max(0,x)
- Forward Propogation
- NN use Backward Propogation
- cost func:
$$ 
C(weight,bias) = \dfrac{1}{2n} * \sum_{x}(target_{x} - activation_{x})^2 
\\ n = total number of datapoints, x = each point
$$
- new weight (lowest cost):
$$
\omega_{new} = \omega - \eta\nabla C
$$
- each find is epoch
- learning rate careful