# Research-Journal
Research Journal for AI Level 2 Research Course

### This Week's Method
(What research method did we learn in class? e.g., comparative analysis, adversarial testing)

Comparative Analysis + Systems Evaluation (performance vs efficiency)

### How I Applied It
(What did I test? What model/Space from my Collection did I use? What inputs did I try?)

This week focused on model scale and deployment efficiency, comparing:

unsloth/Z-Image-Turbo-GGUF (compressed/quantized model)
city96/FLUX.1-dev-gguf (12B quantized)
Tongyi-MAI/Z-Image-Turbo
Qwen/Qwen-Image

Tested:

Generation speed
Memory usage (approximate)
Output quality vs larger models (SDXL, FLUX)

### What I Expected
(My prediction before testing)

Smaller/quantized models would run faster but produce lower-quality images
Larger models would generate better detail but require more compute
Tradeoffs between efficiency and quality would be clearly visible

### What I Found
(Key observations — what happened?)

GGUF/quantized models ran significantly faster and used less memory
However, outputs were less detailed and sometimes less coherent
Z-Image-Turbo performed surprisingly well for speed-focused generation
FLUX-based models produced the highest quality but required more resources
Qwen-Image balanced performance and quality reasonably well

### Why I Think This Happened
(My explanation — connect it to training data, model design, domain, etc.)

Quantization reduces model precision, which:

Improves efficiency (less memory, faster inference)
Reduces representational accuracy

Larger models have:

More parameters → better pattern representation
Higher computational cost

### Limitations
(What couldn't I test? What might be different with other data/models/topics?)

Did not measure exact GPU/CPU usage quantitatively
Testing environment varied across models
No user study to evaluate perceived quality

### What I Want to Try Next
(Where is my investigation going? What question am I circling?)
