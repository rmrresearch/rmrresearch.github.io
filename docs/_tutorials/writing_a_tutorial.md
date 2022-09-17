---
title: Writing a Tutorial
---

This tutorial walks you through writing a tutorial for the website (I know
pretty meta). 

# Overview
Tutorials are written in GitHub flavored markdown and live in the 
`docs/_tutorials` directory (path is relative to the root of this git repo).


# Front Matter

Tutorials minimally need to contain YAML front matter that looks like:

```.md
---
title: Name of Your Tutorial
---
```

For example this tutorial starts with:

```.md
---
title: Writing a Tutorial
---
```

If you're not Ryan then you should add an author profile to
`_data/authors.yml` and make sure you set the tutorial author like:

```.md
---
title: Name of Your Tutorial
author: name_for_your_profile
---
```

The default author of all site content is Ryan. So if you don't take ownership 
of your tutorial then Ryan gets credit.

# Ensuring Jekyll Finds the Tutorial

If you followed the tutorial so far, simply adding a new markdown file to 
the `docs/_tutorials` directory is sufficient for Jekyll to pick it up (after 
the site has been regenerated of course).