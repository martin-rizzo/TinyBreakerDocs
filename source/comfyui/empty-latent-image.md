# Empty latent image
Generate a new empty latent image (or batch of images) that serves as a canvas for subsequent image generation processes. The image configuration is automatically read from the provided GENPARAMS.

# Overview

## Inputs
| Name       | Type       | Description                                             |
|------------|------------|---------------------------------------------------------|
| genparams  | GENPARAMS  | Generation parameters containing configuration settings |


## Outputs
| Name       | Type   | Description                                             |
|------------|--------|---------------------------------------------------------|
| LATENT     | LATENT | Batch of empty latent images with calculated dimensions |


## Key Parameters

- **Image Dimensions:** Calculated based on `genparams.modelspec.resolution` using the scale, orientation, and aspect ratio parameters.
- **Batch Size:** From `genparams.image.batch_size` _(default is 1 if not specified)_
- **Latent Dimensions:** Calculated as `image_dim // DEFAULT_VAE_PATCH_SIZE`, adjusted to ensure the dimensions are even. _(DEFAULT_VAE_PATCH_SIZE = 8)_
- **Device:** Uses the intermediate device as specified by ComfyUI's model management.


## Notes
...Under development...
