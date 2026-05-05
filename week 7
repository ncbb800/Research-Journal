# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Systems Integration + Comparative Analysis

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

This week focused on combining multiple image generation systems into a single workflow pipeline rather than testing models individually.

Models used:

black-forest-labs/FLUX.1-dev
RunDiffusion/Juggernaut-XI-v11
h94/IP-Adapter-FaceID
diffusers/stable-diffusion-xl-1.0-inpainting-0.1

Pipeline tested:

Generate initial composition using FLUX.1-dev
Refine realism using Juggernaut-XI
Apply identity preservation with IP-Adapter-FaceID
Edit specific regions with SDXL inpainting

Prompts included:

“A cinematic portrait of a futuristic explorer”
“A fantasy knight standing in rain under neon lights”
“A realistic magazine-style portrait of a scientist”

### What I Expected
(My prediction before testing)

Multi-model workflows would improve overall quality and controllability
Specialized models would outperform generalist models at specific subtasks
Pipeline complexity might introduce inconsistencies between stages

### What I Found
(Key observations — what happened?)

Pipeline outputs were generally higher quality than single-model generations
FLUX produced strong compositions, while Juggernaut improved realism and texture detail
IP-Adapter preserved facial consistency surprisingly well across edits
Inpainting allowed targeted improvements without regenerating entire images
However, style drift sometimes occurred between stages, especially when switching models trained on different datasets

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Different diffusion models are optimized for different objectives:

FLUX prioritizes composition and detail generation
Juggernaut focuses on photorealism
IP-Adapter anchors identity features
Inpainting models specialize in localized reconstruction

Combining them creates a modular system where strengths compensate for weaknesses.
However, because latent spaces differ between models, transitions are not always perfectly aligned.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Pipeline required manual intervention between stages
Style consistency was difficult to maintain across models
Testing was limited to portrait-oriented prompts

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Explore automated workflow pipelines
Test whether prompt consistency reduces style drift
Investigate iterative refinement loops

