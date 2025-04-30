## Features

### Unified Prompt

The **'Unified Prompt'** node allows you to input both your prompt and parameters within a single text area, streamlining your workflow. This eliminates the need for separate input fields.

When using the Unified Prompt node:
* Begin by typing your desired prompt text as usual.
* Then write any necessary parameters, each preceded by a double hyphen (`--`).
* Utilize the special keys CTRL+UP and CTRL+DOWN to modify the values of each parameter.

#### Parameters Supported by the Unified Prompt

| Minor image adjustments                | Description                                                                 |
|:---------------------------------------|-----------------------------------------------------------------------------|
| **`--no <text>`**                      | Specifies elements that should _not_ appear in the image. (negative prompt) |
| **`--refine <text>`**                  | Specifies elements that should be refined.                                  |
| **`--cfg-shift <number>`**             | Modifies the value of the Classifier-Free Guidance (CFG) scale.             |
| **`--image-shift <number>`**           | Modifies minor image details without altering the overall composition.      |
| **`--upscale`**                        | Enables the application of the upscaling process to the final image.        |
| Major image changes                    | Description                                                                 |
|:---------------------------------------|-----------------------------------------------------------------------------|
| **`--seed <number>`**                  | Defines a number for initializing the random generator.                     |
| **`--aspect <ratio>`**                 | Specifies the aspect ratio of the image (e.g., 16:9, 4:3).                  |
| **`--landscape`**                      | Forces landscape orientation, (ratio 3:2 by default).                       |
| **`--portrait`**                       | Forces portrait orientation, (ratio 2:3 by default).                        |
| **`--medium`**                         | Generates medium-sized images instead of the default large size.            |
| Extra parameters                       | Description                                                                 |
|:---------------------------------------|-----------------------------------------------------------------------------|
| **`--detail-level <level>`**           | Controls the level of detail applied during image refinement.               |
| **`--batch-size <number>`**            | Specifies the number of images to generate in a single batch.               |

#### Examples
`--no trees, clouds` `--refine cats ears` `--cfg-shift -1` `--image_shift 2`  
`--seed 42` `--aspect 16:9` `--portrait` `--medium-size`  
`--detail-level normal` `--batch-size 4`

_For more details on these parameters, see [docs/prompt_parameters.md](docs/prompt_parameters.md)._

### Special Ctrl Keys

The **'Unified Prompt'** node offers special control keys for simplifying parameter input and modification:

- **CTRL+RIGHT (autocomplete):** Initiate a parameter name by typing `--` followed by its beginning (e.g., `--d`). Pressing CTRL+RIGHT will automatically complete the full parameter name (e.g., `--detail-level`).
- **CTRL+UP/DOWN (over parameter value):** Increment or decrement the value associated with a parameter. For instance, if your cursor is positioned over `--seed 20` and you press CTRL+UP, the text will change to `--seed 21`.

### Predefined Styles

The **'Select Style'** node allows you to select an image style. This node injects text into the prompt and modifies sampler parameters to influence the image generation. Please note that these styles are still in development, as I am experimenting with different parameter combinations to refine them over time. Therefore, they might not always function perfectly or reflect exactly what is described here.

#### Available Styles

| Style Name           | Description                                                        |
|:---------------------|--------------------------------------------------------------------|
| `PHOTO`              | Fast photorealistic images with beautiful design.                  |
| `ULTRAPHOTO`         | Realistic images with exceptional detail and clarity.              |
| `DARKFAN80`          | Dark fantasy images with 80s cinematic style.                      |
| `LITTLE_TOY`         | Minimalist images in the style of small toys.                      |
| `COMIC_ART`          | Dynamic illustrations in comic book art style.                     |
| `PIXEL_ART`          | Pixel art images with retro and blocky details.                    |
| `COLOR_INK`          | Beautiful drawings in vibrant colorful ink style.                  |
| `REALISTIC_WAIFU_X`  | Realistic images where a woman is the main subject.                |
| `REALISTIC_WAIFU_Y`  | Realistic images where a woman is the main subject (alternative1). |
| `REALISTIC_WAIFU_Z`  | Realistic images where a woman is the main subject (alternative2). |

### CivitAI/A1111 Image Compatibility

The **'Save Image'** node embeds workflow information into the generated image. Additionally, it embeds prompt and parameter information in a format compatible with CivitAI/A1111, this enables:

  * CivitAI can read the prompt used to generate the image when uploaded.
  * A wide range of applications can access the prompt and parameters used for image generation.

