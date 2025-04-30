## Node Installation

Ensure you have the latest version of [ComfyUI](https://github.com/comfyanonymous/ComfyUI).

### Installation via ComfyUI Manager (Recommended)

The easiest way to install the nodes is through ComfyUI Manager:

1. Open ComfyUI and click on the "Manager" button to launch the "ComfyUI Manager Menu".
2. Within the ComfyUI Manager, locate and click on the "Custom Nodes Manager" button.
3. In the search bar, type "tinybreaker".
4. Select the "ComfyUI-TinyBreaker" node from the search results and click the "Install" button.
5. Restart ComfyUI to ensure the changes take effect.

### Manual Installation

To manually install the nodes:

1. Open your preferred terminal application.
2. Navigate to your ComfyUI directory:
    cd <your_comfyui_directory>
3. Move into the **custom_nodes** folder and clone the repository:
    cd custom_nodes
    git clone https://github.com/martin-rizzo/ComfyUI-TinyBreaker

#### Windows Portable

For those using the standalone ComfyUI release on Windows:

1. Go to where you unpacked **ComfyUI_windows_portable**, you'll find your `run_nvidia_gpu.bat` file here, confirming the correct location.
2. Press **CTRL + SHIFT + RightClick** in an empty space and select "Open PowerShell window here".
3. Clone the repository into your custom nodes folder using:
    git clone https://github.com/martin-rizzo/ComfyUI-TinyBreaker .\ComfyUI\custom_nodes\ComfyUI-TinyBreaker

