---
title: 'Pymagicc: A Python wrapper for the simple climate model MAGICC'
tags:
  - climate change
  - simple climate model
  - python-wrapper
authors:
  - name: Robert Gieseke
    orcid: 0000-0002-1236-5109
    affiliation: 1
  - name: Sven N Willner
    orcid: 0000-0001-6798-6247
    affiliation: 1, 2
  - name: Matthias Mengel
    orcid: 0000-0001-6724-9685
    affiliation: 1
affiliations:
  - name: Potsdam Institute for Climate Impact Research, 14473 Potsdam, Germany
    index: 1
  - name: University of Potsdam, 14476 Potsdam, Germany
    index: 2
date: 01 December 2017
bibliography: paper.bib
output: pdf_document
---

# Summary

Pymagicc is a Python wrapper for the Fortran-based reduced-complexity
climate carbon cycle model MAGICC [@Meinshausen2011].

MAGICC^[http://magicc.org] (Model for the Assessment of Greenhouse Gas Induced Climate Change)
is widely used in the assessment of future emissions pathways in climate policy analyses,
for example in the Fifth Assessment Report of the
Intergovernmental Panel on Climate Change [@IPCC2014]. Integrated Assessment Models (IAMs) utilize
MAGICC to model the physical aspects of climate change.
It has also been used to emulate complex
atmosphere-ocean general circulation models (AOGCM) from the Coupled
Model Intercomparison Projects^[https://cmip.llnl.gov/].

MAGICC has
been under development since the late 1980s and has a hemispherically averaged upwelling-diffusion ocean coupled to an atmosphere layer and a globally averaged carbon cycle model.

Aiming at broadening the user base of the MAGICC model, the Pymagicc tool simplifies usage of the model by integrating it into the scientific Python system.
It provides a wrapper to the MAGICC binary, released under a
Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported
License^[https://creativecommons.org/licenses/by-nc-sa/3.0/], compiled
for the Windows operating system. To enable it to run under Linux and macOS the
Wine^[https://www.winehq.org/] compatibility layer is used in Pymagicc.

Pymagicc facilitates comparisons with other recently
published simple climate models written in Python, such as
@Gasser2017, @Willner17, and @Millar2017.
The emissions scenarios used as input to Pymagicc
use DataFrames from the Pandas library [@McKinney2010] as a data structure to enable
quick creation and modification of scenarios.
Pymagicc utilizes the f90nml^[https://github.com/marshallward/f90nml] library to read and write MAGICC configuration and output files in the Fortran Namelist format.
All MAGICC model parameters can be modified through Pymagicc.

Pymagicc can be installed using `pip` from the Python Package Index ^[<https://pypi.python.org/pypi/pymagicc>].
Source code, usage documentation and issue tracker are available in Pymagicc's GitHub
repository^[<https://github.com/openclimatedata/pymagicc>].
Usage examples are also contained in the repository as a Jupyter Notebook [@Perez2007; @Kluyver2016]. Thanks to the Binder project^[<https://mybinder.org/>], the example
Notebook can also be run interactively and explored without having to locally install Pymagicc.

# References