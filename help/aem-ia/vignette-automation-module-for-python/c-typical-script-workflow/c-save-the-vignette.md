---
description: The final stage is saving the vignette.
seo-description: The final stage is saving the vignette.
seo-title: Save the Vignette
title: Save the Vignette
uuid: 2143a73c-cb75-41e3-9091-7473e2c424b0
index: y
internal: n
snippet: y
---

# Save the Vignette{#save-the-vignette}

The final stage is saving the vignette.

Before a vignette is saved to disk the automation module verifies that the vignette is correct.

If the verification process finds an error, an exception is raised in the script and the vignette is not written. If the verification process finds a warning, it is reported through the [Python warnings mechanism](http://docs.python.org/library/warnings.html).

Once the verification process approves of the vignette, the vignette is saved to disk. 
