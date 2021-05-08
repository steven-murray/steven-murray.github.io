---
title: hankel
gh: steven-murray/hankel
docs: hankel
arxiv: 1906.01088
---

A small Python code that implements a way to do a very specific integral 
transform — the Hankel transform.

This transform is particularly common in astrophysics and cosmology (for instance, it is 
required to transform a correlation function into a power spectrum and vice versa). It is 
also a bit of a tricky integral to do, because it is highly oscillatory. This code 
implements a <a href="https://www.ems-ph.org/journals/show_abstract.php?issn=0034-5318&vol=41&iss=4&rank=8">neat idea</a> 
(not mine!) that is able to accurately perform this integral with
good computational performance (in most cases).
