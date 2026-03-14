Title: Dirac Notation and the Stern-Gerlach Experiment
Authors: CriticalLine
Date: 2026-03-14
Tags: [spin, dirac, intro]
Status: draft

[TOC] <!-- TOC at front of the document -->

# Dirac Notation and the Stern-Gerlach Experiment

## Introduction: Why Quantum Mechanics is Different

In the early 20th century, physicists discovered that classical physics (the rules that work for everyday objects) completely fails to describe tiny things like atoms and electrons. The new theory, **quantum mechanics**, is much richer and applies to a vast range of phenomena.

Instead of following the historical path, we will start with a single experiment that forces us to think in a completely new way—the **Stern-Gerlach experiment**. This experiment shows, in the most dramatic fashion, why classical ideas must be abandoned. It also introduces the concept of **quantum states** as vectors in an abstract space, which is the foundation of quantum mechanics.


### Symbol table (short)
- |S_z; +> / |+>: spin up along z
- |S_z; -> / |->: spin down along z
- S_x, S_y, S_z: spin operators
- ħ: reduced Planck constant

---

## 1.1 The Stern-Gerlach Experiment: A Shock Treatment

### 1.1.1 What They Did and What They Saw

In 1922, Otto Stern and Walther Gerlach performed an experiment with silver atoms.

* **Setup:** They heated silver atoms in an oven, let a beam of atoms escape through a small hole, and passed that beam through a special magnet with a **non-uniform** (inhomogeneous) magnetic field (see Figure 1.1 in the original text). The magnet's poles were shaped so that the field was stronger near one edge.
* **Why Silver?** A silver atom has 47 electrons. 46 of them form a spherical cloud with no net magnetic effect. The 47th electron (the outermost one) has a property called **spin**, which gives the whole atom a tiny **magnetic moment** $\boldsymbol{\mu}$. Think of it as a tiny bar magnet that can interact with an external magnetic field. The magnetic moment is proportional to the electron's spin $\mathbf{S}$:
    $$\boldsymbol{\mu} \propto \mathbf{S}$$
    (The exact constant is not crucial here.)

* **Classical Prediction:** In a non-uniform field, a tiny magnet experiences a force. The force depends on the magnet's orientation. Classically, the atoms' magnetic moments would be randomly oriented in space, so their $z$-components ($\mu_z$) would have a continuous range of values (from $+|\boldsymbol{\mu}|$ to $-|\boldsymbol{\mu}|$). Therefore, the beam should have spread out into a continuous band on the detector screen (Figure 1.2a).

* **The Actual Result:** The beam did **not** spread continuously. Instead, it split into **two distinct spots** on the screen (Figure 1.2b)! One spot corresponded to an upward force ($\mu_z > 0$) and the other to a downward force ($\mu_z < 0$).

✅ **The First Big Idea: Quantization**

This was shocking. It meant that the magnetic moment (and hence the electron spin) cannot point in just any direction. Its component along any axis (say, the $z$-axis) can only take on **two discrete values**. This is called **"space quantization."** For an electron, these two values are $+\hbar/2$ and $-\hbar/2$, where $\hbar$ is a fundamental unit of angular momentum.

We label these two possibilities as:

* $S_z+$ (spin up along z)
* $S_z-$ (spin down along z)

If we had used a magnet oriented in the $x$-direction, we would have seen two spots corresponding to $S_x+$ and $S_x-$.

### 1.1.2 Putting Magnets in a Row: The Puzzle Deepens

The real weirdness appears when we use two or more Stern-Gerlach (SG) apparatuses in sequence.

* **Case 1: Two $z$-magnets (Figure 1.3a)**
    1. An SG$\hat{\mathbf{z}}$ apparatus splits the beam into $S_z+$ and $S_z-$.
    2. Block the $S_z-$ beam.
    3. Send the $S_z+$ beam into **another** SG$\hat{\mathbf{z}}$ apparatus.
    4. **Result:** The second magnet produces only one beam—the $S_z+$ beam. This makes sense: if an atom is spin up, it stays spin up (unless something messes with it).

