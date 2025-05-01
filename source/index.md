# TinyBreaker

[![CivitAI](https://img.shields.io/badge/CivitAI%3A-TinyBreaker-EEE?labelColor=1971C2&logo=c%2B%2B&logoColor=white)](https://civitai.com/models/1213728) |
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face%3A-TinyBreaker-EEE?labelColor=FFD21E&logo=huggingface&logoColor=000)](https://huggingface.co/martin-rizzo/TinyBreaker.prototype0)


![TinyBreaker](images/tinybreaker_grid.jpg)


# What is TinyBreaker?
**TinyBreaker** is a generative image model that combines the [PixArt model](https://github.com/PixArt-alpha/PixArt-sigma) for base image generation with the [Photon model](https://civitai.com/models/84728/photon) for image refinement. This hybrid approach leverages the strengths of both models, enabling efficient operation on mid-range and low-end hardware due to their low parameter count. Additionally, by running them sequentially, you can offload models to system RAM, significantly reducing VRAM usage.

In addition to all that, TinyBreaker also integrates [Tiny AutoEncoders](https://github.com/madebyollin/taesd) for latent space conversion, further optimizing performance and efficiency.  

_**Note**: While Photon is currently embedded in TinyBreaker, any SD1.5 model could be used as a refiner. SDXL models could also be used, but this would increase the parameter count, requiring more GPU resources._


## Resources
- [ComfyUI-TinyBreaker](https://github.com/martin-rizzo/ComfyUI-TinyBreaker): Nodes and workflows for ComfyUI to experiment with the model.  
- [TinyBreakerTools](https://github.com/martin-rizzo/TinyBreakerTools): Scripts I’m developing to assemble the internal models that make up the safetensors file of TinyBreaker.  
- [AbominableWorkflows](https://github.com/martin-rizzo/AbominableWorkflows): The predecessor of TinyBreaker. My first experiment combining PixArt-Sigma and Photon.  


<!--

TinyBreaker represents the natural evolution of two earlier projects:  
- **Photon Model**: A fine-tuning of SD1.5 designed to generate photorealistic and visually appealing images with minimal effort.  
- **The Abominable Workflows**: A set of ComfyUI workflows that emulated TinyBreaker’s capabilities through complex, non-standard workflows.  

---

## What is TinyBreaker?  
TinyBreaker's design leverages the PixArt model for creating a strong base image and uses either a Photon or SD1 model to refine these images. By combining their strengths, the model achieves high-quality results while minimizing computational demands.  

---

## What Makes TinyBreaker Unique?  
### Efficient Parameter Use  
TinyBreaker is notable for its low parameter count, featuring just 0.6 billion parameters in the base model. This efficiency means that high-quality image generation requires significantly fewer computational resources compared to heavier models.  

### Quick Performance  
TinyBreaker currently generates images of size 1536×1024 in approximately 10 to 15 seconds using an NVIDIA RTX 3080 GPU. Initially, the goal was always to achieve image generation in under 10 seconds, and the focus continues toward this target. Exploring new optimizations may allow meeting this objective while maintaining high quality.  

### High Prompt Adherence  
Thanks to the integration of the PixArt model, TinyBreaker achieves impressive adherence to prompts despite its minimal parameter count. This ensures that the generated images closely align with user instructions and expectations.  

---

## Limitations of TinyBreaker  
### Text Generation Challenges  
Currently, TinyBreaker faces significant challenges in producing legible text within images. Since its underlying PixArt model was not specifically trained on tasks involving detailed text generation, achieving high-quality lettering is problematic. Enhancing this capability may be difficult or nearly impossible without substantial retraining beyond simple fine-tuning.  

---

## Technical Advantages  
### Hybrid Architecture  
TinyBreaker's design combines the PixArt model for base image generation with the Photon model (or any SD1 model) for refinement. This hybrid approach balances quality and efficiency.  

### Optimized Latent Space Handling  
The use of Tiny Autoencoders for latent space conversion further enhances TinyBreaker's performance and efficiency. These autoencoders streamline the process of converting input data into meaningful images, ensuring quality while minimizing resource usage.  

---

## Future Directions  
The focus is on enhancing speed without compromising image quality. Efforts are underway to make TinyBreaker more accessible, especially for users with mid-range or lower-end hardware. Thank you for your continued support as we strive to improve. Updates will be shared soon.  

---

## Documentation  
[View full documentation](documentation.md)  
[Download models](models.md)  
[Usage guide](usage.md)  

---
-->

