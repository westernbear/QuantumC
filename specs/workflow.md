# Workflow

## Lifespan of Quantum Data Type

Due to the nature of quantum mechanics, arbitrary quantum information cannot be copied into a classical memory.
This restriction comes from the postulate of quantum mechanics and a mathematical conclusion called the no-cloning theorem.

> **Proof**:
> Let $\ket{\psi} = \alpha\ket{0} + \beta\ket{1}$ denote an arbitrary qubit state, where $\ket{0}$ and $\ket{1}$ are computational basis and $\alpha, \beta \in \mathbb{C}$.
> Suppose there exists a unitary operator $\operatorname{U}: \mathcal{H}_2 \rightarrow \mathcal{H}_2$ that copies the quantum state $\ket{\psi}$ to an initial state $\ket{0}$ such that $\operatorname{U}(\ket{\psi} \otimes \ket{0}) = \operatorname{U}\ket{\psi}\ket{0} = \ket{\psi}\ket{\psi}$.
> By linearity, the following must hold:
$$ \begin{equation} \begin{align*}
    \operatorname{U}\left(\Ket{\psi}\Ket{0}\right)
    &= \operatorname{U}\left(\left(\alpha\Ket{0} + \beta\Ket{1}\right) \otimes \Ket{0}\right) \\
    &= \left(\alpha\Ket{0} + \beta\Ket{1}\right) \otimes \left(\alpha\Ket{0} + \beta\Ket{1}\right) \\
    &= \left(\alpha\Ket{0} \otimes \alpha\Ket{0}\right) + \left(\alpha\Ket{0} \otimes \beta\Ket{1}\right) \\
    &\phantom{=} + \left(\beta\Ket{1} \otimes \alpha\Ket{0}\right) + \left(\beta\Ket{1} \otimes \beta\Ket{1}\right) \\
    &= \alpha^2\Ket{00} + \alpha\beta\left(\Ket{01} + \Ket{10}\right) + \beta^2\Ket{11} \text{.}
\end{align*} \end{equation} $$
> On the other hand, we can write the system of two qubits before applying $\operatorname{U}$ such that $\ket{\psi}\ket{0} = (\alpha\ket{0} + \beta\ket{1}) \otimes \ket{0} = \alpha\ket{00} + \beta\ket{10}$.
> Noting this, if we apply $\operatorname{U}$ to the state $\ket{\psi}\ket{0}$, it gives us:
$$ \begin{equation} \begin{align*}
    \operatorname{U}\left(\Ket{\psi}\Ket{0}\right)
    &= \operatorname{U}\left(\alpha\Ket{00} + \beta\Ket{10}\right) \\
    &= \alpha\operatorname{U}\Ket{00} + \beta\operatorname{U}\Ket{10} \\
    &= \alpha\Ket{00} + \beta\Ket{11} \text{.}
\end{align*} \end{equation} $$
> Realize that the outputs of the operator $\operatorname{U}$ applied on the identical state $\ket{\psi}\ket{0}$ are not the same in $\text{(1)}$ and $\text{(2)}$:
$$ \begin{equation} \begin{align*}
    \alpha^2\Ket{00} + \alpha\beta\left(\Ket{01} + \Ket{10}\right) + \beta^2\Ket{11} \neq \alpha\Ket{00} + \beta\Ket{11} \text{.}
\end{align*} \end{equation} $$
> It implies that the copying operator $\operatorname{U}$ cannot exist and therefore, we cannot copy an arbitrary qubit state to other systems.
> This concludes the proof of the no-cloning theorem.
> ■

This quantum mechanical fact strictly restricts copying quantum data type.
The only instance of the left and the right-hand side of $\text{(3)}$ are equal is when $\alpha = 1$ exclusively or $\beta = 1$, which implies that only classical data can be copied.
A responsible quantum programming language must check whether the data is in a quantum state or not before assigning it to a classical/quantum data type variable.
In compile time, the language must ensure that every quantum variable is $\square(\lozenge\texttt{measured} \operatorname{U} \texttt{stored})$.

### Assigning to a Classical Data Type

Every classical data type cannot store quantum data with an arbitrary number of qubits.
When a value or a variable is assigned to a classical data type variable (e.g., `int`), the language ensures that the value is classical.
If the value is quantum, the quantum state must be collapsed and measured before the assignment.
Also, if a function return type is classical, the returning value must be classical or measured beforehand.

### Assigning to a Quantum Data Type

While assigning quantum data to a quantum data type variable is impossible, a qubit can be initialized based on the given classical value or variable.
