# Activation-Function

## Definition: 
Activation functions in neural networks are mathematical equations that determine the output of a neural network node, or "neuron," given a set of inputs. Each neuron typically takes in a weighted sum of inputs, adds a bias, and then passes this sum through an activation function to produce the output.
<img width="1200" alt="Screenshot 2024-02-17 at 00 10 24" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/faf6ea46-3abf-4215-95a4-d26e973c5bbf">


# Role of Activation Functions:
The role of the activation function in a neural network is to introduce non-linearity. Without non-linear activation functions, a neural network, regardless of how many layers it has, would behave just like a single-layer perceptron, which can only learn linear mappings. Non-linearity allows neural networks to learn and approximate any kind of complex function and to solve problems that are not linearly separable.

Activation functions also help to control the flow of gradients during the backpropagation training process, which is crucial for updating the weights in the network. Some activation functions, like the sigmoid or tanh, have been historically used but are less common now due to problems like vanishing gradients, where the gradients become too small for effective learning during backpropagation

# A taxonomy of activation functions
## Fixed-shape activation functions:
All the activation functions with a fixed shape, for example, all the classic activation functions used in neural network literature.
we can further divide this class of functions into:

–
rectified-based function: all the functions belonging to the rectifier family, such as ReLU, LReLU, etc.

–
classic activation function: all the functions that are not in the rectifier family, such as the sigmoid, tanh, step functions.

### Classic activation functions:
<img width="1200" alt="Screenshot 2024-02-17 at 00 43 47" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/8ac34882-9d2e-43c6-96b2-5ebacdb70fb0">
<img width="1200" alt="Screenshot 2024-02-17 at 00 43 23" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/18390a17-8183-47b3-af42-5c9405c39a3a">

##### Note that: Unfortunately, the training of networks equipped with these functions suffers from the vanishing gradient problem.

### Rectifier-based activation functions:
<img width="1200" alt="Screenshot 2024-02-17 at 00 57 19" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/e1745e1f-09b5-4af9-b704-c7371aa3d44d">
<img width="1200" alt="Screenshot 2024-02-17 at 00 59 41" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/1a4b0b03-8ac5-41e5-85d3-d2b3d418d62b">
<img width="1200" alt="Screenshot 2024-02-17 at 01 01 40" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/1437054b-fe27-4f9e-b616-5e0f78f800c6">
<img width="1200" alt="Screenshot 2024-02-17 at 01 06 09" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/cba5eaaf-b0d1-4e61-bf0d-5acfd077f68f">
<img width="1200" alt="Screenshot 2024-02-17 at 01 08 27" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/758bfbd1-4c06-452a-bd96-e8aaea812942">
<img width="1200" alt="Screenshot 2024-02-17 at 01 09 42" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/97648815-eebd-433e-8ea4-e08a20caa4d5">
<img width="1200" alt="Screenshot 2024-02-17 at 01 11 20" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/d27530e6-230c-47af-bce4-8dcbe74fdbb5">
<img width="1200" alt="Screenshot 2024-02-17 at 01 27 46" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/3d46db98-1de8-48db-867e-a860f6504e4f">
<img width="1200" alt="Screenshot 2024-02-17 at 01 27 33" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/83b9495c-fd01-4bee-925e-090e8e5a7758">

## Trainable activation functions: 
This class contains all the activation functions the shape of which is learned during the training phase. we can isolate two this into different families:

–
Parameterized standard functions: parameterized standard activation functions we refer to all the functions with a shape very similar to a given fixed-shape function, but having a set of trainable parameters that let this shape to be tuned. The addition of these parameters, therefore, requires changes, even minimal ones, in the learning process; for example, when using gradient-based methods, the partial derivatives of these new parameters are needed.

–
Functions based on ensemble methods: With the expression “ensemble methods” we refer to any technique merging together different functions. Basically, each of these techniques uses:

• a set of basis functions, which can contain fixed-shape functions or trainable functions or both;

• a combination model, which defines how the basis functions are combined together
### Parameterized standard functions:
<img width="1200" alt="Screenshot 2024-02-17 at 01 46 29" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/501c8c0c-09dd-4ecb-82cf-6eaaa549bc01">
<img width="1200" alt="Screenshot 2024-02-17 at 01 50 07" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/5d8a9d5a-134d-4040-981b-c3b9132c4e14">
<img width="1200" alt="Screenshot 2024-02-17 at 01 53 47" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/1aa606a8-37bd-4728-9d98-1ebe7cbcf582">
<img width="1200" alt="Screenshot 2024-02-17 at 01 56 41" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/5f0e2116-1a7a-4aaa-8c11-cc0086650b0b">
<img width="1200" alt="Screenshot 2024-02-17 at 01 58 47" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/33b9df46-5863-4f46-9a4b-51bc47cfb168">
<img width="1200" alt="Screenshot 2024-02-17 at 02 00 26" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/17ada8f9-7c1a-4e73-bca0-84f8a78c59c7">

### Functions based on ensemble methods:
<img width="1200" alt="Screenshot 2024-02-17 at 02 14 10" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/2732f403-4572-4870-9ee2-16ad6527423c">
<img width="1200" alt="Screenshot 2024-02-17 at 02 17 33" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/eb3715c1-3995-4527-9397-f5833364ce3f">
<img width="1200" alt="Screenshot 2024-02-17 at 02 21 59" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/df3c3419-a26e-40b0-957e-e3fc356550c5">
<img width="1200" alt="Screenshot 2024-02-17 at 02 23 01" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/d7f59070-c75f-493e-ae03-54f39b5aa1d3">
<img width="1200" alt="Screenshot 2024-02-17 at 02 26 01" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/3df788b1-aa17-439d-9d5e-6baf80f99590">
<img width="1200" alt="Screenshot 2024-02-17 at 02 28 13" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/8279fa44-aa84-4d6f-8aed-1c518614d419">

## Trainable non-standard Activation function:
These functions can be considered as a different type of computational neuron unit compared with the original computational neuron model! please read the literature if you want to know about them. 

#### In the notebook you will find python script for some of the activaion functions. You can have a look there.

### Reference:
Andrea Apicella, Francesco Donnarumma, Francesco Isgrò, Roberto Prevete,
A survey on modern trainable activation functions,
Neural Networks,
Volume 138,
2021,
Pages 14-32,
ISSN 0893-6080,
https://doi.org/10.1016/j.neunet.2021.01.026.
(https://www.sciencedirect.com/science/article/pii/S0893608021000344)
Abstract: In neural networks literature, there is a strong interest in identifying and defining activation functions which can improve neural network performance. In recent years there has been a renovated interest in the scientific community in investigating activation functions which can be trained during the learning process, usually referred to as trainable, learnable or adaptable activation functions. They appear to lead to better network performance. Diverse and heterogeneous models of trainable activation function have been proposed in the literature. In this paper, we present a survey of these models. Starting from a discussion on the use of the term “activation function” in literature, we propose a taxonomy of trainable activation functions, highlight common and distinctive proprieties of recent and past models, and discuss main advantages and limitations of this type of approach. We show that many of the proposed approaches are equivalent to adding neuron layers which use fixed (non-trainable) activation functions and some simple local rule that constrains the corresponding weight layers.
Keywords: Neural networks; Machine learning; Activation functions; Trainable activation functions; Learnable activation functions