* **Case 2: $z$-magnet then $x$-magnet (Figure 1.3b)**
    1. First, an SG$\hat{\mathbf{z}}$ apparatus selects an $S_z+$ beam.
    2. This pure $S_z+$ beam is then sent into an SG$\hat{\mathbf{x}}$ apparatus (magnetic field in the $x$-direction).
    3. **Result:** The SG$\hat{\mathbf{x}}$ apparatus splits the beam into **two** components of equal intensity: one $S_x+$ and one $S_x-$.

    This is puzzling. It seems that the $S_z+$ beam is actually a mixture of atoms that are both $S_x+$ *and* $S_x-$. But wait, it gets worse.

* **Case 3: $z$-magnet, then $x$-magnet, then another $z$-magnet (Figure 1.3c) — The Mind-Bender**
    1. Start with an SG$\hat{\mathbf{z}}$ apparatus, block the $S_z-$ beam, so only $S_z+$ atoms go forward.
    2. Send this $S_z+$ beam into an SG$\hat{\mathbf{x}}$ apparatus. As before, it splits into $S_x+$ and $S_x-$.
    3. **Now, block the $S_x-$ beam** and let only the $S_x+$ beam enter a **third** apparatus, which is another SG$\hat{\mathbf{z}}$.
    4. **Result:** The third SG$\hat{\mathbf{z}}$ apparatus splits the beam again into **two** components: an $S_z+$ beam *and* an $S_z-$ beam!

    How can this be? We had carefully removed all $S_z-$ atoms at the very beginning. The $S_x+$ beam was made purely from $S_z+$ atoms, so how did $S_z-$ atoms suddenly reappear?

✅ **The Second Big Idea: Incompatible Observables**

This experiment demonstrates a core principle of quantum mechanics: **You cannot simultaneously know both the $S_z$ and $S_x$ components of an atom's spin with certainty.** The act of measuring $S_x$ (by the second magnet) completely "scrambles" any previous information about $S_z$. After the $S_x$ measurement, the atom is in a state with a definite $S_x$, but its $S_z$ becomes completely uncertain—it has a 50% chance of being up and 50% chance of being down. That's why the third magnet splits the beam again.

This is not due to experimental clumsiness; it's a fundamental limitation of nature.

### 1.1.3 A Helpful Analogy: Polarized Light

This behavior seems strange, but it's mathematically similar to a classical phenomenon: polarized light.

* **Correspondence:**
  * $S_z+$ and $S_z-$ atoms ↔ $x$-polarized and $y$-polarized light beams.
  * $S_x+$ and $S_x-$ atoms ↔ light beams polarized at $+45^\circ$ ($x'$) and $-45^\circ$ ($y'$).

