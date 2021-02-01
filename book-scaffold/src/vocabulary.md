# Vocabulary 

## Adiabatic Quantum Computer/Computation (AQC)

In physics, an adiabatic process does not involve the transfer of heat or matter in/out
a thermodynamic system; energy is transferred only as work.

For solving a problem with addiabatic computation we need to:
1. Find a (usually complicated) Hamiltonian whose ground state describes the solution to the 
problem.
2. Prepare a quantum system with a simple Hamiltonian that is initialized with the ground state.
3. Evolve (compute) the simple Hamiltonian adiabatically to the desired complicated Halmiltonian.
4. By the adiabatic theorem the system remains in the ground state and at the end of the computation
the state of the system describes the solution to the problem.

AQC has been demonstrated [equivalent in polinomial time](https://arxiv.org/abs/quant-ph/0405098#:~:text=Adiabatic%20Quantum%20Computation%20is%20Equivalent%20to%20Standard%20Quantum%20Computation,-Dorit%20Aharonov%2C%20Wim&text=We%20describe%20an%20efficient%20adiabatic,computation%20model%20are%20polynomially%20equivalent) to the quantum cirquit-model-based computation.
The paper proves:

"Theorem 1.3 Any quantum computation can be efficiently simulated by an adiabatic computation
with two-local nearest neighbor Hamiltonians operating on six-state particles set on a two dimensional grid."

Time complexity in AQC is measured as the time taken to finalize the adiabatic evolution
which in turn is dependent on the gap in the energy eigenvalues (spectral gap) of the Hamiltonian.
When the system starts in the ground state, the energy gap between the ground state (t=0) and the first
(evolved) excited state of H(t) with t=1 is proven to be an upper bound of the rate at which the Hamiltonian can be
evolved at any time t. If the spectral gap is small, the hamiltonian evolves slowly. In O notation:

\\( T = O( 1/g^2_min \\) being \\( g^2_min \\) the minimun spectral gap for H(t) 

## (Quantum) Annealing Computing

In this kind of systems, computation is done like this:

1. Initialize the system with a quantum-mechanical superposition of all possible states with equal weights.
2. Evolve the system following a Schrodinger equation
3. The amplitudes of all candidate states keep changing, effectively describing a quantum parallelism.
4. This causes quantum tunneling between states (based on the time-dependent strength of the traversal
of the magnetic fields.)

\\( H = (1 - s) H_i + s H_f \\) where:

- \\( H_i \\) is the ground state that is supposed easy to prepare
- \\( H_f \\) is the ground state that is the solution of the problem, a hamiltonian of the
corresponging Ising model
- If s is changed slowly, the final state will be the solution to the problem. s can be changed
by modifying the strenght of a magnetic field 

[DWave Quantum Annealing Information](https://docs.dwavesys.com/docs/latest/c_gs_2.html)

Part of the quantum community do not consider quantum annealing as real quantum computers.
 
## Circuit-based Quantum Computing

## Entangelment

A primary diferentiator between classical and quantum mechanics. In the quantum world, it occurs when >2 particles 
interact and the state of each individual particle CANNOT be described independently of the state of the
 others.

## Interference

See [Deutsch algorithm](algorithms.md#Deutsch)

## Minimum Energy State
Physics systems tend to seen a state of minimum energy; objects slide down hills, a hot object
at time _t_ cools down in _t+1_... this is also true in the realm of quantum physics. 

## NISQ (Noisy Intermediate-Scale Quantum)  

Around 2020, NISQ is the current generation of quantum HW. The main drawback of this generation of HW is that it doesn't
have efficient error correction. These days quantum algorithms are very sensitive to noise in the execution environments
to achieve correct results. So while for example in the same way classical computers can't do big 
factorizations effectively, a NISQ computer also requires millions of qubits to achieve the task and this is not feasible
in many cases. The high number of qubits required is not because the algorithm requires them, but because error correction
needs to be done to achieve a required precision in the output (See difference betweent [Logical vs Phisical Qubits](#Logical vs Phisical Qubit)).

Around 2021 we can say that NISQ is the 1st generation of Quantum Computers publicly available.

## QPU

The equivalent in the quatumn computing realm to CPUs/GPUs/TPUs.

## Quantum De-coherence

The mathematical representation of a quantum system is given by a wave function. If there's a definite phase
relation between different states of the system, the system is said to be coherent. In a perfectly isolated
environment, coherence is maintained indefinitely. However, the quantum system is impossible to be maniputated.
For example, during measurement, the system isolation is broken, so coherence is shared with the environment and it's
 lost as time passes. This process is called decoherence.

## Quantum Gates

QG are basically unitary transformations, that rotate the vectors (Qbits) in the Hilbert space.

## Qubit

The (pure) states of quantum systems are modelled with normalized vectors (aka state vectors) in separable complex 
Hilbert spaces.
A vector is normalized if $$\norm\psi\norm = 1$$

A qubit is unitary vector in a two-dimensional complex Hilbert space.

Qubits are manipulated using [Quantum Gates](#Quantum Gates).

## Logical vs Phisical Qubit

1 Logical qubit ~> 1:N Physical qubits. This is related to noise disturbations. The 
lower the N the more efficient the quantum system. 

## QUBO (Quadratic Unconstrained Binary Optimization)

This problems appear in computer science, specially in Machine Learning. Variables are true/false
which corresponds to 1/0 values. QUBO problems are defined by a diagonal matrix Q, an NxN upper
triangular matrix of real weights, and x a vector of binary variables, to minimize the function:

\\( f(x) = sum_i Q_i,i*x_i + sum_i Q_i,j*x_i*x_j \\)

The diagonal terms Q_i,i are the linear coefficients and the non-zer off-diagonal terms are the
quadratic coefficients. In short:

\\( min_x x^T*Q_*x \\)

## Superposition

A superposition it's just a special type of linear combination


## Reversible Computation
