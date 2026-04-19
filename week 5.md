# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Iterative Testing + Ablation (removing/adding components in a pipeline)

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

This week focused on image editing capabilities, using:

diffusers/stable-diffusion-xl-1.0-inpainting-0.1
black-forest-labs/FLUX.1-dev
playgroundai/playground-v2.5-1024px-aesthetic

Tasks tested:

Object removal (remove a person from an image)
Object replacement (replace a dog with a robot)
Background modification (change environment while preserving subject)

Process:

Generate base image
Apply inpainting masks
Compare outputs across models

### What I Expected
(My prediction before testing)

Inpainting models would preserve surrounding context well
Larger models like FLUX might generate more coherent edits
Complex edits (object replacement) would be harder than simple removal

### What I Found
(Key observations — what happened?)

Inpainting worked well for small localized edits, especially background fixes
Large edits (e.g., replacing main subjects) often caused inconsistencies
FLUX.1-dev produced highly coherent textures but sometimes ignored mask boundaries
SDXL inpainting preserved structure better but produced less detailed replacements
Playground v2.5 produced aesthetically pleasing results but sometimes prioritized style over accuracy

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Inpainting relies on partial conditioning, where only part of the image is constrained.
The model must:

Preserve context (unchanged regions)
Generate new content (masked regions)

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Masks were manually created (not standardized)
Did not test multi-step refinement (iterative editing loops)
Limited evaluation metrics (mostly visual inspection)

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Combine generation + editing into a pipeline
Test iterative workflows (generate → edit → refine)
Investigate consistency across multiple edits
