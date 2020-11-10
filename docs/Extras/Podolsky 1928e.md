---
layout: post
mathjax: true
read_time: true
words_per_minute: 200
title: Boris Podolsky Extras(1928)
parent: Extras
---

# Extras on the ground breaking paper published in 1928 on Quantum mechanics paper by <em>Boris Podolsky<em>
{: .no_toc }

This section is dedicated to the readers who are super-intrested in getting their kicks by reading mathematical proofs ommitted from this [article](https://rudradevmandal.github.io/abc/docs/Blog/Podolsky%201928/).
{: .fs-6 .fw-300 }



## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Proofs for the extra interested

In this section, we will see some of the prrofs of the results that we saw before. I will try to prove the results using elementary methods, but by no means these proofs will be mathematically rigourous. 


Let us start by considering a coordinate transformation from $$(x_1,x_2,\dots,x_n)$$ to $$(x'_1,x'_2,\dots,x'_n)$$. As with any coordinate transformations, we have,

$$
\begin{align}
x_1(x'_1,x'_2,\dots,x'_n),x_2(x'_1,x'_2,\dots,x'_n),\dots,x_n(x'_1,x'_2,\dots,x'_n)
\end{align}
$$

Similarly,

$$
\begin{align}
x'_1(x_1,x_2,\dots,x_n),x'_2(x_1,x_2,\dots,x_n)\dots,x'_n(x_1,x_2,\dots,x_n)
\end{align}
$$

As each of the coordinate is a function of the other. We can write down the differentials as,

$$
\begin{align}
dx_1 &= \frac{\partial x_1}{\partial x'_1}dx'_1+\frac{\partial x_1}{\partial x'_2}dx'_2+\dots+\frac{\partial x_1}{\partial x'_n}dx'_n\nonumber\\ 
&= \frac{\partial x_1}{\partial x'_i}dx'_i\\
dx_2 &= \frac{\partial x_2}{\partial x'_i}dx'_i\\
 & =\vdots \\
dx_n &= \frac{\partial x_n}{\partial x'_i}dx'^i
\end{align}
$$

And, similarly for $$x'$$, we have,

$$
\begin{align}
dx'_1 &= \frac{\partial x'_1}{\partial x_1}dx_1+\frac{\partial x'_1}{\partial x_2}dx_2+\dots+\frac{\partial x'_1}{\partial x_n}dx_n\nonumber\\ 
&= \frac{\partial x'_1}{\partial x_i}dx_i\\
dx'_2 &= \frac{\partial x'_2}{\partial x_i}dx_i\\
& \vdotswithin{ = }\notag \\
dx'_n &= \frac{\partial x'_n}{\partial x_i}dx^i
\end{align}
$$

The above relations can be written in a more neat fashion, i.e., by using matrix notation. In matrix notation,

$$
\begin{align}\label{eq:J1}
\begin{bmatrix}
dx'_1 \\
dx'_2\\
\vdots\\
dx'_n
\end{bmatrix}
&=
\begin{bmatrix}
\frac{\partial x'_1}{\partial x_1} & \frac{\partial x'_1}{\partial x_2} & \dots & \frac{\partial x'_1}{\partial x_n}\\
\frac{\partial x'_2}{\partial x_1} & \frac{\partial x'_2}{\partial x_2} & \dots & \frac{\partial x'_2}{\partial x_n}\\
\vdots\\
\frac{\partial x'_n}{\partial x_1} & \frac{\partial x'_n}{\partial x_2} & \dots & \frac{\partial x'_n}{\partial x_n}\\
\end{bmatrix}
\begin{bmatrix}
dx_1 \\
dx_2\\
\vdots\\
dx_n
\end{bmatrix}
\end{align}
$$

and,

$$
\begin{align}\label{eq:J2}
\begin{bmatrix}
dx_1 \\
dx_2\\
\vdots\\
dx_n
\end{bmatrix}
&=
\begin{bmatrix}
\frac{\partial x_1}{\partial x'_1} & \frac{\partial x_1}{\partial x'_2} & \dots & \frac{\partial x_1}{\partial x'_n}\\
\frac{\partial x_2}{\partial x'_1} & \frac{\partial x_2}{\partial x'_2} & \dots & \frac{\partial x_2}{\partial x'_n}\\
\vdots\\
\frac{\partial x_n}{\partial x'_1} & \frac{\partial x_n}{\partial x'_2} & \dots & \frac{\partial x_n}{\partial x'_n}\\
\end{bmatrix}
\begin{bmatrix}
dx'_1 \\
dx'_2\\
\vdots\\
dx'_n
\end{bmatrix}
\end{align}
$$

From the above 2 equations, it can be easily implied that,

$$
\begin{align}
\underbrace{\begin{bmatrix}
\frac{\partial x'_1}{\partial x_1} & \frac{\partial x'_1}{\partial x_2} & \dots & \frac{\partial x'_1}{\partial x_n}\\
\frac{\partial x'_2}{\partial x_1} & \frac{\partial x'_2}{\partial x_2} & \dots & \frac{\partial x'_2}{\partial x_n}\\
\vdots\\
\frac{\partial x'_n}{\partial x_1} & \frac{\partial x'_n}{\partial x_2} & \dots & \frac{\partial x'_n}{\partial x_n}\\
\end{bmatrix}}_\text{J}
=
\begin{bmatrix}
\frac{\partial x_1}{\partial x'_1} & \frac{\partial x_1}{\partial x'_2} & \dots & \frac{\partial x_1}{\partial x'_n}\\
\frac{\partial x_2}{\partial x'_1} & \frac{\partial x_2}{\partial x'_2} & \dots & \frac{\partial x_2}{\partial x'_n}\\
\vdots\\
\frac{\partial x_n}{\partial x'_1} & \frac{\partial x_n}{\partial x'_2} & \dots & \frac{\partial x_n}{\partial x'_n}\\
\end{bmatrix}^{-1}
\end{align}
$$

The matrix on the right hand side of the above equation is called the *Jacobian* matrix, $$J$$. It is of immense importance, as you can see the role it plays in interconnecting the coordinates during a coordinate trnsformation. The information of the Jacobian is enough to do a successful coordinate transformation. From the rule of Matrices, we define the inverse of a matrix by,

$$
\begin{align}
J^{-1} = \frac{\text{Cofactors of J}}{|J|}
\end{align}
$$

Therefore, by writing down the cofactors, we arrive at a very important result,

$$
\begin{align}
\frac{\partial x'_1}{\partial x_1} &= \frac{1}{|J|}\left|\frac{\partial (x_2,x_3,\dots,x_n)}{\partial (x'_2,x'_3,\dots,x'_n)}\right|\\
\frac{\partial x'_2}{\partial x_2} &= \frac{1}{|J|}\left|\frac{\partial (x_1,x_3,\dots,x_n)}{\partial (x'_1,x'_3,\dots,x'_n)}\right|\\
& \vdotswithin{ = }\notag\\
\frac{\partial x'_n}{\partial x_n} &= \frac{1}{|J|}\left|\frac{\partial (x_1,x_3,\dots,x_{n-1})}{\partial (x'_1,x'_3,\dots,x'_{n-1})}\right|
\end{align}
$$

where, the term on the right refers to,

$$
\begin{align}
\left|\frac{\partial (x_2,x_3,\dots,x_n)}{\partial (x'_2,x'_3,\dots,x'_n)}\right| = \text{Co-factor of the term }\frac{\partial x_1}{\partial x'_1} \text{ in $J^{-1}$}. 
\end{align}
$$

From the above two equations, we can figure out the relationship between the area elements in the two coordinate systems. Hence, it follows,

$$
\begin{align}
dx_1dx_2\dots dx_n = |J| dx'_1dx'_2\dots dx'_n
\end{align}
$$

Let us find meaning in these, overwhelmingly, large number of equations(phew!). Consider the coordinate transformation, from cartesian to plane polar. So now, we have,

$$
\begin{align*}
x_1 &= x ; x_2 = y\\
x'_1 &= r ; x'_2 = \theta
\end{align*}
$$

And, the relation between the coordinates are as follows,

$$
\begin{align*}
x&=rcos(\theta) & y&=rsin(\theta)\\
r&=\sqrt{x^2 + y^2}& tan(\theta) &= \frac{y}{x}
\end{align*}
$$

So, the *Jacobian* matrix is,

$$
\begin{align}
J&=
\begin{bmatrix}
\frac{\partial x}{\partial r}  & \frac{\partial x}{\partial \theta}\\
\frac{\partial y}{\partial r} & \frac{\partial x}{\partial \theta}
\end{bmatrix}
=
\begin{bmatrix}
cos(\theta) & -rsin(\theta)\\
= sin(\theta) &  rcos(\theta)
\end{bmatrix}\\
|J| &= rcos^{2}(\theta) + rsin^{2}(\theta) = r
\end{align}
$$

So, the relationship between the area elements is,

$$
\begin{align}
dxdy &= |J|drd\theta\\
dxdy &= rdrd\theta
\end{align}
$$

We got it! This is the same area element we have been using over and over. Now, using similar set of arguments, let us try to prove some other results.

### Converting $$\nabla$$:

Converting partial differentials is very important as they include important information about the space and can be used to find the variation of any functions in the given coordinate systems. So, using the good old chain rule, we can write,

$$
\begin{align}
\frac{\partial}{\partial x_1} &= \frac{\partial x'_1}{\partial x_1}\frac{\partial}{\partial x'_1} + \frac{\partial x'_2}{\partial x_1}\frac{\partial}{\partial x'_2} + \dots+\frac{\partial x'_n}{\partial x_n}\frac{\partial}{\partial x'_n}\\
\intertext{Generalising for all n's,}
\frac{\partial}{\partial x_i} &=  \frac{\partial x'_j}{\partial x_i}\frac{\partial}{\partial x'^j}
\end{align}
$$

Multiplying both sides by $|J|$, and calculating $$\nabla.A$$,

$$
\begin{align}
\nabla.A &= \nabla_{i}.A^i = |J|\frac{\partial A^i}{\partial x_i} = |J| \frac{\partial x'_j}{\partial x_i}\frac{\partial A^i}{\partial x'^j}\\
&=   \frac{\partial}{\partial x'_j}\left(|J|A^{i}\frac{\partial x'^j}{\partial x_i}\right) - A^{i}\frac{\partial}{\partial x'_j}\left(|J|\frac{\partial x'^j}{\partial x_i}\right)
\end{align}
$$

In the above equation I have, essentially, used the rule $$JXdA = d(JXA) - Ad(JX)$$. If you expand the terms in $$\frac{\partial}{\partial x'_j}\left(|J|\frac{\partial x'_j}{\partial x_i}\right)$$, it can be easily verified that all the terms in its expansion add up to zero. Therfore we are, now, left with,

$$
\begin{align}
|J|\frac{\partial A^i}{\partial x_i}&=   \frac{\partial}{\partial x'_j}\left(|J|A\frac{\partial x'^j}{\partial x_i}\right)\\
\intertext{which implies,}
\frac{\partial A^i}{\partial x_i}&=\frac{1}{|J|}   \frac{\partial}{\partial x'_j}\left(|J|A^{i}\frac{\partial x'^j}{\partial x_i}\right)\label{eq:del}
\end{align}
$$

Defining $$A^{i}\frac{\partial x'^j}{\partial x_i} = B^j$$, as the new components of the vector $$\vec{A}$$ in the new coordinate system, leads to,

$$
\begin{align}
\frac{\partial A^i}{\partial x_i}&=\frac{1}{|J|}   \frac{\partial |J|B^j}{\partial x'_j}\label{eq:nabla}
\end{align}
$$

### Converting $$\nabla^{2}$$:
We are just one step away from calculating the form of $$\nabla^{2}$$. This operator can be written as,

$$
\begin{align}
\nabla^2u &= \frac{\partial^2u^i}{\partial x^{2}_i}\\
&= \nabla . (\nabla u)\nonumber\\
&= \nabla.\left(\frac{\partial u}{\partial x^i}\hat{e_i}\right)
\end{align}
$$

Look at \eqref{eq:del}, if we take $$A^i = \frac{\partial u}{\partial x^i}$$, then we will have,

$$
\begin{align}
A^i\frac{\partial x'^j}{\partial x_i} &= \frac{\partial u}{\partial x^i}\frac{\partial x'^j}{\partial x_i}\label{eq:A1}
\end{align}
$$

But, what is $$u$$? $$u$$ is some arbitrary function of the coordinates. Therefore, again using the chain rule, we can write,

$$
\begin{align}
\frac{\partial u}{\partial x^i} = \frac{\partial u}{\partial x'^i}\frac{\partial x'_i}{\partial x^i}\label{eq:A2}
\end{align}
$$

Substituting \eqref{eq:A2} in \eqref{eq:A1},leads us to,

$$
\begin{align}
B^j &= A^i\frac{\partial x'^j}{\partial x_i} = \frac{\partial u}{\partial x'^i}\frac{\partial x'_i}{\partial x^i}\frac{\partial x'^j}{\partial x_i}
\end{align}
$$

Soving for $$\nabla^2 u$$, by using the above expression in $$\nabla.A$$(derived in \eqref{eq:nabla}) , where $$A=\nabla u$$ , which leaves us with,

$$
\begin{align}
\nabla^2 u &= \frac{1}{|J|}\frac{\partial |J|B^j}{\partial x'_j}\\
&=  \frac{1}{|J|}\frac{\partial }{\partial x'_j}\left\{|J|\frac{\partial u}{\partial x'^i}\frac{\partial x'_i}{\partial x^k}\frac{\partial x'^j}{\partial x_k}\right\}
\end{align}
$$

Well, look closley at the above equation. You can, literally smell the metric tensor lurking around. But, it's not quite right, as we will see in a moment. Let's call the term,

$$
\begin{align}
\frac{\partial x'_i}{\partial x^k}\frac{\partial x'^j}{\partial x_k} = g^{jk}
\end{align}
$$

|The choice of notation is intentional.|

Well, Low and Behold!, here pops out the inverse of the metric tensor. It was not mentioned but $$(g_{jk})^{-1}=g^{jk}$$. And the above expression is easily proven by considering,

$$
\begin{align}
g_{jk} &= J^{T}J\\
g^{jk} &= g^{-1}_{jk} = J^{-1}(J^T)^{-1}
\end{align}
$$

If we expand the \textit{Jacobian Matrix} in the partial derivative form, we exactly get the above expression.


It is important to extract the physical meaning of these equations under all this mathematical rigmarole. We should appreciate the beauty and the deep connection between the Jacobian, the Metric or Fundamental Tensor and the geometry of the space itself. All this process was done so that physical entities must not vary with change in coordinate system. After all, a coordinate system is just a viewpoint, changing viewpoints does not change the actual physical entity.