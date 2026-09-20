# Workflow

## Copying Quantum Data Type

Due to the nature of quantum mechanics, arbitrary quantum information cannot be copied in a classical memory.
This restriction comes from the postulate of quantum mechanics and a mathematical conclusion called no-cloning theorem.

> **Proof**:
> Let $\ket{\psi} = \alpha\ket{0} + \beta\ket{1}$ denote an arbitrary qubit state, where $\ket{0}$ and $\ket{1}$ are computational basis and $\alpha, \beta \in \mathbb{C}$.
> Suppose there exists a unitary operator $\operatorname{U}: \mathcal{H}_2 \rightarrow \mathcal{H}_2$ that copies the quantum state $\ket{\psi}$ to an initial state $\ket{0}$ such that $\operatorname{U}(\ket{\psi} \otimes \ket{0}) = \operatorname{U}\ket{\psi}\ket{0} = \ket{\psi}\ket{\psi}$.
> By linearity, they following must hold:
$$
\begin{equation} \begin{align*}
    \operatorname{U}\left(\Ket{\psi}\Ket{0}\right)
    &= \operatorname{U}\left(\left(\alpha\Ket{0} + \beta\Ket{1}\right) \otimes \Ket{0}\right) \\
    &= \left(\alpha\Ket{0} + \beta\Ket{1}\right) \otimes \left(\alpha\Ket{0} + \beta\Ket{1}\right) \\
    &= \left(\alpha\Ket{0} \otimes \alpha\Ket{0}\right) + \left(\alpha\Ket{0} \otimes \beta\Ket{1}\right) \\
    &\phantom{=} + \left(\beta\Ket{1} \otimes \alpha\Ket{1}\right) + \left(\beta\Ket{1} \otimes \beta\Ket{1}\right) \\
    &= \alpha^2\Ket{00} + \alpha\beta\left(\Ket{01} + \Ket{10}\right) + \beta^2\Ket{11} \text{.}
\end{align*} \end{equation}
$$
> On the other hand, we can write the system of two qubits before applying $\operatorname{U}$ such that $\ket{\psi}\ket{0} = (\alpha\ket{0} + \beta\ket{1}) \otimes \ket{0} = \alpha\ket{00} + \beta\ket{10}$.
> Noting this, if we apply $\operatorname{U}$ on the state $\ket{\psi}\ket{0}$ gives us:
$$
\begin{equation} \begin{align*}
    \operatorname{U}\left(\Ket{\psi}\Ket{0}\right)
    &= \operatorname{U}\left(\alpha\Ket{00} + \beta\Ket{10}\right) \\
    &= \alpha\operatorname{U}\Ket{00} + \beta\operatorname{U}\Ket{10} \\
    &= \alpha\Ket{00} + \beta\Ket{11} \text{.}
\end{align*} \end{equation}
$$
> Realize that the output of the operator $\operatorname{U}$ applied on the identical state $\ket{\psi}\ket{0}$ are not same in $\text{(1)}$ and $\text{(2)}$.
$$
\begin{equation} \begin{align*}
    \alpha^2\Ket{00} + \alpha\beta\left(\Ket{01} + \Ket{10}\right) + \beta^2\Ket{11} \text{.}
\end{align*} \end{equation}
$$
> It implies that the copying operator $\operatorname{U}$ cannot exist and therefore, we cannot copy an arbitrary qubit state to other systems.
> This concludes the proof of no-cloning theorem.
> ■

<!-- $\square(\lozenge\texttt{measure} \Rightarrow \texttt{store})$ -->

### Measurement Check

### Assigning Quantum Data

