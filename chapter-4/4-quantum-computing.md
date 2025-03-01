# Quantum Computing

In the previous chapter we introduced the techniques and the benefits of game-based learning. We will then discuss the basic theory around quantum computing, which provided the information needed to design the theory slides presented in the game and on which the game mechanics are based.

Quantum computers are computers that perform calculations by taking advantage of quantum phenomena, such as superposition and entanglement. The quantum properties of the microcosm provide the ability to store and process larger amounts of information and perform specific calculations at higher speeds than conventional computers. Information is processed using quantum gates and quantum algorithms, analogs of which cannot exist in conventional computers. [@karafyllidis_book], [@wikipedia_quantum_computing]

## Quantum Bits

Quantum computers store information as bits. A quantum bit is a two-state system based on properties of the microcosm such as spin, energy state or the way particles oscillate and is the basic unit of information storage. [@wikipedia_quantum_computing]

State 0 is represented as $|0\rangle$ and state 1 as $|1\rangle$ and are called basic or basis states and are orthogonal to each other. Because the two states belong to a vector space, Hilbert space^[https://en.wikipedia.org/wiki/Hilbert_space], they can be multiplied by a number and added together, and the result will be a valid state. Superposition is based on this fact. [@wikipedia_quantum_computing]

Each valid state can be written as:
$$|q\rangle = a|0\rangle + b|1\rangle$$
where a and b are called probability amplitudes and are complex numbers. The magnitudes of a and b are always less than one, and it holds that:

$$|a|^2 + |b|^2 = 1$$

The two basic states of a qubit can be represented as matrices:

$$
|0\rangle = \begin{pmatrix}
1 \\
0
\end{pmatrix}
$$

$$
|1\rangle = \begin{pmatrix}
0 \\
1
\end{pmatrix}
$$

The state $|q\rangle = a|0\rangle + b|1\rangle$ can be represented using matrices as follows:
$$
|q\rangle = a \begin{pmatrix}
1 \\
0
\end{pmatrix} + b \begin{pmatrix}
0 \\
1
\end{pmatrix} = \begin{pmatrix}
a \\
b
\end{pmatrix}
$$

The probability amplitudes, a and b, are complex numbers, so we can write the last equation in a more general form:

$$
|q\rangle = e^{i\phi_a} \sin\left(\frac{\theta}{2}\right) |0\rangle + e^{i\phi_b} \cos\left(\frac{\theta}{2}\right) |1\rangle \Leftrightarrow
$$

$$
|q\rangle = e^{i\phi_a} \Bigl( \sin\left(\frac{\theta}{2}\right) |0\rangle + e^{i(\phi_b - \phi_a)} \cos\left(\frac{\theta}{2}\right) |1\rangle \Bigr)
$$

If the global phase term $e^{i\phi_a}$ is omitted while the phase difference $\phi_b - \phi_a$ is called $\phi$, the last equation simplifies to the following:

$$
|q\rangle = \sin\left(\frac{\theta}{2}\right) |0\rangle + e^{i\phi} \cos\left(\frac{\theta}{2}\right) |1\rangle
$$

The angle $\theta$ determines the magnitude of the probability amplitudes a and b, while the angle $\phi$ is called the phase angle and does not affect the measurement outcome. This means that two qubits differing only by a phase angle cannot be distinguished by a measurement. However, the phase angle should not be omitted, as it affects quantum computations.

The term $e^{i\phi_a}$ is called the global phase and is a mathematical artifact that can be safely ignored.

[@karafyllidis_book]

### Superposition

Superposition is based on the addition of two states, similar to how we would add two waves, and gives quantum computers the ability to perform parallel computations.

A classical bit can have two distinct states, 0 or 1, and can be stored by any system that has two distinct states, closed or open. All information is analyzed, stored, and processed as a sequence of 0s and 1s by classical computers.

A quantum system can be in both states simultaneously. Before we measure its state, it tends to be in the state $|q\rangle$ or $|1\rangle$. The quantum state $|q\rangle = a|0\rangle + b|1\rangle$ is a superposition of the two basic states. Measuring the state of the system destroys the superposition, so a qubit can only be found in one of the two basis states.

The outcome of the measurement is impossible to predict with certainty, as all we know are the probabilities of it being in one of the two basis states, which are given by the square of the probability amplitudes, a and b.

[@aws_quantum_computing], [@karafyllidis_book]

### Quantum Entanglement

Quantum entanglement is defined as the state of two quantum systems when it cannot be written as a tensor product of their basic states. Quantum entanglement is a physical resource that can be used for the development of quantum algorithms and the execution of quantum computations. There is no classical analog of this state. When two systems are entangled, measuring the state of one reveals the state of the other, regardless of the distance between them. Essentially, the state of one quantum system depends on the state of the other. [@aws_quantum_computing], [@karafyllidis_book]

### Decoherence
Superposition states are unstable and decohere so that the system becomes stable. Decoherence is an irreversible process and can be caused by external factors such as an increase in temperature or radiation. [@aws_quantum_computing]

## Quantum Registers
Quantum registers are an array of qubits used as memory and represent a superposition of $2^n$ quantum states, where $n$ is the number of qubits. The numbering of the qubits is done from right to left or from bottom to top. Quantum computers do not have classical circuits but perform operations by acting on bits that are within quantum registers.

The state of a quantum register with $n$ qubits is defined as the tensor product of the states of the qubits that comprise it:

$$
|q_r\rangle = |q_{n - 1}\rangle \otimes ... \otimes |q_1\rangle \otimes |q_0\rangle
$$

[@karafyllidis_book]

## Quantum Gates

https://quantum.microsoft.com/en-us/insights/education/concepts/single-qubit-gates#:~:text=The%20Y%20gate%20performs%20a,essential%20for%20many%20quantum%20algorithms.

https://www.sharetechnote.com/html/QC/QuantumComputing_Gate_X.html

Quantum gates are not physical systems like classical gates, but physical processes applied to quantum bits (qubits) and registers that change their state. Additionally, information does not pass through quantum gates as it does with classical gates, since they are not part of any physical circuit with conductors. The information remains within the quantum registers, and the gates act on them by rotating their state vectors. A quantum gate can be a laser pulse or a magnetic field. [@karafyllidis_book], [@wikipedia_quantum_computing]

Since quantum bits are vectors in Hilbert space, quantum gates must be operators in Hilbert space. However, not all operators in Hilbert space are suitable for representing quantum gates. For an operator to be characterized as a quantum gate, it must not change the length of the state vector, only its angle, and it must not change the values of the inner products between state vectors. Thus, only unitary operators can constitute quantum gates. [@karafyllidis_book], [@wikipedia_quantum_computing]


The table below presents some of the most well-known quantum gates and the effects of their actions.

+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Name(s)                                             | # of qubits            | Symbol(s)                        | Matrix                                                                                                                            |
+:===================================================:+:======================:+:================================:+:=================================================================================================================================:+
| Identity, No-Op                                     | any                    | I                                | $\begin{pmatrix} 1 & 0 & \cdots & 0\\ 0 & 1 & \cdots & 0\\ \vdots & \vdots & \ddots & \ddots\\ 0 & 0 & \cdots & 1\end{pmatrix}$   |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Pauli-X, NOT, Bit Flip                              | 1                      | X, NOT, σ~x~                     | $\begin{pmatrix} 0 & 1\\ 1 & 0\end{pmatrix}$                                                                                      |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Pauli-Y                                             | 1                      | Y, σ~y~                          | $\begin{pmatrix} 0 & -i\\ i & 0\end{pmatrix}$                                                                                     |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Pauli-Z, Phase Flip                                 | 1                      | Z, σ~z~                          | $\begin{pmatrix} 1 & 0\\ 0 & -1\end{pmatrix}$                                                                                     |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Phase                                               | 1                      | S, P, $\sqrt{Z}$                 | $\begin{pmatrix} 1 & 0\\ 0 & i\end{pmatrix}$                                                                                      |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Hadamard                                            | 1                      | H                                | $\frac{1}{\sqrt{2}} \begin{pmatrix} 1 & 1\\ 1 & -1\end{pmatrix}$                                                                  |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Controlled-NOT, Controlled-X, Controlled Bit Flip   | 2                      | CNOT, XOR, CX                    | $\begin{pmatrix} 1 & 0 & 0 & 0\\ 0 & 0 & 0 & 1\\ 0 & 0 & 1 & 0\\ 0 & 1 & 0 & 0\end{pmatrix}$                                      |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Controlled-NOT, Controlled-X, Controlled Bit Flip   | 2                      | CNOT, XOR, CX                    | $\begin{pmatrix} 1 & 0 & 0 & 0\\ 0 & 0 & 0 & 1\\ 0 & 0 & 1 & 0\\ 0 & 1 & 0 & 0\end{pmatrix}$                                      |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+
| Swap                                                | 2                      | SWAP                             | $\begin{pmatrix} 1 & 0 & 0 & 0\\ 0 & 0 & 1 & 0\\ 0 & 1 & 0 & 0\\ 0 & 0 & 0 & 1\end{pmatrix}$                                      |
+-----------------------------------------------------+------------------------+----------------------------------+-----------------------------------------------------------------------------------------------------------------------------------+

Table: Quantum Gates. [@wikipedia_quantum_gates] {#tbl:tbl601}

### Identity

The identity quantum gate does not affect the state of the qubit. Its symbol is often omitted in quantum circuits.

| $|q_i\rangle$             | $|q_o\rangle$             |
|---------------------------|---------------------------|
| $|0\rangle$               | $|0\rangle$               |
| $|1\rangle$               | $|1\rangle$               |
| $a|0\rangle + b|1\rangle$ | $a|0\rangle + b|1\rangle$ |

Table: Identity Gate Truth Table. {#tbl:tbl602}

![Identity Gate Circuit Diagram.](chapter-4/I.svg){#fig:fig601}

### Pauli-X

The quantum X gate functions similarly to the classical NOT gate, rotating the state vector by 180 degrees around the X-axis. This operation changes the state from $|0\rangle$ to $|1\rangle$ and vice versa.

| $|q_i\rangle$             | $|q_o\rangle$             |
|---------------------------|---------------------------|
| $|0\rangle$               | $|1\rangle$               |
| $|1\rangle$               | $|0\rangle$               |
| $a|0\rangle + b|1\rangle$ | $a|1\rangle + b|0\rangle$ |

Table: Pauli-X Gate Truth Table. {#tbl:tbl603}

![Pauli-X Gate Circuit Diagram.](chapter-4/X.svg){#fig:fig602}

### Pauli-Y

The quantum Y gate operates similarly to the X gate but rotates the state vector by 180 degrees around the Y-axis. It changes the state from $|0\rangle$ to $|1\rangle$ and vice versa, and additionally shifts the phase of the $|0\rangle$ state by 90 degrees and the phase of the $|1\rangle$ state by -90 degrees.

| $|q_i\rangle$             | $|q_o\rangle$                |
|---------------------------|------------------------------|
| $|0\rangle$               | $i|1\rangle$                 |
| $|1\rangle$               | $-i|0\rangle$                |
| $a|0\rangle + b|1\rangle$ | $ia|1\rangle - ib|0\rangle$  |

Table: Pauli-Y Gate Truth Table. {#tbl:tbl604}

![Pauli-Y Gate Circuit Diagram.](chapter-4/Y.svg){#fig:fig603}

### Pauli-Z

The quantum Z gate rotates the state vector by 180 degrees around the Z-axis. It shifts the phase of the $|1\rangle$ state by 180 degrees and does not affect the state of the $|0\rangle$ state.

| $|q_i\rangle$             | $|q_o\rangle$                |
|---------------------------|------------------------------|
| $|0\rangle$               | $|0\rangle$                  |
| $|1\rangle$               | $-|1\rangle$                 |
| $a|0\rangle + b|1\rangle$ | $a|0\rangle - b|1\rangle$    |

Table: Pauli-Z Gate Truth Table. {#tbl:tbl605}

![Pauli-Z Gate Circuit Diagram.](chapter-4/Z.svg){#fig:fig604}

### Phase

The S gate shifts the phase of the $|1\rangle$ state by 90 degrees.

| $|q_i\rangle$             | $|q_o\rangle$                |
|---------------------------|------------------------------|
| $|0\rangle$               | $|0\rangle$                  |
| $|1\rangle$               | $i|1\rangle$                 |
| $a|0\rangle + b|1\rangle$ | $a|0\rangle + ib|1\rangle$   |

Table: Phase Gate Truth Table. {#tbl:tbl606}

![Phase Gate Circuit Diagram.](chapter-4/S.svg){#fig:fig605}

### Hadamard

The Hadamard gate, when acting on a qubit in one of the two basis states, places it in a superposition of the two basis states. Conversely, when it acts on a qubit that is in a superposition of the two basis states, it returns it to one of the basis states.

| $|q_i\rangle$                                               | $|q_o\rangle$                                                                               |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| $|0\rangle$                                                 | $\frac{1}{\sqrt{2}}|0\rangle + \frac{1}{\sqrt{2}}|1\rangle$                                 |
| $|1\rangle$                                                 | $\frac{1}{\sqrt{2}}|0\rangle - \frac{1}{\sqrt{2}}|1\rangle$                                 |
| $\frac{1}{\sqrt{2}}|0\rangle + \frac{1}{\sqrt{2}}|1\rangle$ | $|0\rangle$                                                                                 |
| $\frac{1}{\sqrt{2}}|0\rangle - \frac{1}{\sqrt{2}}|1\rangle$ | $|1\rangle$                                                                                 |
| $a|0\rangle + b|1\rangle$                                   | $\frac{1}{\sqrt{2}}\left(a+b)\right|0\rangle + \frac{1}{\sqrt{2}}\left(a-b)\right|1\rangle$ |

Table: Hadamard Gate Truth Table. {#tbl:tbl607}

![Hadamard Gate Circuit Diagram.](chapter-4/H.svg){#fig:fig606 height=20%}

### Controlled-NOT

The CNOT gate inverts the target bit when the control bit is set to 1. It functions as an X gate controlled by the control bit.

| $|q_{control} q_{target}\rangle$                            | $|q_{control} q_{target}\rangle$                    |
|---------------------------------------------------------|---------------------------------------------------------|
| $|00\rangle$                                            | $|00\rangle$                                            |
| $|01\rangle$                                            | $|01\rangle$                                            |
| $|10\rangle$                                            | $|11\rangle$                                            |
| $|11\rangle$                                            | $|10\rangle$                                            |
| $a|00\rangle + b|01\rangle + c|10\rangle + d|11\rangle$ | $a|00\rangle + b|01\rangle + c|11\rangle + d|10\rangle$ |

Table: Controlled-NOT Gate Truth Table - Second bit as control bit. {#tbl:tbl608}

![CNOT Gate Circuit Diagram - Second bit as Control bit.](chapter-4/CNOT_2.svg){#fig:fig607 height=50%}

| $|q_{control} q_{target}\rangle$                            | $|q_{control} q_{target}\rangle$                    |
|---------------------------------------------------------|---------------------------------------------------------|
| $|00\rangle$                                            | $|00\rangle$                                            |
| $|01\rangle$                                            | $|11\rangle$                                            |
| $|10\rangle$                                            | $|10\rangle$                                            |
| $|11\rangle$                                            | $|00\rangle$                                            |
| $a|00\rangle + b|01\rangle + c|10\rangle + d|11\rangle$ | $a|00\rangle + b|11\rangle + c|10\rangle + d|11\rangle$ |

Table: Controlled-NOT Gate Truth Table - First bit as control bit. {#tbl:tbl609}

![CNOT Gate Circuit Diagram - First bit as Control bit.](chapter-4/CNOT_R.svg){#fig:fig608 height=50%}

### Swap

The SWAP gate exchanges the states of two qubits.

| $|q_{i1} q_{i0}\rangle$                                 | $|q_{01} q_{o0}\rangle$                                 |
|---------------------------------------------------------|---------------------------------------------------------|
| $|00\rangle$                                            | $|00\rangle$                                            |
| $|01\rangle$                                            | $|10\rangle$                                            |
| $|10\rangle$                                            | $|01\rangle$                                            |
| $|11\rangle$                                            | $|11\rangle$                                            |
| $a|00\rangle + b|01\rangle + c|10\rangle + d|11\rangle$ | $a|00\rangle + b|10\rangle + c|01\rangle + d|11\rangle$ |

Table: SWAP Gate Truth Table. {#tbl:tbl610}

![SWAP Gate Circuit Diagram.](chapter-4/SWAP.svg){#fig:fig609}

## References {.unnumbered}

The details about quantum gates and the tables are based on the following sources:

  * [@karafyllidis_book]

  * [@azure_multi_bit_gates]

  * [@azure_single_bit_gates]

  * [@wikipedia_quantum_gates]

The images are sourced from [@wikipedia_quantum_gates].
