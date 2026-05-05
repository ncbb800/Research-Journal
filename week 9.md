# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Adversarial Testing + Failure Analysis

### How I Applied It
This week focused on identifying systematic weaknesses in image generation systems using adversarial and contradictory prompts.

Models tested:

black-forest-labs/FLUX.1-dev
stabilityai/stable-diffusion-xl-base-1.0
Tongyi-MAI/Z-Image-Turbo

Prompts included:

“A transparent glass dragon made of fire”
“A person standing both underwater and in outer space”
“A mirror reflecting something that does not exist”
“An impossible staircase folding into itself infinitely”

Tested:

Logical consistency
Object relationships
Spatial reasoning
Abstract concept handling

### What I Expected
(My prediction before testing)

Models would struggle with paradoxical or physically impossible prompts
Larger models might handle abstraction better
Spatial contradictions would expose weaknesses in reasoning ability

### What I Found
(Key observations — what happened?)

All models struggled with logical contradictions
FLUX handled composition best but still ignored parts of impossible prompts
SDXL often simplified prompts into more familiar visual patterns
Z-Image-Turbo generated faster but produced less coherent abstract outputs
Infinite reflections, paradoxes, and recursive structures consistently caused distortions

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Diffusion models do not truly “understand” logic or physics.
They generate outputs by predicting visual patterns learned from training data distributions.

When prompts describe situations rarely or never seen in training data, models rely on approximation rather than reasoning.

This suggests diffusion systems are strong pattern generators but limited world-model reasoners.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Evaluations were subjective rather than quantitative
Adversarial prompts were manually designed
Could not test multimodal reasoning systems

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Compare image generation models with multimodal reasoning models
Investigate whether chain-of-thought prompting affects image quality
Explore structured scene generation systems
