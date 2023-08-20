---
title: Software Development for Computational Chemistry
layout: splash
permalink: /research/software_development/
toc: true
feature_row:
  - title: "ParallelZone"
    url: "https://github.com/NWChemEx-Project/ParallelZone"
    excerpt: "A parallel runtime."
    btn_label: "GitHub"
    btn_class: "btn--primary"
  - title: "PluginPlay"
    image_path: /_pages/research/assets/plugin_play_logo.png
    url: "https://github.com/NWChemEx-Project/PluginPlay"
    excerpt: "Framework for writing modular software"
    btn_label: "GitHub"
    btn_class: "btn--primary"
  - title: "SimDE"
    url: "https://github.com/NWChemEx-Project/SimDE"
    excerpt: "Framework for writing modular Chemistry software"
    btn_label: "GitHub"
    btn_class: "btn--primary"
feature_row2:
  - title: "TensorWrapper"
    image_path: /_pages/research/assets/tensor_wrapper_logo.png
    url: "https://github.com/NWChemEx-Project/TensorWrapper"
    excerpt: "C++ library wrapping numerous existing tensor libraries"
    btn_label: "GitHub"
    btn_class: "btn--primary"
  - title: "Chemist"
    url: "https://github.com/NWChemEx-Project/Chemist"
    excerpt: "High-performance, C++ implementations of chemistry objects"
    btn_label: "GitHub"
    btn_class: "btn--primary"
feature_row3:
  - title: "Integrals"
    url: "https://github.com/NWChemEx-Project/Integrals"
    excerpt: >-
      NWChemEx plugin containing modules for building and transforming integrals
      in the atomic-orbital basis set.
    btn_label: "GitHub"
    btn_class: "btn--primary"  
  - title: "SCF"
    url: "https://github.com/NWChemEx-Project/SCF"
    excerpt: "NWChemEx plugin targeting self-consistent field theories."
    btn_label: "GitHub"
    btn_class: "btn--primary"
  - title: "GhostFragment"
    url: "https://github.com/rmrresearch/GhostFragment"
    excerpt: >-
      NWChemEx plugin targeting fragment-based methods and corrections for 
      basis set superposition error.
    btn_label: "GitHub"
    btn_class: "btn--primary"
---

At present many of the projects linked to are not publicly released yet. If you 
are a member of the NWChemEx-Project GitHub organization the links should take
you to the corresponding repository; if you are not, you will be unable to see
the repository. All linked projects will eventually be released as open-source
software, but development has been somewhat slow.
{: .notice--warning}

# Background

Software development in computational chemistry has a long history of 
prioritizing results over infrastructure. This means developers (often graduate 
students with little to no computer science skills) are rewarded for 
implementing working code, regardless of the code quality (as measured by
computer science metrics such as code complexity, readability, maintainability,
testability, and performance). If the code was a one-off code (not meant for 
reuse), then this would be fine; however, the vast majority of code makes its 
way into one or more established software packages. Generally speaking high
quality code does not happen by accident, and the lack of a formal development
process tends to increase the technical debt of the package (the extra cost, 
usually measured in lost developer productivity, incurred because someone chose 
an easy less robust solution). In some of the more established packages, the
prioritization of results over code quality goes back for decades and 
subsequently many packages have lifetimes of unpaid technical debt.

So why do we care how much technical debt a code has? The short answer is it
tends to decrease software sustainability (the ability for a piece of software
to persist despite new use cases, hardware, and applications). As scientists we
want to do science, but ignoring the health of the code is akin to an 
experimentalist not maintaining their instrument. More practically, you will
quickly realize that developing for a code with a large amount of technical debt
is much more time consuming than developing for one with no technical debt.

Having come up through the ranks developing for codes with varying degrees of
technical debt, Ryan is very passionate about writing good, sustainable
software. While this may seem like a lot of extra work at first, like most
things, it becomes substantially easier as you practice it.

# Research

Ryan adopts a "lazy programmer" approach to software development. The idea
being, try to avoid doing anything that you can get the computer to do for
you. Somewhat ironically this philosophy tends to require a larger upfront
development cost, as you must spend time automating tasks which you may be able
to do faster if you just implemented them manually. The problem with manually
performing tasks is that if the same task needs to be done again, then it must
again be manually done. It turns out we can actually automate fairly complicated
tasks with the right infrastructure. This brings us to the first software
development research area: frameworks.

## Frameworks

In computer science, a framework is a software package designed to facilitate
writing additional software. Usually frameworks provide a series of coarse-
grained features targeted at a specific problem. When user code needs to solve
those problems they can rely on the framework's implementations instead of
writing their own. While most frameworks are libraries, not all libraries are
frameworks. The key distinguishing feature of a framework over a library is
"inversion of control" (IOC). IOC says that the user of the framework does not
get to dictate the control flow, the framework does. While giving up control
may seem like a big concession, you do it all the time unless you are using 
your own operating system and coding language. 

The Richard group actively contributes to a number of frameworks targeting 
various problems in computational science. ParallelZone is designed to provide
a user-friendly object-oriented abstraction over low-lying parallel runtimes.
PluginPlay leverages ParallelZone to help the user write modular scientific
software. PluginPlay strives to automate as much of scientific software
development as possible so that users need only write the science. Finally,
SimDE further narrows PluginPlay's scope by introducing computational chemistry
abstractions.

{% include feature_row %}

## Chemistry Utility Libraries

In going from PluginPlay to SimDE it is necessary to introduce object-oriented
representations for concepts commonly appearing in computational chemistry.
The TensorWrapper library provides classes to facilitate creating, initializing,
and composing tensors. Tensor algebra is a key component of most methods and by
using TensorWrapper we can succintly write performant tensor code. Chemist
provides classes for common chemistry input such as molecules, atomic basis
sets, and wavefunctions. Like TensorWrapper, Chemist is designed to hide the
complexity needed to write performant chemistry objects behind a user-friendly
interface.

{% include feature_row id="feature_row2" %}

## NWChemEx Plugins

Using the chemistry-focused SimDE framework, software is implemented as a series
of plugins. Each plugin behaves a bit like an app on your smart phone. The user
is free to extend the functionality of their version of NWChemEx by installing 
new plugins or even writing their own. At present, the Richard group is heavily
involved in the development of a number of NWChemEx plugins:

{% include feature_row id="feature_row3" %}