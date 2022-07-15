---
title: "Introduction for Q<sup>2</sup>Chemistry"
categories:
  - blog
tags:
  - Introduce
  - update
---

# Background Info
The advent of quantum computing technologies allows a new approach to solve quantum chemistry problems, referred to as quantum computational chemistry. In the long term, the quantum phase estimation algorithm can efﬁciently solve quantum chemistry problems with fault-tolerant quantum computers. In the short term, **variational quantum eigensolver** (VQE) provides a promising heuristic algorithm on noisy quantum computers.

**Noisy intermediate quantum** (NISQ) devices have been studied extensively to demonstrate a variaty of smallscale quantum computations. Quantum computation provides a promising pathway to solve the quantum chemistry problems.  In recent years, VQE experiments using different parametric wave function ansatzes such as the hardware efficient circuit and unitary coupled cluster (UCC) ansatz have been successfully demonstrated on contemporary and near-future quantum computers to study the ground and excited states.

# Our Work
We developed an efficient VQE simulator for quantum chemistry named Q<i>2</i>Chemistry. The package uses Python as its frontend for versatility. Connected to an ab initio quantum chemistry package such as PySCF, Q<i>2</i>Chemistry generates the qubit Hamiltonian for quantum circuit simulations. We implement several ansatzes for constructing the parametric wave function ansatz, including hardware efficient circuit, unitary coupled cluster, ADAPT algorithm and a couple of UCC-based variants. Q<i>2</i>Chemistry uses C++ and Julia-based backends for high performance quantum circuit simulation, including the matrix product state (MPS) algorithm for large scale simulations, as well as the commonly used state vector and density matrix method to perform brute-force calculations. A two-level parallelization technique is implemented for energy evaluation, and gradients of energy with respect to variational circuit parameters are efficiently calculated through the revere-mode differentiation. Our results show that Q<i>2</i>Chemistry is capable of performing VQE simulations for molecules up to 50-100 qubits at the level of chemical accuracy.


<figure>
  <img src="{{ '/assets/images/Introduce1.jpg' | relative_url }}" alt="Q2C image example">
  <figcaption>An example of the mapped circuit is present.</figcaption>
</figure>


<!-- Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/ -->
