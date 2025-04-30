
# Model Files  
TinyBreaker consists of two core components: the diffusion model and the text encoder. These files are essential for generating high-quality images and interpreting textual prompts.  

## Safetensors Files  
### Diffusion Model  
**tinybreaker_prototype0.safetensors (3.0 GB)**  
This is the primary diffusion model file for TinyBreaker. It contains all the necessary weights for generating high-resolution images. The model is optimized for performance and serves as the main generator in the pipeline.  

### Text Encoder  
**t5xxl_fp8_e4m3fn.safetensors (4.9 GB)**  
This model functions as a **text encoder**, transforming textual prompts into numerical embeddings that guide image generation. It is the classic T5 encoder used in various other generative models such as FLUX and SD3.5.  

---  
## Using TinyBreaker in ComfyUI  
To integrate TinyBreaker with **ComfyUI**, follow these steps:  

### 1. Core Model Configuration  
- **File Location:** Place `tinybreaker_prototype0.safetensors` in `<your-comfyui-dir>/models/checkpoints`.  
- **Purpose:** This directory is the standard location for diffusion models in ComfyUI.  

### 2. Text Encoder Configuration  
- **File Location:** Place `t5xxl_fp8_e4m3fn.safetensors` in either `<your-comfyui-dir>/models/clip` or `<your-comfyui-dir>/models/text_encoders`.  
- **Note:** While both directories are valid, `clip` is the legacy location for text encoders in ComfyUI.  

### 3. Verification  
Ensure the file paths match your ComfyUI installation to avoid errors during execution. Double-check directory permissions and file integrity if issues arise.  

---  
## Notes  
- All files are in **Safetensors** format, which is recommended for stability and compatibility.  
- Always back up your ComfyUI configuration before adding new models.