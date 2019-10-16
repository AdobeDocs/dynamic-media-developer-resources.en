---
description: The Vignette Automation Module (s7vampy) extends Python 2.7.3 with the ability to write scripts to automate the creation, modification, and inspection of vignettes.
seo-description: The Vignette Automation Module (s7vampy) extends Python 2.7.3 with the ability to write scripts to automate the creation, modification, and inspection of vignettes.
seo-title: Scene7 Vignette Automation Module for Python
title: Scene7 Vignette Automation Module for Python
uuid: adb07726-7daf-460d-b775-ffcf524d165a
---

# Scene7 Vignette Automation Module for Python{#scene-vignette-automation-module-for-python}

The Vignette Automation Module (s7vampy) extends Python 2.7.3 with the ability to write scripts to automate the creation, modification, and inspection of vignettes.

s7vampy automates the creation of vignettes using available masks, uv texture data, and illumination.

s7vampy allows scripts to create new vignettes, add or modify global and local illumination maps, and build an object hierarchy with static objects, non-texturable objects, surface objects, flat objects, and overlapping objects.

The Python programming language can be used to write scripts or whole applications. It's an open source language that you can install directly from [http://www.python.org](http://www.python.org). It is free to use by anyone.

The primary use case for s7vampy is when you have all the necessary images and data already available to build a vignette.

For example, imagine that a jewelry retailer has rendered all the gems and jewelry assets in their 3D CAD environment using specialized render technology. They are able to automatically create the images from their 3D CAD environment so that they are ready to push it in to a vignette. However, that means that they need to use Image Authoring to manually build each vignette, and if something changes in the original asset they must build the vignette manually again. The Vignette Automation Module allows them to write a Python script that will take those images that they've created and build a vignette out of it. They could script it to process a lot of their assets without any user interaction to create the vignettes and have the vignettes ready for upload to SPS.

