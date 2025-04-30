
# Model Files  

TinyBreaker consists of two core components: the diffusion model and the text encoder. These files are essential for generating high-quality images and interpreting textual prompts.  

## Safetensors

### Diffusion Model  

**[tinybreaker_prototype0.safetensors](https://civitai.com/models/1213728) (3.0 GB)**  
This is the primary **diffusion model** file for TinyBreaker. It contains all the necessary weights for sub-models required to generate high-resolution images. The sub-models are optimized for performance and serve as the base and refiner generator in the pipeline.  

### Text Encoder  

**[t5xxl_fp8_e4m3fn.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/text_encoders/t5xxl_fp8_e4m3fn.safetensors) (4.9 GB)**  
This model functions as a **text encoder**, transforming textual prompts into numerical embeddings that guide image generation. It is the classic T5 encoder used in various other generative models such as FLUX and SD3.5.  

---  

## Installing in ComfyUI  
To use **TinyBreaker** in ComfyUI, you must first install the corresponding **[custom nodes](https://github.com/martin-rizzo/ComfyUI-TinyBreaker)** and place the following safetensors files in the appropriate directories of your ComfyUI installation:  

- **[tinybreaker_prototype0.safetensors](https://civitai.com/models/1213728)**  
  Must be placed in the directory: `<your-comfyui-dir>/models/checkpoints`  

- **[t5xxl_fp8_e4m3fn.safetensors](https://huggingface.co/Comfy-Org/stable-diffusion-3.5-fp8/blob/main/text_encoders/t5xxl_fp8_e4m3fn.safetensors)**  
  Must be placed in either: `<your-comfyui-dir>/models/clip`  
  (or `<your-comfyui-dir>/models/text_encoders`)


### Notes  
 - Make sure to keep ComfyUI updated to the latest version.  
 - To use the upscaler, only Prototype1 has the appropriate sub-models.  
 - Verify that the file paths match your ComfyUI installation.  
 - Double-check directory permissions and file integrity if issues arise.  
