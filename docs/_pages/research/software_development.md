---
title: Software Development for Computational Chemistry
layou: single
toc: true
permalink: /research/software_development/
---

Research in this topic area revolves around making the development of new 
theoretical chemistry methods a more pleasant experience.

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

So why do we care how much technical debt a code has? TODO: Finish me!

Generally speaking 

# SimDE

{% include figure image_path="/assets/images/research/simde.png"
                  caption="SimDE allows NWChemEx to be built around a 
                           separations of concerns" 
%}


# PluginPlay

{% include figure image_path="/assets/images/research/pt_vs_module.png"
                  caption="PluginPlay facilitates plugin-based development by
                           using modules and property types."
%}

# Research Questions

- How much can we leverage PluginPlay to automate software development?

- Can we get implementing a newly derived theory to an afternoon's worth of
  coding?