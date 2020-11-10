---
layout: post
mathjax: true
read_time: true
words_per_minute: 200
title: Boris Podolsky (1928)
parent: Blog
---

# Breaking down the ground breaking paper published in 1928 on Quantum mechanics paper by <em>Boris Podolsky<em>
{: .no_toc }

Today, we will take a closer look on the ground breaking paper, first published in 1928, by the young Boris Podolsky while working at the University of California in Berkley.
{: .fs-6 .fw-300 }



## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## A Prelude
The problem that Podolsky was trying to solve was that of transforming the Quantum Mechanical Hamiltonian (A sophisticated terminology for the energy of the system) into other coordinates such as polar coordinate system and finding the subsequent wave equation. The difficulty was inherent in a way that we have always worked with classical systems and the order of transformation didn't really matter. But in Quantum Mechanics, the order, *really*, did matter. In a nutshell, if we wanted to make a sweet lemon juice, the order in which we mix the ingredients doesn't matter in a classical physics, but it does matter in Quantum Physics. We would get a completely different end product if we mix the order of ingredients. Now let's get to some serious business and crack this [paper](https://journals.aps.org/pr/abstract/10.1103/PhysRev.32.812).

## The Problem
Let's start our discussion with a brief review of the problem in hand. We know that, the Hamiltonian for a system can be written as,

\begin{equation}
H=T + U = E
\end{equation}

under the assumptions that, the system in question:
-  is conservative i.e., the forces are derivable from a conservative potential ($U$).[^1]
- has generalised coordinates which does not depend on time.

Only under these assumption, we can write the Hamiltonian as, 

\begin{equation}
H=T + U = E
\end{equation}

where, $E$ is the total energy of the system comprised of, $T$, the total KE and $U$, the total PE.


To convert the classical Hamiltonian into a Quantum Mechanical Hamiltonian operator, we replace the momenta, $p$, by their corresponding differential operators,

\begin{equation}
p_x\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial x} 
\end{equation}

and then write the corresponding Schr&#246;dinger wave equation,

\begin{equation}\label{eq:S}
\hat{H}\psi = E\psi 
\end{equation}

Now we use all our might to find the solution of this equation! But, what if the equations are easily solved in a different coordinate system (say $1$ and $2$), then we need to *transform* this wave equation using the transformation equations of $2$. But, as we will see in a bit,


*Classical Hamiltonian,* $H_{1} \rightarrow$ *QM Hamiltonian,* $\hat{H_{1}} \rightarrow$ *Wave eq in* $1$ $\rightarrow$ *Wave eq in* $2$ 


and,


*Classical Hamiltonian,* $H_{2} \rightarrow$ *QM Hamiltonian,* $\hat{H_{2}} \rightarrow$ *Wave eq in* $2$


These two processes does not lead to concurring equations for the wave equations. Let's see this in action with a very trivial example of a single particle in a space with no potential, and with just 2 coordinates. So, here's the plan:
- Write down the Hamiltonian in the cartesian coordinates.
- Write down its corresponding QM Hamiltonian operator and the corresponding Schr&#246;dinger wave equation.
- Transform the wave equation to the plane polar coordinates.
- Finally, repeat the process but starting, now, with the Hamiltonian directly in plane polar coordinates.


The Hamiltonian in cartesian coordinates for a single particle is given by:

\begin{equation}\label{eq:hx}
H = \frac{1}{2\mu}\left(p_{x}^{2} + p_{y}^{2} \right) 
\end{equation}

Now, replacing $p_x\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial x}$ and $p_y\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial y}$ in \eqref{eq:hx},

\begin{equation}\label{eq:Hx}
\hat{H} = \frac{-\hbar^{2}}{2\mu}\left(\frac{\partial^{2}}{\partial x^{2}} + \frac{\partial^{2}}{\partial y^{2}} \right) 
\end{equation}

The Schr&#246;dinger wave equation follows from \eqref{eq:S},

\begin{equation}\label{eq:Sx}
\frac{\partial^{2}\psi_c(x,y)}{\partial x^{2}} + \frac{\partial^{2}\psi_c(x,y)}{\partial y^{2}} + \frac{2\mu E}{\hbar^{2}}\psi_c(x,y) = 0
\end{equation}

