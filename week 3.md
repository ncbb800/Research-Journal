## Week [3] — [Comparative Analysis and Adversarial Testing]

### This Week's Method
Comparative Analysis and Adversarial Testing

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

Tested three models from my collection:

h94/IP-Adapter-FaceID – specialized for face editing and conditioning
cagliostrolab/animagine-xl-3.1 – anime-style image generation
RunDiffusion/Juggernaut-XL-v9 – general-purpose high-resolution image generation

Prompted each model with:

“A young woman with cyberpunk makeup under neon lights”
“An anime-style cat wizard casting a spell in a forest”
“A photorealistic portrait of a smiling elderly man in natural light”

Generated 5–8 images per prompt per model and compared quality and consistency.

### What I Expected
(My prediction before testing)

IP-Adapter-FaceID would excel at facial realism and identity.
Animagine-XL would produce vibrant, accurate anime imagery.
Juggernaut-XL would generate high-quality images across multiple domains but may lack stylization.

### What I Found
(Key observations — what happened?)

IP-Adapter-FaceID produced extremely realistic faces, with consistent identity and natural lighting,
but struggled with non-human subjects or abstract backgrounds.

Animagine-XL generated vibrant, consistent anime-style characters, but proportions occasionally 
skewed and backgrounds were less detailed.

Juggernaut-XL produced high-quality images in all cases, but style consistency was weaker than specialized models.

Facial expressions and small details were most accurately represented by IP-Adapter-FaceID; 
Animagine-XL exaggerated expressions for stylistic effect.

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

IP-Adapter-FaceID is trained on datasets emphasizing human faces and identity, giving it strong performance in portrait tasks.
Animagine-XL is trained specifically on anime datasets, explaining its success in stylized art but occasional anatomical inconsistencies.
Juggernaut-XL is a generalist model,it balances quality across domains but lacks fine-grained specialization.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Only three types of prompts were tested.
Non-facial subjects tested with IP-Adapter-FaceID performed poorly, so the model is very specialized.
Anime backgrounds often lacked depth, which could be improved with prompt engineering.

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

Combine IP-Adapter-FaceID with Juggernaut-XL for hybrid portrait generation to see if stylized realism improves.
