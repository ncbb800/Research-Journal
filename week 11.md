# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Prototype Development + Constraint Testing

### How I Applied It
This week, I started building my second Hugging Face Space: Anime Character Consistency Generator.

The goal was to create a tool for student artists, anime creators, and storytellers who want to generate the same anime character across different scenes.

I designed the Space to take inputs such as:

character description
scene description
mood
style
seed value

I used a Gradio interface and tried to run the system on Hugging Face’s free CPU tier.

### What I Expected
(My prediction before testing)

I expected that a detailed character description and fixed seed would help the model preserve the same character identity across multiple generations.

I also expected that the Space would run slowly on CPU but still generate usable anime-style images.

### What I Found
(Key observations — what happened?)

The Space could generate anime-style images, but character consistency was unstable.

Even when I reused the same character description, the model sometimes changed:

face shape
hairstyle
eye design
clothing details
age appearance

The fixed seed helped reduce randomness, but it did not fully solve identity drift.

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Prompt-only image generation does not give the model a strong identity anchor. The model interprets the text description each time instead of remembering a persistent character.

Also, because the Space runs on free CPU, I could not efficiently use heavier identity-conditioning tools such as IP-Adapter, FaceID, or reference-image pipelines.

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

I could not run larger models smoothly on free CPU.

I also could not test advanced identity-preservation methods inside the Space because they require more compute.

The evaluation was mostly visual rather than quantitative.

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)

I want to improve the Space by adding clearer prompt templates, seed control, and side-by-side comparison outputs so users can directly observe identity drift across generations.
