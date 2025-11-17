# Random Number Generator
# Author 
 Name: Kritan Bastola
# Executive Summary
 This project focuses on building a Quantum Random Number Generator using Qiskit. The main idea is to use the quantum cirsuits to produce random numbers within a
 range chosen by the user. Along with the generator itself, the program includes a short guessing game and a graphing option to make the results easier to understand 
 and explore.

# Quantum Circuit Design
To create randomness, the program first figures out how many qubits are needed to cover the desired numerical range given by the user. Each qubit goes through a
Hadamard gate , putting it into superposition and measured into classical bits. When all qubits are measured, they collapse into a random bitstring. 
These bitstrings are then converted into integers. If the number doesn’t fit inside the range requested by the user, it simply tries again ensuring that all 
valid outputs are truly random and equally likely.

# Random Number Sampling Procedure
The circuit is simulated using Qiskit’s AerSimulator. It runs 1000 individual trials, each producing a single random number.
A dictionary myl{} keeps track of how many times each number appears.
From these results, the very first valid number is saved separately which becomes the “secret number” for the guessing game.

# Interactive Features
Initially the program asks the user to choose one option from : 
1. Play the guessing game of numbers within your given range.
2. Plot a bar graph that illustrates the repeatition of numbers within your range.
![image alt](https://github.com/kritanbastola10-bot/quantum-random-number-generator/blob/c2e7a9ca5e4cdb7dc7f1ce74e5556de7a0276662/Screenshot%202025-11-17%20231757.png)
      And then it proceeds with the program accordingly.
      
# 1. Guessing Game
Once the random number is chosen, the user can try to guess it.
The program gives hints like whether the guess is higher or lower, and counts how many tries it takes. It’s a simple way to show how unpredictable the quantum 
choice really is.
![image alt](https://github.com/kritanbastola10-bot/quantum-random-number-generator/blob/6ac3f3c0ae706fa9194e94cc07923d8cc6f053f2/Screenshot%202025-11-17%20230125.png)


# 2. Bar Graph Visualization
The second option displays a bar graph showing how often each number was generated out of the 1000 trials.
This makes it easy to see whether the distribution looks uniform and helps the user visualize quantum randomness in action.
![image alt](https://github.com/kritanbastola10-bot/quantum-random-number-generator/blob/07dd3f856cbb267a7f3cbcb425d1237c829ba33d/Screenshot%202025-11-17%20232138.png)
# Summary of Results
Overall, the QRNG works reliably for any range of numbers.
The quantum circuit behaves as expected, giving a spread of values that looks random and balanced. The bar chart reinforces this visually, 
and the guessing game adds a more playful way to interact with the quantum-generated data.
