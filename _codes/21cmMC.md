---
title: 21cmMC
gh: 21cmFAST/21cmMC
docs: 21cmMC
caption: Figure 5 from Greig et al (2015) showing 21cmMC forecasting future experiments.
---

21cmMC uses 21cmFAST to compare observations with theory, and predict astrophysical and 
cosmological parameters. This is a beast of a process, since it must run thousands of 
cosmological simulations to generate the predictions. Thus, 21cmMC is highly parallelized 
with MPI and is geared to run on supercomputers.

21cmMC was originally written by <a href="https://github.com/BradGreig">Brad Greig</a>.
My primary role has been to integrate it with <a href="https://github.com/21cmFAST/21cmFAST">21cmFAST v3+</a>,
and to improve the interface and extensibility.
