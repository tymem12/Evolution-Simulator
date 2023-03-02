# Evolution-Simulator
The program that uses the concept of neuroevolution to simulate the evolution of creatures


It is my first major project created in Java.

The simple idea behind this project was to create a population of individuals with random "brains", which makes them take some kind of specific actions (mostly related to
moving). The environment of these individuals is composed of two types of places: white, where individuals die at the end of their lives, and green, where they can reproduce
and create a new population. The project shows that in each generation, individuals in the population are more likely to move in the direction of green spaces.

BRAIN IMPLEMENTATION DETAILS
- Every individual has its own genome made of a given number of genes.
- From the genome, we can unambiguously obtain information about the structure of the brain.
- Every gene represents one connection between two nodes.
- The brain is made up of three types of nodes.
  - Sensor- based on information about the environment, generates the pulse.
  - Neuron- collects all input pulses and sends a modified pulse on.
  - Action Neuron- collects the pulse and, based on its value, performs an action.
- Every gene consists of 32 bits:
  - 1 - indicates whether the start of the connection is a sensor or neuron.
  - 2-8 - indicate what type of sensor is given (if the connection does not have a sensor, then the value encoded in these bits is not important.
  - 9 - indicates whether the end of the connection is an action neuron or a normal neuron.
  - 10-16 - indicate what type of action neuron is given (if the connection does not have action, then the value encoded in these bites is not important).
  - 17 - indicates the sign of weight of the connection.
  - 18-32 - indicates the value of weight
  
  
  