* **The Light Experiment (Figure 1.4):**
    1. Send unpolarized light through an **$x$-polarizing filter**. Only $x$-polarized light comes out.
    2. Send this $x$-polarized light through a **$y$-polarizing filter**. No light comes out—just like putting an $S_z+$ beam through another $z$-magnet.
    3. Now, insert a **$45^\circ$ ($x'$) filter** between the $x$ and $y$ filters. Surprisingly, light now comes out of the final $y$ filter! The $x'$ filter "rescues" the light, and some of it can now pass the $y$ filter. This is directly analogous to the three-magnet experiment: the middle $x'$ filter (like the SG$\hat{\mathbf{x}}$ magnet) changes the situation so that $y$-polarized light (like $S_z-$ atoms) can appear at the end.

* **The Mathematical Connection:**
    How do we describe a light beam polarized at $45^\circ$? It's a **superposition** (a combination) of $x$ and $y$ polarizations:
    $$ \hat{\mathbf{x}}' = \frac{1}{\sqrt{2}}\hat{\mathbf{x}} + \frac{1}{\sqrt{2}}\hat{\mathbf{y}} $$
    $$ \hat{\mathbf{y}}' = -\frac{1}{\sqrt{2}}\hat{\mathbf{x}} + \frac{1}{\sqrt{2}}\hat{\mathbf{y}} $$

💡 **The Leap to Quantum States**

This suggests that the spin states of an atom can also be represented as vectors in an abstract space. We can represent the state "$S_x+$" as a combination of the two base states "$S_z+$" and "$S_z-$":

$$ |S_x; +\rangle \stackrel{?}{=} \frac{1}{\sqrt{2}} |S_z; +\rangle + \frac{1}{\sqrt{2}} |S_z; -\rangle $$
$$ |S_x; -\rangle \stackrel{?}{=} -\frac{1}{\sqrt{2}} |S_z; +\rangle + \frac{1}{\sqrt{2}} |S_z; -\rangle $$

The symbols like $|S_z; +\rangle$ are called **kets**, and they represent the quantum state of the atom.

But what about $S_y$ states? To represent them, we need to use **complex numbers**. Just as circularly polarized light (right-handed) can be represented using the imaginary number $i$:
$$ \epsilon_{\text{right}} = \frac{1}{\sqrt{2}}\hat{\mathbf{x}} + \frac{i}{\sqrt{2}}\hat{\mathbf{y}} $$
We can represent $S_y+$ and $S_y-$ states with complex coefficients:
$$ |S_y; \pm\rangle = \frac{1}{\sqrt{2}}|S_z; +\rangle \pm \frac{i}{\sqrt{2}}|S_z; -\rangle $$

This shows that the vector space for quantum states must be a **complex vector space**.

📌 **Summary of Section 1.1:**

* The Stern-Gerlach experiment proves that spin components are **quantized** (only two possible values).
* Sequential SG experiments reveal that some quantum properties (like $S_z$ and $S_x$) are **incompatible**—precise knowledge of one forbids precise knowledge of the other.
* The behavior of quantum states is analogous to polarized light, suggesting that states can be represented as vectors (**kets**) in a complex vector space. A state like $S_x+$ is a **superposition** of $S_z+$ and $S_z-$.

## 1.2 The Mathematical Toolbox: Kets, Bras, and Operators

The Stern-Gerlach experiment forces us to describe quantum states as vectors in a complex vector space. To work with these ideas, we need a precise mathematical language. The notation we use was developed by Paul Dirac and is called **bra-ket notation**.

### 1.2.1 Ket Space: Where States Live

* **The State Ket $|\alpha\rangle$:** A physical state (e.g., a silver atom with spin up along $z$) is represented by a vector called a **ket**, denoted as $|\alpha\rangle$. This ket contains *all* the information about that state.
* **Key Properties:**
  * Kets can be added: $|\alpha\rangle + |\beta\rangle = |\gamma\rangle$.
  * Kets can be multiplied by complex numbers: $c|\alpha\rangle$, where $c$ is complex.
  * **Important Physics Rule:** The kets $|\alpha\rangle$ and $c|\alpha\rangle$ (with $c \neq 0$) represent the **same physical state**. Only the "direction" of the ket matters, not its "length." (Mathematicians call this a "ray.")
* **Eigenkets:** For an operator $A$ (which represents an observable like $S_z$), there are special kets called **eigenkets**, denoted $|a'\rangle$, $|a''\rangle$, etc., that satisfy:
    $$ A|a'\rangle = a'|a'\rangle $$
    Here, $a'$ is a number called the **eigenvalue**. This equation means that when the operator $A$ acts on its eigenket $|a'\rangle$, it simply returns the same ket multiplied by the eigenvalue $a'$. The state $|a'\rangle$ has a well-defined value $a'$ for the observable $A$.
  * *Example:* For the $S_z$ operator, the eigenkets are $|S_z; +\rangle$ and $|S_z; -\rangle$, with eigenvalues $+\hbar/2$ and $-\hbar/2$:
        $$ S_z|S_z; +\rangle = \frac{\hbar}{2} |S_z; +\rangle $$
        $$ S_z|S_z; -\rangle = -\frac{\hbar}{2} |S_z; -\rangle $$

* **Completeness:** The eigenkets of an observable like $S_z$ form a **complete set**. This means that *any* possible spin state $|\alpha\rangle$ of the atom can be written as a unique combination (a **superposition**) of these eigenkets:
    $$ |\alpha\rangle = \sum_{a'} c_{a'}|a'\rangle $$
    where $c_{a'}$ are complex numbers.

### 1.2.2 Bra Space and Inner Products: Finding the "Length" and "Angle"

For every ket $|\alpha\rangle$, there is a corresponding "dual" vector called a **bra**, denoted $\langle\alpha|$. The bra space is the mirror image of the ket space.

* **Dual Correspondence (DC):** The correspondence between a ket and its bra involves complex conjugation.
    $$ |\alpha\rangle \xleftrightarrow{\text{DC}} \langle\alpha| $$
    $$ c|\alpha\rangle \xleftrightarrow{\text{DC}} c^{*}\langle\alpha| $$
    (If you multiply a ket by a complex number $c$, its corresponding bra is multiplied by $c^{*}$, the complex conjugate.)

* **Inner Product $\langle\beta|\alpha\rangle$:** This is the "product" of a bra and a ket, and it's always a (complex) number. It's analogous to the dot product in ordinary vector math. Think of it as a way to see how much one state "overlaps" with another.
  * **Property 1:** $\langle\beta|\alpha\rangle = \langle\alpha|\beta\rangle^{*}$ (Swapping the order gives the complex conjugate).
  * **Property 2:** $\langle\alpha|\alpha\rangle \ge 0$. This is a real number and is zero only if $|\alpha\rangle$ is a null ket (which represents no physical state). This is crucial for probability.

* **Normalization and Orthogonality:**
  * **Normalization:** We usually work with **normalized** kets, where $\langle\alpha|\alpha\rangle = 1$. This is like setting the "length" of our state vector to 1.
  * **Orthogonal:** Two kets are orthogonal if their inner product is zero: $\langle\alpha|\beta\rangle = 0$. This means the states are completely distinct and have no overlap, like the $S_z+$ and $S_z-$ states.

### 1.2.3 Operators: How We Change States and Represent Measurements

An **operator** (like $X$) acts on a ket from the left to produce a new ket: $X|\alpha\rangle = |\gamma\rangle$.

* **Linearity:** Operators in quantum mechanics are linear:
    $$ X(c_{\alpha}|\alpha\rangle + c_{\beta}|\beta\rangle) = c_{\alpha}X|\alpha\rangle + c_{\beta}X|\beta\rangle $$
* **Operators Acting on Bras:** An operator can also act on a bra from the right: $\langle\alpha|X$ produces a new bra.
* **Hermitian Adjoint $X^{\dagger}$:** This is the operator's "dual" counterpart. The bra dual to $X|\alpha\rangle$ is $\langle\alpha|X^{\dagger}$.
    $$ X|\alpha\rangle \xleftrightarrow{\text{DC}} \langle\alpha|X^{\dagger} $$
* **Hermitian Operator:** An operator is **Hermitian** if it is equal to its own adjoint: $X = X^{\dagger}$. These operators are vital because they represent **observables** (like $S_z$, position, momentum). A key theorem states that Hermitian operators have **real eigenvalues**, which is essential because measurement results are real numbers.

### 1.2.4 Multiplication and the Associative Axiom

* **Multiplication:** Operators can be multiplied ($XY$). Operator multiplication is generally **not commutative** ($XY \neq YX$), but it is associative ($X(YZ) = (XY)Z$).
* **Outer Product $|\beta\rangle\langle\alpha|$:** This is an important type of multiplication between a ket and a bra. Unlike the inner product (bra-ket), which is a number, the outer product (ket-bra) is an **operator**.
* **The Associative Axiom:** This is a powerful rule that says multiplication of kets, bras, and operators is associative wherever it is legal. For example:
    $$ (|\beta\rangle\langle\alpha|) \cdot |\gamma\rangle = |\beta\rangle \cdot (\langle\alpha|\gamma\rangle) $$
    This shows that the outer product $|\beta\rangle\langle\alpha|$ acts on a ket $|\gamma\rangle$ by first calculating the number $\langle\alpha|\gamma\rangle$ and then scaling the ket $|\beta\rangle$ by that number. It "projects" $|\gamma\rangle$ onto the direction of $|\beta\rangle$.

---

## 1.3 Base Kets and Matrix Representations: Making it Concrete

The abstract vector space becomes much easier to work with when we choose a set of base kets and represent everything as matrices and column vectors.

### 1.3.1 Eigenkets of an Observable as a Basis

For a Hermitian operator $A$ (an observable), its eigenkets $\{|a'\rangle\}$ form a perfect set of base kets for our vector space.

* **Orthonormality:** These eigenkets are chosen to be **orthonormal**:
    $$ \langle a'' | a' \rangle = \delta_{a''a'} $$
    ($\delta_{a''a'}$ is the Kronecker delta symbol, which is 1 if $a'' = a'$ and 0 otherwise.)

* **Completeness (Closure):** Because any ket can be expanded in this basis, the sum of the outer products of the basis kets equals the identity operator:
    $$ \sum_{a'} |a'\rangle\langle a'| = \mathbb{1} $$
    This is an incredibly useful trick. You can insert this "identity" anywhere in an expression to simplify it.

* **Expanding a Ket:** Any arbitrary ket $|\alpha\rangle$ can be expanded as:
    $$ |\alpha\rangle = \sum_{a'} |a'\rangle\langle a'|\alpha\rangle $$
    Here, the complex numbers $\langle a'|\alpha\rangle$ are the **expansion coefficients**. They are the "coordinates" of the ket $|\alpha\rangle$ in the $|a'\rangle$ basis.

### 1.3.2 Matrix Representations

Once we have a basis $\{|a'\rangle\}$, we can represent everything as matrices and vectors.

* **Representing a Ket:** A ket $|\alpha\rangle$ is represented by a **column vector**, where each entry is its expansion coefficient in the chosen basis.
    $$ |\alpha\rangle \doteq \begin{pmatrix} \langle a^{(1)}|\alpha\rangle \\ \langle a^{(2)}|\alpha\rangle \\ \langle a^{(3)}|\alpha\rangle \\ \vdots \end{pmatrix} $$
* **Representing a Bra:** The corresponding bra $\langle\alpha|$ is represented by a **row vector**, whose entries are the complex conjugates of the ket's coefficients.
    $$ \langle\alpha| \doteq (\langle\alpha|a^{(1)}\rangle, \langle\alpha|a^{(2)}\rangle, \langle\alpha|a^{(3)}\rangle, \dots) = (\langle a^{(1)}|\alpha\rangle^{*}, \langle a^{(2)}|\alpha\rangle^{*}, \langle a^{(3)}|\alpha\rangle^{*}, \dots) $$
* **Representing an Operator $X$:** An operator is represented by a **square matrix**. The matrix element in the $a''$-th row and $a'$-th column is $\langle a''|X|a'\rangle$.
    $$ X \doteq \begin{pmatrix}
    \langle a^{(1)}|X|a^{(1)}\rangle & \langle a^{(1)}|X|a^{(2)}\rangle & \cdots \
    \langle a^{(2)}|X|a^{(1)}\rangle & \langle a^{(2)}|X|a^{(2)}\rangle & \cdots \
    \vdots & \vdots & \ddots
    \end{pmatrix} $$
* **Matrix Multiplication:** With these representations, all the abstract algebra becomes standard matrix multiplication.
  * Operator equation $Z=XY$ becomes $ \langle a''|Z|a'\rangle = \sum_{a'''} \langle a''|X|a'''\rangle \langle a'''|Y|a'\rangle $.
  * Ket equation $|\gamma\rangle = X|\alpha\rangle$ becomes $ \langle a'|\gamma\rangle = \sum_{a''} \langle a'|X|a''\rangle \langle a''|\alpha\rangle $ (a matrix times a column vector).
  * Inner product $\langle\beta|\alpha\rangle$ becomes a row vector times a column vector.

* **A Special Case: The Observable $A$ in its Own Basis**
    If we use the eigenkets of $A$ itself as the basis, the matrix representation of $A$ is beautifully simple: it's a **diagonal matrix** with its eigenvalues on the diagonal.
    $$ \langle a''|A|a'\rangle = a' \delta_{a''a'} $$
    $$ A \doteq \begin{pmatrix}
    a^{(1)} & 0 & \cdots \
    0 & a^{(2)} & \cdots \
    \vdots & \vdots & \ddots
    \end{pmatrix} $$
    This means $A$ can be written as a sum of its eigenvalues times projection operators: $A = \sum_{a'} a' |a'\rangle\langle a'|$.

### 1.3.3 Example: Spin-1/2 Systems

Let's make this concrete for the simplest quantum system: a spin-1/2 particle like our silver atom.

* **Basis Kets:** We choose the $S_z$ eigenkets as our basis. We'll use the shorthand notation $|+\rangle$ for $S_z+$ and $|-\rangle$ for $S_z-$.
  * Orthonormality: $\langle + | + \rangle = 1$, $\langle - | - \rangle = 1$, $\langle + | - \rangle = 0$.
  * Completeness: $|+\rangle\langle +| + |-|\rangle\langle -| = \mathbb{1}$.

* **Matrix Representations:**
  * **Base Kets:**
        $$ |+\rangle \doteq \begin{pmatrix} 1 \\ 0 \end{pmatrix}, \quad |-|\rangle \doteq \begin{pmatrix} 0 \\ 1 \end{pmatrix} $$
  * **$S_z$ Operator:** From $S_z = (\hbar/2)[(|+\rangle\langle +|) - (|-\rangle\langle -|)]$, its matrix is:
        $$ S_z \doteq \frac{\hbar}{2} \begin{pmatrix} 1 & 0 \\ 0 & -1 \end{pmatrix} $$
  * **Ladder Operators $S_+$ and $S_-$:** These are non-Hermitian operators that "flip" the spin.
    * $S_+ \equiv \hbar |+\rangle\langle -|$ raises spin-down to spin-up: $S_+|-\rangle = \hbar|+\rangle$.
    * $S_- \equiv \hbar |-\rangle\langle +|$ lowers spin-up to spin-down: $S_-|+\rangle = \hbar|-\rangle$.
        Their matrix representations are:
        $$ S_+ \doteq \hbar \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}, \quad S_- \doteq \hbar \begin{pmatrix} 0 & 0 \\ 1 & 0 \end{pmatrix} $$
        (We will later see that $S_{\pm} = S_x \pm iS_y$.)

📌 **Summary of Sections 1.2 and 1.3:**

* Quantum states are represented by vectors called **kets** in a complex vector space.
* **Observables** are represented by **Hermitian operators**, whose eigenvectors form a complete orthonormal basis.
* The **inner product** $\langle\beta|\alpha\rangle$ gives the overlap between states.
* The **completeness relation** $\sum |a'\rangle\langle a'| = \mathbb{1}$ is a powerful tool for calculations.
* By choosing a basis (e.g., the eigenkets of $S_z$), we can represent kets as column vectors, bras as row vectors, and operators as matrices. This turns abstract quantum mechanics into concrete linear algebra.
* The spin-1/2 system provides a perfect, simple example of this entire mathematical framework.

## References

1. J. J. Sakurai, Modern Quantum Mechanics.
2. Original Stern–Gerlach papers (1922).
