---
title: Computational Physics
date: 2024-09-28 05:00:00 +0300
math: true
image:
  path: /files/Pics/MvsP.png
  alt: Mathematica vs. Python
categories: [Physics, Computational Physics]
---
## This is a guide into learning computational skills, and a guide into my Mathematica and Python codes.

I have highlighted earlier that coding is an indispensable skill for physicists, this by no means a complete guide, but a bit of my thoughts.

## Mathematics vs. Python
The answer is _both_. The ideal scenario is to be competent in both, because both of these platforms have strengths and weaknesses that combining them leaves you with the ultimate toolbox for Physics. For example, Mathematica lacks the community-wide package support due to its closed-source nature. Python is weak for symbolic computations, no matter what Sympy fans would try to convince you otherwise. The real question is:

_if you have to pick one only, which one should you pick?_

I hate _depends_ answers, so I will give you my answer based on an educated guess about your needs. The answer is _Python_. Python is general, can be used for Physics and otherwise, and very versatile with an awesome package support. Python is also easily integrable to Physical apparatuses, and has great support in that regard. Mathematica is the answer is you are a hardcore theorist, or a mathematician. You will find Mathematica very rewarding in that regard.

## General Tips on How to Learn Coding for Physics
I am always bugged when people ask me: "What resources did u learn Python and Mathematica from?". I have no answer but ```Stack Exchange```. My methodology in learning computational skills for Physics: is by attempting to solve Physics problems with them. So, the golden advice is:

_Learn coding by attempting Physics problems_

Wasting your time into theoretical backgrounds in coding really makes no sense to me. You learn by practice, like any other language. If you embrace this method of learning, then the medium (platform) for solving Physics problems should not matter at all. You can write your code in C, because you have honed your problem-solving skills to be easily translated into a pseudo-code, whatever the platform of that code turns to be.

Here is an example of the thought process you should be having when solving a Physics problem like simulating the evolution of schrodinger's equation for some system:

1. I need to discretize my time and space, e.g., $-1\le x \le 1$ and $dx = 1e^{-2}$, $0\le t \le 1$ and $dt = 1e^{-6}$. 
2. I need to make all operators in matrix form, e.g. $\hat{H}, \hat{\frac{\partial^2}{\partial x^2}}$.
3. I need to solve schrodinger's equation for each time and space steps, and get the wavefunctions $\Psi(x,t)$ as a 2D list of my whole system of $x$ and $t$.
4. Plot whatever I want, investigate different potentials, etc.

For Mathematica, check this [term project notebook](/files/Mathematica/PhysicsTrainingNotebook.nb) prepared by Dr. Khodja, an Assistant Professor of Physics @ ```KFUPM```

## My Undergrad Projects: Mathematica

You can find all of my undergraduate Mathematica notebooks on [my github](https://github.com/ibralyousef/UnderGrad/tree/main/00_Mathematica), most of them are well documented but some are badly maintained. You can ask me about the specifics of any one of them and I will gladly help. Here is a list of some interesting ones, labeled with the level of physics knowledge you need: 

- [Intro] MathematicaHelpSession.nb: Start with this guy, a simple introduction into functions and plotting and some differential equations.
- [Mid] SwingingAtwoodMachine.nb & Lagrange-and-Density-of-State.nb: For those who studied classical mechanics, and are familiar with Lagrangian mechanics.
- [Mid] RelaxationMethod.nb: The relaxation method sor solving Laplace's equation for an electric potential.
- [Mid] Merry-Go-Round.nb: This is also for classical mechanics, understanding different frames and the coriolis effect.
- [Adv] QuantumOperatorsHS&More.nb: Intro to QM.
- [Adv] CombDeltaPotential.nb: Check [here](/files/Mathematica/CDP.pdf) for details.
- [Adv] NumericalSchrodingerEquation.nb: Says what it does. 
- [a Favorite of mine] TransferMatrixApproach.nb: Check [here](/files/Mathematica/TMA.pdf) for details.

## My Undergrad Projects: Python
For Python, I have done both Physics and Chemistry, found [here](https://github.com/ibralyousef/UnderGrad/tree/main/00_Python). The Physics ones have clear names and was mostly a part of a "Computational Physics" course, with an extra file, namely "Monte Carlo for Gamma Ray Transport.ipynb", that was a part of "Nuclear and Particle Physics" course.

As for the Chemistry part, they were a part of a phenomenal course called "Computational Chemistry" which was basically an introduction into quantum Physics simulations beyond the Hydrogen atom. Check the notebooks if you are comfortable enough with quantum physics, the notebooks were prepared by a great instructor, and should be easily readable.

## Final remarks

There aren't any.

Here are your memes of the post:

|                              .                              |                              .                              |
| :---------------------------------------------------------: | :---------------------------------------------------------: |
| <img src="/files/Memes/PS.png" height = "300" width="300" alt="Meme"/> | <img src="/files/Memes/SM.jpg" height = "291" width="291" alt="Meme"/> |
|                              .                              |                              .                              |

