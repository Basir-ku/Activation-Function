# Activation-Function

## Definition: 
Activation functions in neural networks are mathematical equations that determine the output of a neural network node, or "neuron," given a set of inputs. Each neuron typically takes in a weighted sum of inputs, adds a bias, and then passes this sum through an activation function to produce the output.
<img width="1430" alt="Screenshot 2024-02-17 at 00 10 24" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/faf6ea46-3abf-4215-95a4-d26e973c5bbf">


# Role of Activation Functions:
The role of the activation function in a neural network is to introduce non-linearity. Without non-linear activation functions, a neural network, regardless of how many layers it has, would behave just like a single-layer perceptron, which can only learn linear mappings. Non-linearity allows neural networks to learn and approximate any kind of complex function and to solve problems that are not linearly separable.

Activation functions also help to control the flow of gradients during the backpropagation training process, which is crucial for updating the weights in the network. Some activation functions, like the sigmoid or tanh, have been historically used but are less common now due to problems like vanishing gradients, where the gradients become too small for effective learning during backpropagation

# A taxonomy of activation functions

### fixed-shape activation functions:
all the activation functions with a fixed shape, for example, all the classic activation functions used in neural network literature.
we can further divide this class of functions into:

–
rectified-based function: all the functions belonging to the rectifier family, such as ReLU, LReLU, etc.

–
classic activation function: all the functions that are not in the rectifier family, such as the sigmoid, tanh, step functions.

### trainable activation functions: 
This class contains all the activation functions the shape of which is learned during the training phase. we can isolate two this into different families:

–
parameterized standard functions: in this case, we consider all the trainable functions derived from standard fixed activation functions with the addition of a set of trainable parameters.

–
Functions based on ensemble methods: they are defined by mixing several distinct functions. A common way to mix different functions is combining them linearly, i.e., the 
final activation functions are modeled in terms of linear combinations of one-variable functions. We group together all these activation functions in a subclass that we named linear combination of one-to-one functions.

<img width="826" alt="Screenshot 2024-02-17 at 00 29 53" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/5af7c779-cd4c-438f-bfc6-e5958bde4ad9">

#### Classic activation functions:
<img width="871" alt="Screenshot 2024-02-17 at 00 43 47" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/8ac34882-9d2e-43c6-96b2-5ebacdb70fb0">
<img width="940" alt="Screenshot 2024-02-17 at 00 43 23" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/18390a17-8183-47b3-af42-5c9405c39a3a">

##### Note that: Unfortunately, the training of networks equipped with these functions suffers from the vanishing gradient problem.

#### Rectifier-based activation functions:
<img width="920" alt="Screenshot 2024-02-17 at 00 57 19" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/e1745e1f-09b5-4af9-b704-c7371aa3d44d">
<img width="929" alt="Screenshot 2024-02-17 at 00 59 41" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/1a4b0b03-8ac5-41e5-85d3-d2b3d418d62b">
<img width="910" alt="Screenshot 2024-02-17 at 01 01 40" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/1437054b-fe27-4f9e-b616-5e0f78f800c6">
<img width="946" alt="Screenshot 2024-02-17 at 01 06 09" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/cba5eaaf-b0d1-4e61-bf0d-5acfd077f68f">
<img width="920" alt="Screenshot 2024-02-17 at 01 08 27" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/758bfbd1-4c06-452a-bd96-e8aaea812942">
<img width="927" alt="Screenshot 2024-02-17 at 01 09 42" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/97648815-eebd-433e-8ea4-e08a20caa4d5">
<img width="927" alt="Screenshot 2024-02-17 at 01 11 20" src="https://github.com/Basir-ku/Activation-Function/assets/123528497/d27530e6-230c-47af-bce4-8dcbe74fdbb5">





 



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