If we, now, transform the equation \eqref{eq:Sx} to plane polar coordinates using the transformation (The exact derivation of this formula will be shown in the further sections.):

\begin{equation}
\frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2}\longrightarrow \frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial}{\partial r}\right) + \frac{1}{r^2}\left(\frac{\partial^2}{\partial \theta^2}\right)
\end{equation}

This leads us to,

\begin{equation}\label{eq:Sr1}
\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial \psi_c(r,\theta)}{\partial r}\right) + \frac{1}{r^2}\left(\frac{\partial^2 \psi_c(r,\theta)}{\partial \theta^2}\right) + \frac{2\mu E}{\hbar^{2}}\psi_c(r,\theta) = 0
\end{equation}


**_NOTE:_**  The symbols used for $\psi$ in \eqref{eq:Sx} and \eqref{eq:Sr1} are same. Subscript $c$ denotes cartesian and $r$ denotes polar.



|**_ASIDE:_**  The above statement says that, $\psi_c(x,y) = \psi_c(r,\theta)$. This is an abuse of notation, what I mean is that, I should write $\psi_c(x,y) = \psi_c(rcos(\theta),rsin(\theta))$ i.e., to say that in the function $\psi_c(x,y)$ the $x$'s are replaced by $rcos(\theta)$ and $y$'s are replaced by $rsin(\theta)$ to get $\psi_c(r,\theta)$. But, not always we know the exact functional form of the coordinates, that is why the choice of this notation.|


Once you've written the wave equation in plane polar coordinates starting from a Hamiltonian in cartesian coordinates, now it's time to start with the Hamiltonian in plane polar coordinates and, then, get to the wave equation. So, the Hamiltonian in plane polar coordinates is:

\begin{equation}\label{eq:hr}
H = \frac{1}{2\mu}\left(p_{r}^2 + \frac{1}{r^2}p_{\theta}^2\right)
\end{equation}

Now, replacing $p_r\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial r}$ and $p_{\theta}\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial \theta}$ in \eqref{eq:hr}, to get the corresponding Hamiltonian operator in plane polar coordinates:

\begin{equation}\label{eq:Hr}
\hat{H} = \frac{-\hbar^{2}}{2\mu}\left(\frac{\partial^{2}}{\partial r^{2}} + \frac{1}{r^2}\frac{\partial^{2}}{\partial y^{2}} \right) 
\end{equation}

Finally, from \eqref{eq:S}, the Schr&#246;dinger wave equation is,

\begin{equation}\label{eq:Sr2}
\frac{\partial^2 \psi_r(r,\theta)}{\partial r^2} + \frac{1}{r^2}\left(\frac{\partial^2 \psi_r(r,\theta)}{\partial \theta^2}\right) + \frac{2\mu E}{\hbar^{2}}\psi_r(r,\theta) = 0 
\end{equation}

Clearly, \eqref{eq:Sr1} and \eqref{eq:Sr2} are not same. One of the reason, which is easy to see, is the relationship between $\psi_c$ and $\psi_r$. The normalisation of $\psi_c$ and $\psi_r$ is done as follows,

\begin{equation}\label{eq:N1}
\iint \psi_c(x,y) \psi_c^{*}(x,y) dxdy = \iint \psi_c(r,\theta) \psi_c^{*}(r,\theta) rdrd\theta = 1
\end{equation}

and similarly, 

\begin{equation}\label{eq:N2}
\iint \psi_r(r,\theta) \psi_r^{*}(r,\theta) drd\theta = 1
\end{equation}

From \eqref{eq:N1} and \eqref{eq:N2} we conclude that,

\begin{equation}\label{eq:psi}
\psi_c = \frac{1}{\sqrt r} \psi_r
\end{equation}

Substituting \eqref{eq:psi} in \eqref{eq:Sr1}, gives,

\begin{equation}\label{eq:Sr3}
\left(\frac{\partial^2 \psi_r(r,\theta)}{\partial r^2}\right) +r^{-2}\left(\frac{\partial^2 \psi_r(r,\theta)}{\partial \theta^2}\right) + \left(\frac{2\mu  E}{\hbar^{2}} + \frac{r^{-2} }{4} \right)\psi_r(r,\theta) = 0 
\end{equation}

