# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Comparative analysis and adversarial testing

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

Tested several different image generation models, including the Stable Diffusion v1.5, DALL E mini/craiyon, and Latent Diffusion Image Models (SDXL). Tested prompts 
describing objects and scenes (e.g., “a futuristic city at sunset,” “a cat wearing a spacesuit”). Generated 5–10 images per prompt per model, and 
compared output quality and diversity of images

### What I Expected
(My prediction before testing)

Stable Diffusion models would produce realistic and detailed images for general prompts,
DALL·E Mini would produce creative but sometimes distorted or lower-resolution images,
Latent diffusion (SDXL) might excel at complex compositions but take longer to generate.

### What I Found
(Key observations — what happened?)

Stable Diffusion gave the most realistic and quality images for most prompts.
DALL·E Mini outputs were creative, sometimes humorous, with unusual proportions.
SDXL produced highly detailed scenes, better handling complex interactions in the scene.
All models struggled with highly conceptual and overly complicated prompts.
Style modifiers worked inconsistently; Stable Diffusion responded best, DALL·E Mini least.

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Stable Diffusion models are trained on curated datasets, allowing for better generalization.
DALL·E Mini has a smaller training dataset and less model capacity, which can cause distortions.
SDXL uses latent diffusion that captures details and complex relationships between objects.
Abstract prompts fail because models are trained primarily on image-caption pairs, not on abstract concepts.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Could not test every possible model variant on Hugging Face due to time constraints.
Only tested text-to-image prompts in English, performance in other languages unknown.
Results may differ with higher-quality prompts or with larger model checkpoints.

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Explore specialized models (e.g., anime).
Test prompt engineering techniques to improve abstract outputs.
Compare image-to-image generation capabilities.
