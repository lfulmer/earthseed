General Questions
- What does a neuron *do*? I understand that there is a definition below, but I need 
a plane-English explanation for what a neuron *does* with data.
- How do the neurons in a layer work together?
- Why is the first input always constant or equal to 1? What's the point of having that 
input in the first place? What information does it offer?
- What does it mean to "cycle information" through the layers of an RNN? Is that type of 
cycling still possible with uni-directional RNN?
- Does batch normalization corrupt the data in any way? (If it did, it wouldn't be a very 
effective technique, I guessing I'm just asking do we have to consider this at all.)
- Is "stability" a technical term? What defines stability?
- What is bias? What's the difference between bias and weights? I think I need an 
example. I see what is happening mathematically, but I still don't really *get* it.

Functions
- Activation: See Neural Networks, Anatomy.
- Heaviside: "The unit step function", holds the value 0 for negative arguments 
(inputs) and 1 for positive arguments. All step functions can be expressed as linear 
combinations or translations of the Heaviside step function (that's why it's called the 
unit!).
- Objective: I notice that sometimes the objective function is minimized and sometimes 
it's maximized. Is there a difference between these states?
- Predictor: 
- Threshold: 

Learning
- Deep: Any machine learning algorithm that makes use of multiple neuron layers in order 
to learn a task. More layers allow one to extract more complex features from a given input 
and thus learn more complex tasks or make more complex decisions.
- Machine: Machine learning refers to any computational algorithm that performs a specific 
task without explicit instruction. Such an algorithm relies on pattern recognition and 
inference in order to complete the task and learns by experience (taking in many repeated 
examples of the data to be identified, classified, etc). In this way, machine learning 
attempts to mimic the way that humans learn. As a child, you learn that a spoon is called 
a "spoon" because a parent repeatedly refers to it as such. Children may misclassify their 
experiences because they have few reference points from which to assess them. Adults are 
typically more skilled at processing and classifying their experiences because they have a 
foundation of pattern recognition on which to base their analysis. Machine learning is an 
important technique among tasks for which explicit instructions are impossible to provide 
(i.e. "tell me which of these objects humans have never seen before").
- Transfer:

Neural Networks, Types
- Advanced: 
- Artificial: Otherwise known as simply a "neural network", ANNs are a form of machine 
learning algorithm whose architecture is made up of interconnected nodes or "neurons". 
Neurons receive, process, and transmit information among one another, collectively 
transforming input to output.
- Bayesian:
- Convolutional:
- Deep:
- Recurrent: A neural network in which the order of inputs contains meaning and inputs 
are processed in an ordered sequence, the layers are successive. For our purposes, the 
meaning of that order is the passing of time. 

Neural Networks, Anatomy
- Activation Function: Otherwise known as a "transfer function", activation functions 
determine the output of a neuron. An activation function is a mathematical proxy to the rate 
of action potential within a cell. In its most simplistic form, a neuron has two possible 
outputs: "off" - 0, and "on" - 1. With more complex outputs (i.e. a function that 
interpolates between 0 and 1), one may construct a neural network capable of more complex 
tasks. The nonlinearity of an activation function offers nuance; you can ask questions that 
have more complicated answers than "yes" or "no". Furthermore, in order to learn non-trivial 
tasks, a neural network *must* contain nonlinear activation functions. Activation functions 
typically have a sigmoid shape (close to hyperbolic tangent), and "they are [] often 
monotonically increasing, continuous, differentiable and bounded." For backpropogation, the 
activation function must be differentiable.
- Backpropogation: 
- Biases:
- Directed Connection: Connections between successive nodes occur in only one direction, 
represented by arrows.
- Feedforward:
- Fully Connected:
- Gates / Gated State / Gated Memory: 
- Gated Recurrent Units:
- Layer: The aggregation of a number of neurons. 
-- Dense:
- Long Short-Term Memory:
-- Phased:
- Memory: 
- Neuron: A mathematical function that receives one or more inputs, creates a linear 
combination of the inputs (sums them with weights), passes the linear combination through a 
non-linear function ("activation function"), and transmits the activation function resulting 
value as an output. This output may undergo further processing by other layers within the 
neural network.
- Perceptron: A linear binary classifier, a single layer neural network. Perceptrons only 
classify inputs into two categories, and the boundary between those categories is a line. 
Note, multilayer perceptrons do not match this definition. They are rather variations on 
the artificial neuron.
- Storage: 
- Weights:

Miscellaneous / Not Yet Sorted Above
- Architecture:
- Batch Normalization:
- Boosting (Boosted Decision Trees): 
- Catagorical Cross-Entropy:
- Data Mining:
- Dropout: 
- Gradient:
- k-Nearest Neighbors: 
- Latency: 
- Logic Gates:
- Multilayer Perceptrons: 
- Naive Bayes: 
- Receiver Operating Characteristic Curve:
- Semi-Supervised Learning: 
- Stability: 
- Support Vector Machines: 
- Testing Set: 
- Training Set: The set of example information from which a machine learning algorithm learns 
its intended task. Constructing a "good" (comprehensive, reprepresentative) training set is 
important, because it determines the degree to which your algorithm will perform its intended 
task in the future. If you want a child to speak multiple languages, they must receive input 
from native speakers of those languages. Similarly, a machine learning algorithm can only 
reproduce what it has been shown.


Phrases to Parse (Girl, What?):
- "computes the Bayesian evidence by marginalizing the likelihood over the parameter space"
- "encode an internal representation of previous epochs in time-series data, which along 
with real-time data, can be used for classification"
- "one-hot encoded vector"
- "proportional to the negative log-likelihood of the probabilities of a categorical 
distribution (or a generalized Bernoulli distribution)"
- "gradient descent optimizer"
- "uni-direcitonal GRU"
- "parameters that control the information that should be remembered at each step along the 
light curve"
- "encode it into a higher-dimensional representation"
- "the distribution of each layer's inputs changes as the parameters of the previous layers 
change"
- "time-distributed layer"


Question / Phrases to Parse Resting Place:
- What is the advantage of having more nodes?
-- More nodes = more nuance / expression = capable of learning more complex tasks.
- What is the standard number of nodes used for a complex task? Is the number of nodes used 
in an algorithm something that people compare / use as a metric, such as lines of code?
-- No. Figuring out how many nodes to use for a task is determined through a process of 
trial and error. Too many nodes leads to overfitting, too few nodes leads to an 
insufficiently nuanced learner.
- Why do activation functions have the shape that they do?
-- Must be nonlinear to capture nuanced infomation. Hyperbolic tangent (tanh) used because 
it has a domain of (-inf, inf) and a range of [-1, 1]. 
- What determines the shape of an activation function?
-- I feel like this question is vague. I think what determines the function in the 
intention for which we need that function. Again, hyperbolic tangent (tanh) used because 
it has a domain of (-inf, inf) and a range of [-1, 1]. This means that it can take any 
input and produce a manageable output.
- What in heaven's name are gates? What is happening?
-- Gates = decisions ; activation functions = information. Gates take input information 
and translate that information to a decision about how much of that information will be 
passed on to the next layer or fed into the activation function.
- Does forward and backward propogation just mean, "talk to a neuron closer to the output" 
and "talk to a neuron closer to the input", respectively?
-- I think so.
- How does something store long-term information? What does it mean for it to do so?
-- GATES! I still want to learn more about this, but within the context of gates, 
"memory" is just the information that is allowed to propogate to future layers. 
Information is preserved within the activation function, and if that information is 
preserved over many layers, then it is "remembered" long-term.
- What is "real-time" classification? What is meant by "real-time"?
-- I think this means in the moment or close to the moment of observation.
