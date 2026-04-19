# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Comparative Analysis + Controlled Variable Testing (conditioning inputs)

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

This week focused on controlled image generation using external conditioning models, specifically:

xinsir/controlnet-union-sdxl-1.0 (ControlNet)
h94/IP-Adapter-FaceID
stabilityai/stable-diffusion-xl-base-1.0

I tested how adding structured inputs affects generation:

Edge maps (Canny)
Pose skeletons
Reference face images (FaceID)

### What I Expected
(My prediction before testing)

ControlNet would significantly improve structural consistency (pose, layout)
IP-Adapter-FaceID would strongly preserve identity in portraits
Combining conditioning methods might improve both realism and control

### What I Found
(Key observations — what happened?)

ControlNet dramatically improved pose accuracy and composition alignment, especially for human figures
However, it sometimes reduced creativity and introduced stiffness in images
IP-Adapter-FaceID consistently preserved facial identity across generations
Combining ControlNet + FaceID worked, but required careful balancing—too much conditioning caused artifacts
Without conditioning, SDXL produced more natural but less controlled outputs

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Diffusion models generate images by gradually refining noise, guided by conditioning signals.
ControlNet introduces strong spatial constraints, forcing the model to follow structure.
FaceID works by injecting identity embeddings, anchoring facial features.

However, too many constraints can over-constrain the latent space, reducing diversity and causing artifacts.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Did not systematically tune conditioning strength parameters
Limited to a few types of ControlNet inputs (edges, pose)
Did not test multi-step pipelines (e.g., ControlNet → inpainting)

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Explore inpainting and editing workflows
Test whether controlled generation improves iterative editing
Investigate how models handle partial image modification vs full generation
