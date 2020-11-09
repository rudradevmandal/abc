---
layout: post
mathjax: true
read_time: true
words_per_minute: 200
title: Boris Podolsky (1928)
parent: Blog
---

# Breaking down the ground breaking paper published in 1928 on Quantum mechanics paper by <em>Boris Podolsky<em>
{: .fs-9 }

Today we will take a closer look on the ground breaking paper, first published in 1928, by the young Boris Podolsky while working at the University of California in Berkley.
{: .fs-6 .fw-300 }


## A Prelude
The problem that Podolsky was trying to solve was that of transforming the Quantum Mechanical Hamiltonian (A sophisticated terminology for the energy of the system) into other coordinates such as polar coordinate system and finding the subsequent wave equation. The difficulty was inherent in a way that we have always worked with classical systems and the order of transformation didn't really matter. But in Quantum Mechanics, the order, *really*, did matter. In a nutshell, if we wanted to make a sweet lemon juice, the order in which we mix the ingredients doesn't matter in a classical physics, but it does matter in Quantum Physics. We would get a completely different end product if we mix the order of ingredients. Now let's get to some serious business and crack this [paper](https://journals.aps.org/pr/abstract/10.1103/PhysRev.32.812).

## The Problem
Let's start our discussion with a brief review of the problem in hand. We know that, the Hamiltonian for a system can be written as,

$$
H=\frac{p^2}{2m} + U \,
$$

under the assumptions that, the system in question:
-  is conservative i.e., the forces are derivable from a conservative potential.[^1]
- has generalised coordinates which does not depend on time.

Only under these assumption, we can write the Hamiltonian as, $H=T + U = E$.\
To convert the classical Hamiltonian into a Quantum Mechanical Hamiltonian operator, we replace the momenta, $p$, by their corresponding differential operators,

$$
p_x\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial x} \,
$$

and then write the corresponding Schr&#246;dinger wave equation,

$$
\hat{H}\psi = E\psi \,
$$

Now we use all our might to find the solution of this equation! But, what if the equations are easily solved in a different coordinate system, then we need to *transform* this wave equation using the transformation equations. But, as we will see in a bit,\

*Classical Hamiltonian,* $H_{1} \rightarrow$ *QM Hamiltonian,* $\hat{H_{1}} \rightarrow$ *Wave eq in* $1$ $\rightarrow$ *Wave eq in* $2$\


[^1]: Goldstein H et al. Classical Mechanics. Vol. 3rd edition. Pearson, 2002, xviii, 330–339 p.

## KaTeX

You can render LaTeX mathematical expressions using [KaTeX](https://khan.github.io/KaTeX/):

The *Gamma function* satisfying $\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N$ is via the Euler integral

$$
E = m\cdot c^2 \,
$$

$$
\Gamma(n) = (n-1)!\quad\forall n\in\mathbb N \,
$$


