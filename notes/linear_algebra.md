---
title: linear_algebra
created: 2023-02-17T17:32:30.981Z
modified: 2023-02-17T17:32:30.981Z
---

## Linear Algebra

**Accelerated Linear Algebra (XLA)** is a domain-specific compiler for linear algebra computations.
It is a component of TensorFlow. It can take advantage of special hardware like TPUs.

XLA can be used with any programming language that has an API for TensorFlow.

TensorFlow's computation graph is a language-agnostic representation of the computation graph.

**EXLA** (<https://github.com/elixir-nx/nx/tree/main/exla>) is an XLA compiler/backend for Nx.

Think about Nx as a series of compilers:

* Elixir compiler
* defn (macro) call -> change to computational graph (instead of actually computing) generating a nested AST
* that is then compiled (either JIT or properly compiled at runtime)
* then could be compiled to various targets (such as maybe LaTeX)

you can get the same AST, pass into EXLA, into XLA, compiled for the device (GPU, CPU, etc)
which would include things like tree pruning and operator fusion for efficiency

In terms of performance, the XLA-ready AST produced by Nx should be indistinguishable from XLA produced by TensorFlow/Python.

You can think of the XLA level stuff as being run as side processes, in batches, managed by the Nx/Elixir application. This may generally be more pleasant to manage in an Elixir/BEAM environment than in, say, Python.
