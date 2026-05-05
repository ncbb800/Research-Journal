# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Longitudinal Testing + Controlled Variation

### How I Applied It
This week focused on testing whether diffusion systems can maintain a consistent character across multiple generations.

Models tested:

h94/IP-Adapter-FaceID
RunDiffusion/Juggernaut-XL-v9
Qwen/Qwen-Image

Created a fictional character and generated:

Portraits
Different camera angles
Different lighting conditions
Different emotional expressions
Different outfits and environments

Base character prompt:
“A young cyberpunk engineer with silver hair, glowing blue glasses, and a dark futuristic jacket.”

### What I Expected
(My prediction before testing)

IP-Adapter-FaceID would maintain facial identity most effectively
General-purpose models would struggle with long-term consistency
Outfit and lighting changes would weaken character persistence

### What I Found
(Key observations — what happened?)

IP-Adapter significantly improved facial consistency across generations
Juggernaut maintained general appearance but changed facial details between images
Qwen-Image preserved stylistic consistency well but sometimes altered age or facial structure
Emotional expressions often caused identity drift
Maintaining consistency across extreme angles remained difficult for all models

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Diffusion models generate images probabilistically rather than storing persistent object identity.
Without explicit identity conditioning, each generation is effectively a new reconstruction.

IP-Adapter improves consistency by injecting facial embedding information, helping stabilize identity representation across outputs.

However, large viewpoint or expression changes move the image outside the original conditioning distribution, increasing drift.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Did not quantitatively measure identity similarity
Limited testing across only one primary character design
No video or temporal consistency testing

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Investigate temporal consistency in sequential images
Explore AI video generation systems
Test whether reference-image datasets improve persistence
