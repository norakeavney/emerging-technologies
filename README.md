# Emerging Technologies Assignment

**Author:** Nora Keavney  
**Student ID:** G00415845

This repository contains solutions to problems exploring quantum computing concepts using Python and Qiskit.

---

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- pip package manager

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/norakeavney/emerging-technologies.git
   cd emerging-technologies
   ```

2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter Lab or Jupyter Notebook:
   ```bash
   jupyter lab
   ```
   or
   ```bash
   jupyter notebook
   ```

4. Open the `problems.ipynb` notebook and run the cells.

---

## Problem 1: Generating Random Boolean Functions

This problem creates randomly generated Boolean functions that are either **constant** or **balanced**. These functions take four Boolean inputs and return a single Boolean output.

- A **constant function** returns the same value (either True or False) for all possible input combinations.
- A **balanced function** returns True for exactly half of the inputs and False for the other half.

These functions serve as the foundation for testing the Deutsch-Jozsa algorithm, which can determine whether a function is constant or balanced with a single quantum evaluation, compared to multiple classical evaluations.

---

## Problem 2: Classical Function Analysis

In this problem, a classical algorithm was developed to determine whether a Boolean function is **constant** or **balanced**.

The function takes four Boolean inputs, resulting in $2^4 = 16$ possible input combinations. The algorithm evaluates the function across these inputs and analyses the outputs:

- If all outputs are identical : the function is **constant**
- If outputs are evenly split : the function is **balanced**

The implementation guarantees correctness by evaluating all inputs in the worst case. This highlights the **classical cost** of solving the problem, as up to 16 function evaluations may be required.

This problem provides the foundation for understanding the efficiency improvement offered by quantum algorithms in later sections.

---

## Problem 3: Quantum Oracles

In this problem, the classical Boolean functions are translated into **quantum oracles** using Qiskit.

For a single Boolean input, there are four possible functions:

- $f(x) = 0$ (constant)  
- $f(x) = 1$ (constant)  
- $f(x) = x$ (balanced)  
- $f(x) = \neg x$ (balanced)

Each function is implemented as a **reversible quantum circuit** acting on two qubits:

- one input qubit  
- one auxiliary (output) qubit  

The oracles are constructed using basic quantum gates such as:

- **X gates** (bit flip)
- **CNOT gates** (conditional flip)

Each oracle was then tested using a quantum simulator to verify that it behaves according to its corresponding Boolean function.

This problem demonstrates how classical functions are embedded into quantum circuits and prepares the groundwork for implementing **Deutsch’s algorithm** in the next stage.

---

## Problem 4

*Coming soon*

---

## Problem 5

*Coming soon*

---

## References

*References will be added as the project develops.*
