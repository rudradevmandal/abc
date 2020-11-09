---
layout: post
mathjax: true
read_time: true
words_per_minute: 200default
title: Boris Podolsky (1928)
parent: Blog
---

# Breaking down the ground breaking paper published in 1928 on Quantum mechanics paper by <em>Boris Podolsky<em>
{: .fs-9 }

Today we will take a closer look on the ground breaking paper, first published in 1928, by the young Boris Podolsky while working at the University of California in Berkley.
{: .fs-6 .fw-300 }


## A Prelude
The problem that Podolsky was trying to solve was that of transforming the Quantum Mechanical Hamiltonian (A sophisticated terminology for the energy of the system) into other coordinates such as polar coordinate system and finding the subsequent wave equation. The difficulty was inherent in a way that we have always worked with classical systems and the order of transformation didn't really matter. But in Quantum Mechanics, the order, *really*, did matter. In a nutshell, if we wanted to make a sweet lemon juice, the order in which we mix the ingredients doesn't matter in a classical physics, but it does matter in Quantum Physics. We would get a completely different end product if we mix the order of ingredients. Now let's get to some serious business and crack this [paper](https://journals.aps.org/pr/abstract/10.1103/PhysRev.32.812).

#
# The Problem
Let's start our discussion with a brief review of the problem in hand. We know that, the Hamiltonian for a system can be written as,

$$
H=\frac{p^2}{2m} + U
$$

under the assumptions that, the system in question:
-  is conservative i.e., the forces are derivable from a conservative potential ($U$).[^1]
- has generalised coordinates which does not depend on time.

Only under these assumption, we can write the Hamiltonian as, 

$$
H=T + U = E
$$

where, $E$ is the total energy of the system comprised of, $T$, the total KE and $U$, the total PE.


To convert the classical Hamiltonian into a Quantum Mechanical Hamiltonian operator, we replace the momenta, $p$, by their corresponding differential operators,

$$
p_x\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial x}
$$

and then write the corresponding Schr&#246;dinger wave equation,

$$
\hat{H}\psi = E\psi \label{eq:S} 
$$

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

$$
H = \frac{1}{2\mu}\left(p_{x}^{2} + p_{y}^{2} \right) \label{eq:hx}
$$

Now, replacing $p_x\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial x}$ and $p_y\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial y}$ in \eqref{eq:hx},

$$
\hat{H} = \frac{-\hbar^{2}}{2\mu}\left(\frac{\partial^{2}}{\partial x^{2}} + \frac{\partial^{2}}{\partial y^{2}} \right) \label{eq:Hx}
$$

The Schr&#246;dinger wave equation follows from \eqref{eq:S},

$$
\frac{\partial^{2}\psi_c(x,y)}{\partial x^{2}} + \frac{\partial^{2}\psi_c(x,y)}{\partial y^{2}} + \frac{2\mu E}{\hbar^{2}}\psi_c(x,y) = 0 \label{eq:Sx}
$$

If we, now, transform the equation \eqref{eq:Sx} to plane polar coordinates using the transformation (The exact derivation of this formula will be shown in the further sections.):

$$
\frac{\partial^2}{\partial x^2} + \frac{\partial^2}{\partial y^2}\longrightarrow \frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial}{\partial r}\right) + \frac{1}{r^2}\left(\frac{\partial^2}{\partial \theta^2}\right)
$$

This leads us to,

$$
\frac{1}{r}\frac{\partial}{\partial r}\left(r\frac{\partial \psi_c(r,\theta)}{\partial r}\right) + \frac{1}{r^2}\left(\frac{\partial^2 \psi_c(r,\theta)}{\partial \theta^2}\right) + \frac{2\mu E}{\hbar^{2}}\psi_c(r,\theta) = 0 \label{eq:Sr1}
$$


**_NOTE:_**  The symbols used for $\psi$ in \eqref{eq:Sx} and \eqref{eq:Sr1} are same.



|**_ASIDE:_**  The above statement says that, $\psi_c(x,y) = \psi_c(r,\theta)$. This is an abuse of notation, what I mean is that, I should write $\psi_c(x,y) = \psi_c(rcos(\theta),rsin(\theta))$ i.e., to say that in the function $\psi_c(x,y)$ the $x$'s are replaced by $rcos(\theta)$ and $y$'s are replaced by $rsin(\theta)$ to get $\psi_c(r,\theta)$. But, not always we know the exact functional form of the coordinates, that is why the choice of this notation.|


Once you've written the wave equation in plane polar coordinates starting from a Hamiltonian in cartesian coordinates, now it's time to start with the Hamiltonian in plane polar coordinates and, then, get to the wave equation. So, the Hamiltonian in plane polar coordinates is:

$$
H = \frac{1}{2\mu}\left(p_{r}^2 + \frac{1}{r^2}p_{\theta}^2\right) \label{eq:hr}
$$

Now, replacing $p_r\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial r}$ and $p_{\theta}\rightarrow \left( \frac{h}{2 \pi i} \right) \frac{\partial}{\partial \theta}$ in \eqref{eq:hr}, to get the corresponding Hamiltonian operator in plane polar coordinates:

$$
\hat{H} = \frac{-\hbar^{2}}{2\mu}\left(\frac{\partial^{2}}{\partial r^{2}} + \frac{1}{r^2}\frac{\partial^{2}}{\partial y^{2}} \right) \label{eq:Hr}
$$

Finally, from \eqref{eq:S}, the Schr&#246;dinger wave equation is,

$$
\frac{\partial^2 \psi_r(r,\theta)}{\partial r^2} + \frac{1}{r^2}\left(\frac{\partial^2 \psi_r(r,\theta)}{\partial \theta^2}\right) + \frac{2\mu E}{\hbar^{2}}\psi_r(r,\theta) = 0 \label{eq:Sr2}
$$

Clearly, \eqref{eq:Sr1} and \eqref{eq:Sr2} are not same. One of the reason, which is easy to see, is the relationship between $\psi_c$ and $\psi_r$. The normalisation of $\psi_c$ and $\psi_r$ is done as follows,

$$
\iint \psi_c(x,y) \psi_c^{*}(x,y) dxdy = \iint \psi_c(r,\theta) \psi_c^{*}(r,\theta) rdrd\theta = 1 \label{eq:N1}
$$

and similarly, 

$$
\iint \psi_r(r,\theta) \psi_r^{*}(r,\theta) drd\theta = 1 \label{eq:N2}
$$

From \eqref{eq:N1} and \eqref{eq:N2} we conclude that,

$$
\psi_c = \frac{1}{\sqrt r} \psi_r \label{eq:psi}
$$

Substituting \eqref{eq:psi} in \eqref{eq:Sr1}, gives,

$$
\left(\frac{\partial^2 \psi_r(r,\theta)}{\partial r^2}\right) +r^{-2}\left(\frac{\partial^2 \psi_r(r,\theta)}{\partial \theta^2}\right) + \left(\frac{2\mu  E}{\hbar^{2}} + \frac{r^{-2} }{4} \right)\psi_r(r,\theta) = 0 \label{eq:Sr3}
$$

First of all, equation \eqref{eq:Sr3} is a mess. And secondly, equation \eqref{eq:Sr3}, again, is not equal to \eqref{eq:Sr2}. This leads to the, obvious, conclusion that the Hamiltonian defined in \eqref{eq:hr} is not correct. The Hamiltonian cannot be of the form as defined in \eqref{eq:hr}.








---
[^1]: Goldstein H et al. Classical Mechanics. Vol. 3rd edition. Pearson, 2002, xviii, 330–339 p.