First of all, equation \eqref{eq:Sr3} is a mess. And secondly, equation \eqref{eq:Sr3}, again, is not equal to \eqref{eq:Sr2}. This leads to the, obvious, conclusion that the Hamiltonian defined in \eqref{eq:hr} is not correct. The Hamiltonian cannot be of the form as defined in \eqref{eq:hr}.

## The Solution

Having identified the problem with the form of the Hamiltonian, we need to investigate this on a more intricate level. To solve this issue, we will take a small detour towards a more geometric approach to understand coordinate systems. Once that is done, all our discussion will automaticaly lead us to the correct form of the Hamiltonian.

### A Little bit of Vector algebra!


We will see, how vectors transform\footnote{I'm using the terminology in a very sloppy manner. What I mean to say is the components of a vector.} under a coordinate transformation? Let us start with a very simple example. Consider the vector, $\vec{A} = 1\hat{e_x} + 1\hat{e_y}$.

<p align="center">
  <img src="https://raw.githubusercontent.com/rudradevmandal/abc/master/docs/Blog/podolsky_1928/1.png" alt="1" width="300"/>
</p>

The way we find the componets of the vector $\vec{A}$ is by projecting the vector length on $x-$axis and $y-$axis. So, the $x-$component is given by line projecting the tip of the vector which is parallel to the $y-$axis and similarly the $y-$component is found by projecting the tip of the vector to the $y-$axis by a line which is parallel to $x-$axis. The scalar product is given by,

\begin{equation}
\vec{A}.\vec{A} =  (1\hat{e_x} + 1\hat{e_y}).(1\hat{e_x} + 1\hat{e_y}) = \hat{e_x}.\hat{e_x} + \hat{e_y}.\hat{e_y} = 2
\end{equation}

So let's call the $x-$component of the vector $\vec{A}$ to be $A^x$ and $y-$component to be $A^y$ (*The choice of this notation will be clarified later*).


Now, let us see the same dot product in an obliqe axis coordinate. Consider the $y-$axis to be rotated clockwise by $30^o$.


**_NOTE:_**  The dot product of a vector is a scalar. It should not change with change in the coordinate system.

<p align="center">
  <img src="https://raw.githubusercontent.com/rudradevmandal/abc/master/docs/Blog/podolsky_1928/2.png" alt="2" width="300"/>
</p>

Solving for $A^{x^{'}}$ and $A^{y^{'}}$:

$$
\begin{align*}
A^{y^{'}} &=  \frac{1}{cos(30^o)} = 1.15\\
A^{x^{'}} &= 1 - \frac{cos(60^o)}{cos(30^o)} = 0.422
\end{align*}
$$

Let's calculate the scalar product:

\begin{equation}
\vec{A'}.\vec{A'} =  1.15^{2} \times \hat{e_{x'}}.\hat{e_{x'}} + 0.422^{2} \times \hat{e_{y'}}.\hat{e_{y'}} + 2 \times 1.15 \times 0.422 \times \hat{e_{x'}}.\hat{e_{y'}} = 2
\end{equation}

Well that's nice. But, is there any other way to do this? In fact, there is a more elegant way to reach this. That starts with the concept of *The Dual Vector Space*.

### Building the dual space

Let us stick to our 2-D space for now and follow it till the end. It is, just, wonderful to see that an example as simple as this can give a lot of mathematical intuition about the nature of vector spaces.


We started with the fact that the vector components of a vector is given by projecting itself parallel to the other axis. What if the projection is perpendicular? What will happen? Let's see:

<p align="center">
  <img src="https://raw.githubusercontent.com/rudradevmandal/abc/master/docs/Blog/podolsky_1928/3.png" alt="3" width="300"/>
</p>


Calculating the components $A_{x'}$ and $A_{y'}$ using trivial trignometry, gives,

$$
\begin{align*}
A_{x'} =  1.00\\
A_{y'} = 1.36
\end{align*}
$$

So, What is the use of finding these components? They do not add up to give the corresponding vector. But, that is because we have, yet, not defined the basis vectors. In the space, where components are taken by perpendicular projections, the basis vectors $\hat{e}^{x'}$ and $\hat{e}^{y'}$ must be selected such that:

1. $\hat{e}_{x'}.\hat{e}^{x'} = 1$
1. $\hat{e}_{y'}.\hat{e}^{y'} = 1$
1. $\hat{e}_{x'}.\hat{e}^{y'} = 0$

So, if you had increased the length of the basis vector $$\hat{e}_{x'}$$, then by the above rules $$\hat{e}^{x'}$$ would have to decrease, because one is the reciprocal of the other. This would lead to the corresponding component of $$\hat{e}_{x'}$$ i.e., $$A^{x'}$$ to decrease and the corresponding component of $$\hat{e}^{x'}$$ i.e., $$A_{x'}$$ to increase. Hence, their names *"Contravariant"* and *"Covariant"* vector components.(*The componets of the vector are covariant or contravariant, and not the vector itself.*)

Now, Let's calculate $\vec{A'}.\vec{\tilde{A'}}$:

$$
\begin{align*}
\vec{A'}.\vec{\tilde{A'}} &= (0.422.\hat{e}_{x'} + 1.15 \hat{e}_{y'}) . (1.\hat{e}^{x'} + 1.36.\hat{e}^{y'}) \\
								 &= 0.422.\hat{e}_{x'}.\hat{e}^{x'} + 1.578.\hat{e}_{y'}.\hat{e}^{y'} \\
								 &= 2
\end{align*}
$$

Therefore, we get the same scalar product as we got before. This is the precise way, the inner product of a vector is defined in any coordinate system. In 3D-Euclidean space we do not notice this because the space is self-dual i.e., there is no distinction between the 2 vector spaces. So, the components are exactly the same. knowingly,or, unknowningly, we have always done it. While normalisng a complex quantity, we take its conjugate, i.e., one quantity is taken from the *normal complex plane* and the other from the *dual complex plane*. So, the conjugate of a complex number exists in the dual complex vector space. The whole idea of row and coloumn vectors is based on the *dual vector spaces*. All the row vectors are a part of a *vector space* and all the column vectors are part of its *dual vector space*. That's why, we get a scalar when we multiply a row vector with a column vector. Essentially, we are calculating the dot or scalar or inner product. We do it all the time in Quantum Mechanics, when we find a scalar quantity such as $$\left\langle\phi\vert\psi\right\rangle$$ or $$\left\langle A\vert B\right\rangle$$. *Therefore, in general,* ***we always find the inner product between a vector and its dual***


Generalising this idea (*This is called the Einstein's summation convention where repeated indecies are, automatically, summed over*),

$$
\begin{align*}
\vec{A}.\vec{A} &=  A^i.\hat{e_i} . A^i.\hat{e_i} \\
					   &= (\hat{e_i} . \hat{e_j}) \times A^i . A^j  \\
					   &= g_{ij} A^i . A^j
\end{align*}
$$

This term $$g_{ij}$$ is known as the *metric tensor*, and it contains all the information about the geometry of the space we are working in. This is a very important quantity and it characterises the space or the coordinates that we are working in. It's just amazing, how much information can be extracted just by looking at this tensor. This is used everywhere, to calculate distances, areas, and differentials. And from our definition of inner product, this term is used to go back and fourth between covariant and contravariant vector components. Therefore,

$$
\begin{align*}
\vec{A}.\vec{A} &=  A_i. A^i = A_i.g^{ij}.A_j = A^i.g_{ij}.A^j
\end{align*}
$$

Let's do an example, to find the general partial derivative form of the metric tensor. Consider our good old transformation from cartesian to plane polar coordinate system, where,

$$
\begin{align*}
x = rcos(\theta)\\
y = rsin(\theta)
\end{align*}
$$

The *basis vectors* in the plane polar coordinate system can be written as[^2]:

$$
\begin{align*}
&\hat{e_r} = \left(\frac{\partial x}{\partial r},\frac{\partial y}{\partial r}\right) = (cos(\theta),sin(\theta))\\
&\hat{e_{\theta}} = \left(\frac{\partial x}{\partial \theta},\frac{\partial y}{\partial \theta}\right) = (-rsin(\theta),rcos(\theta))
\end{align*}
$$

This implies, that the metric tensor is:

$$
\begin{align*}
g_{ij} &= 
\begin{bmatrix}
\hat{e_r}.\hat{e_r} & \hat{e_r}.\hat{e_{\theta}} \\
\hat{e_{\theta}}.\hat{e_r} & \hat{e_{\theta}}.\hat{e_{\theta}}
\end{bmatrix}
=
\begin{bmatrix}
\frac{\partial x}{\partial r}.\frac{\partial x}{\partial r} + \frac{\partial y}{\partial r}.\frac{\partial y}{\partial r} & \frac{\partial x}{\partial r}.\frac{\partial x}{\partial \theta} + \frac{\partial y}{\partial r}.\frac{\partial y}{\partial \theta}\\
\frac{\partial x}{\partial \theta}.\frac{\partial x}{\partial r} + \frac{\partial y}{\partial \theta}.\frac{\partial y}{\partial r} & \frac{\partial x}{\partial \theta}.\frac{\partial x}{\partial \theta} + \frac{\partial y}{\partial \theta}.\frac{\partial y}{\partial \theta}
\end{bmatrix}\label{eq:g}\\
&= 
\begin{bmatrix}
1 & 0 \\
0 & r^2
\end{bmatrix}
\end{align*}
$$

Looking at equation \eqref{eq:g} causes $$d\acute{e}j\grave{a}$$ $$vu$$. That's right, if you stare long enough at \eqref{eq:g}, you might see a striking similarity between the *Jacobian* and the *the metric tensor*. The relation is:

$$
\begin{align*}
g = J^{T}J
\end{align*}
$$

which implies,

$$
\begin{align*}
|g| = |J|^2
\end{align*}
$$

Having found these relationships, we can now turn our attention to figuring out the differentials under coordinate transformation.This whole excercise was done to find out the differentials under a coordinate transformation. I will quote the required results in the next few lines, whose proof can be found in the last section.


If we have a transformation from $$(x_1,x_2,...,x_n)\rightarrow (x'_1,x'_2,...,x'_n)$$ then,

$$
\begin{align}\label{eq:tf1}
dx_1dx_2...dx_n = |J|dx'_1dx'_2...dx'_n = g^{\frac{1}{2}} dx'_1dx'_2...dx'_n
\end{align}
$$

|The proof is actually buried in the exterior algebra or the wedge product in vector spaces.|

For example, a transformation from $$(x,y)\rightarrow (r,\theta)$$

$$
\begin{align*}
dxdy = rdrd\theta
\end{align*}
$$

Similarly, using the \textit{Jacobian}, it can be shown that[^3],

$$
\begin{align}\label{eq:tf2}
&\frac{\partial}{\partial x^i} \rightarrow \frac{1}{|J|}\frac{\partial}{\partial x'^i}|J| = g^{-\frac{1}{2}}\frac{\partial}{\partial x'^i}g^{\frac{1}{2}}\\
&\frac{\partial}{\partial x^i}\frac{\partial}{\partial x^j} \rightarrow g^{-\frac{1}{2}}\frac{\partial}{\partial x'^i}g^{\frac{1}{2}} g_{ij} \frac{\partial}{\partial x'^j}
\end{align}
$$

We, now, have all the required tools to correct the form of the Hamiltonian.

## Correcting the Hamiltonian

The Schr&#246;dinger wave equation in cartesian coordinates with n dimensions, is:

$$
\begin{align}\label{eq:SH1}
&\frac{\partial^2 \psi_x}{\partial x^2_1} + \frac{\partial^2 \psi_x}{\partial x^2_2} + . . . + \frac{\partial^2 \psi_x}{\partial x^2_n} + \frac{2\mu E}{\hbar^2}\psi_x = 0
\end{align}
$$

Where $$\psi_x$$ is normalised as,

$$
\begin{align}\label{eq:SN1}
\int_{-\infty}^{\infty} \dots  \int_{-\infty}^{\infty} \psi_x\psi^*_x dx_1\dots dx_n = 1
\end{align}
$$

If we apply \eqref{eq:tf1} and \eqref{eq:tf2} to \eqref{eq:SH1} and \eqref{eq:SN1}, we get,

$$
\begin{align}\label{eq:SH2}
g^{-\frac{1}{2}}\frac{\partial}{\partial x'^i}g^{\frac{1}{2}}g_{ij}\frac{\partial \psi_x}{\partial x'^j} + \frac{2\mu E}{\hbar^2}\psi_x = 0
\end{align}
$$

and

$$
\begin{align}
&\int_{-\infty}^{\infty} \dots  \int_{-\infty}^{\infty} \psi_x\psi^*_x dx_1\dots dx_n = 1\\
&\int_{-\infty}^{\infty} \dots  \int_{-\infty}^{\infty} \psi_x\psi^*_x g^{\frac{1}{2}}dx'_1\dots dx'_n = 1
\end{align}
$$

also,

$$
\begin{align}
&\int_{-\infty}^{\infty} \dots  \int_{-\infty}^{\infty} \psi_{x'}\psi^*_{x'} dx'_1\dots dx'_n = 1
\end{align}
$$

Comparing the form of the integrands defined above, we can conclude that,

$$
\begin{align}\label{eq:tf3}
&\psi_x = g^{\frac{-1}{4}}\psi_{x'}
\end{align}
$$

Substituting \eqref{eq:tf3} in \eqref{eq:SH2}, gives,

$$
\begin{align}\label{eq:SH3}
\frac{1}{2\mu}g^{-\frac{1}{4}}\frac{\hbar}{i}\frac{\partial}{\partial x'^i}\left(g^{\frac{1}{2}}g_{ij}\frac{\hbar}{i}\frac{\partial}{\partial x'^j}g^{-\frac{1}{4}}\psi_x'\right) - E\psi_x' =0
\end{align}
$$

Converting the above equation into its corresponding Hamiltonian,

$$
\begin{align}\label{eq:H3}
H = \frac{1}{2\mu}g^{-\frac{1}{4}}p^i g^{\frac{1}{2}}g_{ij}p^j g^{-\frac{1}{4}}
\end{align}
$$

Classically, the above equation simplifies to,

$$
\begin{align}
H = \frac{1}{2\mu}p^i g_{ij} p^j
\end{align}
$$

In our case, the plane polar coordinates,

$$
\begin{align}
&g_{ij} = 
\begin{bmatrix}
1 & 0 \\
0 & r^2
\end{bmatrix}\\
&|g| = r^2
\end{align}
$$

The Hamiltonian, as defined in \eqref{eq:H3}, is,

$$
\begin{align}\label{eq:H4}
H = \frac{1}{2\mu}r^{-\frac{1}{2}}\left(p_r r. p_r r^{-\frac{1}{2}} + p_{\theta}r. r^{-2}p_{\theta} r^{-\frac{1}{2}}\right)
\end{align}
$$

Finding the corresponding Hamiltonian operator for the above Hamiltonian,

$$
\begin{align}
H\psi &= \frac{-\hbar^2}{2\mu}r^{-\frac{1}{2}}\left(\frac{\partial}{\partial r} r. \frac{\partial}{\partial r} r^{-\frac{1}{2}} + \frac{\partial}{\partial \theta}r. r^{-2}\frac{\partial}{\partial \theta} r^{-\frac{1}{2}}\right)\psi \\
&= \frac{-\hbar^2}{2\mu}\left(\frac{\partial^2 \psi}{\partial r^2} + r^{-2}\frac{\partial^2 \psi}{\partial \theta^2} + \frac{r^{-2} \psi}{4}\right)
\end{align}
$$

The above equation exatly matches the one in \eqref{eq:Sr3}. That means, the Hamiltonian in \eqref{eq:H4} is in Quantum-Mechanically Correct form. 

A lot of proofs are ommitted from this article to keep it concise as well as not to make the reader go bonkers while reading such heavy mathematical proofs. But, a comprehensive set of proofs can be found here. 
















---
[^1]: Goldstein H et al. Classical Mechanics. Vol. 3rd edition. Pearson, 2002, xviii, 330–339 p.
[^2]: Daniel Fleisch. A Student's Guide to Vectors and Tensors. Cambridge: Cambridge University Press, 2011, 97{157 p.
[^3]: Francis D. Murnaghan. Vector analysis and the theory of relativity (classic reprint). FORGOTTEN Books, 2015, 40{50 p. isbn: 1440094349.