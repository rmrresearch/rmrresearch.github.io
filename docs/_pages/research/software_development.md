---
title: Software Development for Computational Chemistry
layout: splash
permalink: /research/software_development/
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
---

At present many of the projects linked to are not publicly released yet. If you 
are a member of the NWChemEx-Project GitHub organization the links should take
you to the corresponding repository; if you are not, you will be unable to see
the repository. All linked projects will eventually be released as open-source
software, but development has been somewhat slow.
{: .notice--warning}

Research in software development revolves around making the development of new 
theoretical chemistry methods easier and a more pleasant experience. Generally,
speaking all of our software developments are part of the NWChemEx electronic
structure package; however, due to the modular nature of NWChemEx most of the
software is actually usable by many other packages as well.

# Background

Software development in computational chemistry has a long history of 
prioritizing results over infrastructure. This means developers (often graduate 
students with little to no computer science skills) are rewarded for 
implementing working code, regardless of the code quality (from the perspective
of computer science). If the code was a one-off code (not meant for reuse),
then this is fine; however, the vast majority of this code makes its way into
one or more established software packages increasing the technical debt of the
package (technical debt is the extra cost, usually lost developer productivity, 
incurred because someone chose an easy less robust solution). With these
practices dating back to the 1970s, in some of the more established packages,
many packages have lifetimes of unpaid technical debt.

So why do we care how much technical debt a code has? The short answer is it
tends to decrease software sustainability (the ability for a piece of software
to persist despite new use cases, hardware, and applications). 

In the Richard group we place a serious emphasis on writing good, sustainable
software. One of the ways we 

# Frameworks

{% include feature_row %}

# Chemistry Utility Libraries

{% include feature_row id="feature_row2" %}