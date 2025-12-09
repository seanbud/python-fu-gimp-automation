# my-gimp-automation

Automate common GIMP workflows for sprite and image processing using Python-fu scripts.

## Overview

**my-gimp-automation** is a collection of Python-fu scripts to automate repetitive GIMP tasks, especially for sprite and image manipulation. The scripts streamline processes such as cropping, thresholding, blurring, inverting, and batch exporting layers, simplifying the creation of "shadow sprite" assets and similar workflows.

## Features

- **Crop and Export:** Automatically crops images to a centered square region and exports processed layers.
- **Layer Threshold and Blur:** Applies a threshold (making the layer black) and iterative blur to each layer, then exports the results as shadow images.
- **Invert Layers:** Batch inverts all layers in the current image.
- **Batch Export:** Saves all layers or selected layers to a dedicated `shadow_sprites` subfolder.
- **Automatic Output Directory Creation:** Output directories for exported layers are created automatically if they don’t exist.

## Scripts

Located in `python-fu/`:
- `crop-threshold-blur-export.py`: Crops the image, applies threshold and blur to each layer, and saves results as `_shadow.png` files in `shadow_sprites/`.
- `export_shadow_sprites.py`: Functions for inverting all layers, exporting all layers, or exporting a specific layer by index.

## Usage

1. **Install GIMP with Python support** (`gimpfu`).
2. Copy the scripts from the `python-fu` directory into your GIMP plug-ins folder.
3. Open your image in GIMP and ensure your layers are named for intended processing.
4. Run the script(s) from the GIMP Python-fu console or assign them to menu actions as needed.

### Example

To batch export shadow sprites:
- Run `crop-threshold-blur-export.py` to process and export cropped, thresholded, blurred versions of each layer.
- Alternatively, use `export_shadow_sprites.py`:
  - Run `InvertAll()` to invert all layers.
  - Run `ExportAll()` to export all layers.

Exported files will be found in a `shadow_sprites` subfolder next to your original image.

## Requirements

- GIMP with Python-fu enabled.
- Python standard library (os module).

## Contributing

Pull requests and suggestions are welcome!
