# Mojo Optimisation Strategies

Some optimisation strategies to consider when trying to speed up Mojo code.

- Mojo is a very young language and these are likely to change.
- My explanations of why the stratigies work are probably wrong. A lot of it might come down to specific optimisations being applied by the compiler in specific situations which is not described in detail anywhere yet. And my understanding of registers, caches and other internal plumbing are probably too vague for me to reliably think about what the language is doing.
- Each optimisation strategy has a notebook to demonstrate how it works. It is somewhere between an overly complex bug report, a tutorial, and notes to myself. But it may be of interest to others also using the language.
- The general idea is to build up a checklist of things to go through. Probably sorted by magnitude of speed up and ease of application. Also writing the notebooks is making me write specific reproducers which might identify specific bugs. And over time the performance can be updated.
- General optimisations that apply in any language like reducing loops in code probably supercede any of these optimisations. Or moving expensive operations out of hot loops. I might add some of those things in the list at a point as a reminder. Generally finding and writing about more esoteric stuff is more fun though.

## Optimisation Strategies

1. [Only write the mutated field of a large struct](notebooks/specific-field-updates.ipynb)
