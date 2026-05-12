# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Failure Analysis + Research Framing

### How I Applied It
This week, I focused on analyzing the main limitation of my second Space rather than only improving the app.

I tested the same anime character description across different scenes:

classroom
rooftop at sunset
fantasy forest
futuristic city
battle scene

I kept the character description mostly the same while changing only the scene or mood.

Base character prompt:

“a silver-haired anime girl with blue eyes, a black school uniform, and a red ribbon”

### What I Expected
(My prediction before testing)

I expected that keeping the same character description would preserve most major identity features, especially hair color, eye color, and clothing.

I also expected scene changes to affect the background more than the character.

### What I Found
(Key observations — what happened?)

The system preserved some broad features, such as “silver hair” or “anime style,” but failed to maintain a stable identity.

The same character often looked like different people across scenes.

The model sometimes changed the outfit, facial structure, eye shape, or age even when the prompt stayed consistent.

This showed that prompt consistency is not the same as character consistency.


### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Text prompts describe a character category, not a unique identity.

For example, “silver-haired anime girl with blue eyes” can match many possible characters in the model’s training distribution. Without reference-image conditioning or identity embeddings, the model has no reliable way to lock onto one specific character.

This explains why lightweight CPU-based workflows struggle with persistent character generation.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

I did not use a formal similarity metric to measure identity drift.

I also tested only a small number of character designs and scenes.

The Space still depends on subjective human judgment to decide whether the character “looks the same.”

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

My next step is to build a third Space that directly compares outputs and tests possible solutions, such as:

fixed seed
stronger character templates
repeated feature locking
side-by-side generations
reference-image or identity-conditioning research

This will help turn the failure from Space 2 into a clearer research experiment.
