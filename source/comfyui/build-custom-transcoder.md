# Build Custom Transcoder

Builds a custom transcoder using two Variational Autoencoders (VAEs) to convert between different latent spaces. Combines source and target VAEs into an integrated transcoder with optional enhancement operations.  

# Overview

## Inputs  
| Name           | Type  | Description                                                |  
|----------------|-------|------------------------------------------------------------|  
| source_vae     | VAE   | VAE model of the source latent space (used as the decoder) |  
| target_vae     | VAE   | VAE model of the target latent space (used as the encoder) |  
| enhancer_op    | ENUM  | Operation to apply after decoding but before encoding.<br>`None`, `Auto`, `Blur` |  
| enhancer_level | FLOAT | Strength of the enhancer operation<br>(only applicable when `enhancer_op` is `Blur`) |  


## Outputs  
| Name       | Type       | Description                                              |  
|------------|------------|----------------------------------------------------------|  
| TRANSCODER | TRANSCODER | A custom transcoder combining the source and target VAEs |  


## Key Parameters  
* **Enhancer Operation:**  
  Process applied between decoding and encoding to improve output quality:  
    - **`Auto`**: Automatic mode _(apply blur by default)_  
    - **`None`**: No enhancement.  
    - **`Blur`**: Applies Gaussian blur with strength defined by **enhancer_level**.  
* **Enhancer Level:**  
  Controls the intensity of the enhancer operation.  


## Notes
...Under development...
