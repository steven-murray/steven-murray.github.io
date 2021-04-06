---
layout: page
title: Code
permalink: /code/
feature-img: "assets/img/pexels/travel.jpeg"
tags: [Code]
---

Coding is one of my favourite parts of doing astrophysics and cosmology. 
I’ve created a fair number of scientific codes, and been involved in many more. 
Here’s a bit of a summary.

I do essentially all my coding on GitHub. To see everything I’m involved in, 
head to my profile.

## TheHaloMod

`TheHaloMod` is a web-application that uses my Python codes `hmf` and `halomod` to 
calculate halo model quantities, and serve up plots directly without ever having to 
install the codes, from the comfort of your web browser.

If you’re interested in the actual code behind `TheHaloMod`, it’s free and open-source.

The purpose of `TheHaloMod` is to be useful for both researchers and students trying to 
get into large-scale structure research. `TheHaloMod` was formerly known as `HMFcalc`, 
and has been well-used since its creation in 2013. `TheHaloMod` adds extra goodies to 
the original `HMFcalc` — namely, the ability to calculate correlation functions and 
power spectra of galaxies.

`TheHaloMod` has an associated paper describing all the calculations. Check it out!


## hmf

`hmf` is a “python application that provides a flexible and simple way to calculate the 
Halo Mass Function for a range of varying parameters.”

For the non-experts, the Halo Mass Function is a critical quantity in determining 
properties of the large-scale structure of the Universe. It encodes the number of halos 
of a given mass in a given volume of the Universe, and can be predicted from some 
fairly neat little arguments given a cosmology that describes how the Universe is 
expanding. The predictions can be used to compare to observations of galaxy clusters to 
determine parameters of the large scale structure. The HMF is also a key ingredient in 
more complex predictions of the Universe, via the halo model (see below!).

The HMF (and large-scale structure) were the topic of my PhD research at UWA, in which 
time I wrote this code. Since then, it has been widely used, and I still maintain it 
(though I work in a somewhat different field now!).

`hmf` has an associated paper describing the Halo Mass Function, and its implementation.

## halomod

`halomod` takes the ideas and implementations of hmf to the next level: it uses the HMF 
predictions as an ingredient in the halo model.

The halo model is a super-convenient analytic tool to predict the spatial distribution of 
“things” in the Universe. It uses dark matter halos as the basic scaffolding, and then 
can associate other things with the halos — eg. galaxies or diffuse gas. The predictions 
can be compared to observations of the spatial layout of galaxies, for example, to 
determine either cosmological parameters or properties of the galaxies themselves.

While I wrote the basic structure of this code during my PhD (2013-2016), I only 
published it much later (2020), in conjunction with a massive update of HMFcalc to 
`TheHaloMod`.


## hankel

`hankel` is a small Python code that implements a way to do a very specific integral 
transform — the Hankel transform.

This transform is particularly common in astrophysics and cosmology (for instance, it is 
required to transform a correlation function into a power spectrum and vice versa). It is 
also a bit of a tricky integral to do, because it is highly oscillatory. This code 
implements a neat idea (not mine!) that is able to accurately perform this integral with
good computational performance (in most cases).

The beginnings of `hankel` came together through my PhD, since I did a lot of converting 
correlation functions to power spectra. But when I changed fields to 21cm cosmology, 
I realized that the same transform is used there, and I made the package more general. 
It is now used in several fields of astronomy, and outside of astronomy too!

hankel has an associated article that presents the code in a little more detail.

## powerbox

`powerbox` is a small Python code that is all about power spectra in “boxes” of arbitrary 
dimension. It can both create boxes with a given power spectrum, or determine the power 
spectrum of a given box. It does all of this with a lot of generality — we’re not just 
talking about 2- or 3-dimensional boxes, but boxes with an arbitrary number of dimensions 
(as long as your computer has enough memory!). Bring on the 5-dimensional cubes!

`powerbox` has an associated article — check it out!

## Other Codes I Contribute To

In addition to building codes from the ground up (with the help of others in the scientific 
community, of course!), I also contribute to several other efforts — typically more 
grandiose in scale. For some of these I am a core developer or administrator, and others 
I just contribute something every now and then. Some of the Github Organizations I 
belong to are:

|---|------|
| 21cmFAST	| 21cm Cosmology simulation and inference codes. I am a core admin in this organization. |
| RadioAstronomySoftwareGroup |	Packages to aide the wider Radio Astronomy community in simulating and analysing large interferometric datasets.|
| hera-team |	Repositories to simulate and analyse data from the HERA telescope. |
| edges-collab |	Software to reduce and analyse data from the EDGES experiment.|
|---| ------|


Some key software that I play a strong role in developing:

### 21cmFAST

21cmFAST is the premiere semi-numerical 21cm cosmological simulator. It is currently 
used by every 21cm cosmology experiment to derive predictions of the spatial distribution 
of 21cm brightness temperature, to compare to observations.

I am a core developer in this project. My role has been primarily to wrap the archaic 
(but fast!) C-code of the original simulator in Python, so that it can be more widely 
and easily used. This also has the benefit of adding a number of tests so that future
development is safer and so that the code can be trusted by its many users.

The goal of wrapping the code is not trivial, and the updated package has an associated 
article to describe the implementation.

### 21cmMC

21cmMC uses 21cmFAST to compare observations with theory, and predict astrophysical and 
cosmological parameters. This is a beast of a process, since it must run thousands of 
cosmological simulations to generate the predictions. Thus, 21cmMC is highly parallelized 
with MPI and is geared to run on supercomputers.

21cmMC was originally written by Brad Greig, and I have worked on integrating it with 
the shiny new 21cmFAST.


### hera_sim

hera_sim is one of the primary codes I contribute to in the HERA software suite. It is 
geared at simulating HERA-specific instrumental effects (thermal noise, cross-coupling, 
cable reflections) and injecting them into simulated (or observed!) visibilities.

### The EDGES software suite

I am the primary developer of a new software pipeline for EDGES data. This involves data 
reading/writing (edges-io), calibration (edges-cal), analysis (edges-analysis) and 
parameter estimation (edges-estimate).

The software is developed by a small team, and I am overseeing (and contributing to) the 
development, in order to transform the EDGES analysis pipeline into something that is 
highly transparent, reproducible and accurate.