# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Comparative analysis and adversarial testing

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

This week focused on prompt engineering experiments using Stable Diffusion v1.5 and SDXL through Hugging Face Spaces 
and several GitHub diffusion pipelines. Instead of changing models, I varied inputs systematically: negative prompts, 
seed values, CFG scale, and prompt structure (ordering of descriptors, style tokens, and object emphasis). 
I also designed adversarial prompts intended to stress model limitations, such as “a transparent glass building made of 
water reflecting itself infinitely” and “a cat composed of smoke and electricity existing in multiple places at once.”

### What I Expected
(My prediction before testing)

I expected prompt engineering to significantly improve coherence and controllability, especially for SDXL. 
I also expected adversarial prompts to clearly expose weaknesses that were not obvious in Week 1’s baseline comparisons.

### What I Found
(Key observations — what happened?)

Prompt adjustments produced noticeable improvements in Stable Diffusion v1.5, particularly when negative prompts were used. 
SDXL showed more subtle improvements since it already handled composition well. However, both models struggled with highly paradoxical prompts, 
often collapsing into distorted structures or ignoring parts of the instruction. Seed variation had a surprisingly 
large effect on output diversity, sometimes more than changing the wording of the prompt itself. In image-to-image tests, SDXL preserved structure
and layout more consistently, while v1.5 tended to drift away from the original composition.

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Diffusion models are highly sensitive to conditioning signals, so prompt engineering can strongly influence outputs. 
However, adversarial prompts fall outside typical training distributions, causing breakdowns in learned representations.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

I could not run large-scale hyperparameter sweeps or fully systematic grid searches due to compute and time constraints.


