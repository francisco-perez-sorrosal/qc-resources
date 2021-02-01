# Tools

An amazing tool:
* [Wolfgram Alpha](https://www.wolframalpha.com/)

## In Practice

- [O'Reilly QC](https://oreilly-qc.github.io) From [Johnston's et al. Oreilly book](refs.md#jonston) 

- [IBM Quantum](https://www.ibm.com/quantum-computing/)

- [Microsoft Quantum](https://docs.microsoft.com/en-us/quantum/)

<details><summary>Programming Frameworks</summary>
<p>

* [Q#](https://docs.microsoft.com/en-us/quantum/user-guide/)
* [Circuit Composer/Quiskit, IBM](https://quantum-computing.ibm.com/docs/)
* [Quirk](http://algassert.com/quirk) 
    - Online simulator (!6 bits as of Nov 2020)
* [DWave Leap](https://dwavesys.com/take-leap) 
    - Access to D-Wave quantum computers
    - Ocean: Ptyhon library for quantum annealing
    - Problem specific libraries: QUBO, Ising...

</p>
</details>

# Programming QC

You program a QC as a classical computer, so the interface is "classic" let's say

\\[ \mu = \frac{1}{N} \sum_{i=0} x_i \\]
Apply unitary transformation on a quantum state \\[S_{n}\\] to move to a quantum state \\[S_{n+1}\\]

Usually we cant with the current hardware have unitary tranformations represented with big matrices (Which act on many qubits) so we use unitary transformations in simpler 1 or 2 (or 4 tops) qubits..
Quantum gates move a vector representing a qubit on the Bloch sphere to another place


Quantum cirquits are equivalent to programs in the classical world

##Evolution of programming

### Past  80s and 90s

Without programming languages
Algorithm research based on linear algrebra and basic axioms of Quantum Mechanincs

Outcome: 
-Accurate algos
-Represente d with linear algebra
- Simon, Grover, Peter Shore's algorithms etc.

### Now
there are various programming languages
we are in a hybrid phase - Quantum SW is still in it's infancy but developing fast

Outocmes:

Focus on NISQ algorithms (Asdd this to the vocabl)
Universal HW agnostic quantum cirquits
Compilation & transpilation

QML: Quatum SVM, optimization

End users - mainly quantum information PhDs

## Gate Level Coding
Qiskit - Python
## Tuning know algorithms
Cirq - Python
## Embedding accurate building blocks
Q# - Python

Current state
- nOw we're limited to gate level/building blocks programming
- this  limits quantum software development creativity and productivity
- to move from 1965 a brakatrhough is required

# Future

Higher leel of abstraction
-model base
automation
syntheses of q cirquits
-varios of programming langs

outocmes:
- more quantum algorithms??? Hope so!
-focus changes over time from NISQ towards FaultTolerant algorithms

End Users:
- Quantum information experts
- Computer scientist
- Expert programmers
- Domain experts  

Quantum Algorithm design
-Cadmium comprehensive solution


