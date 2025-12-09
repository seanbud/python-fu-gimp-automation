# python-fu-gimp-automations

> gamedev automation scripts for GIMP

## Installation

Copy scripts to your GIMP plug-ins folder:
```
Windows: C:\Users\[USER]\AppData\Roaming\GIMP\2.10\plug-ins\
Linux:   ~/.config/GIMP/2.10/plug-ins/
macOS:   ~/Library/Application Support/GIMP/2.10/plug-ins/
```

Restart GIMP. Tools appear under `Filters → Game Dev`

**Requirements:** GIMP 2.8+ with Python-Fu

---

## Tools

### tileset_slicer.py
Slice spritesheet, save into separate files.
- **Menu:** Filters → Game Dev → Slice Tileset
- **Config:** tile width/height, margin, spacing
- **Output:** `tile_0000.png`, `tile_0001.png`, ...

### normal_map_generator.py
Generate normal maps from sprites.
- **Menu:** Filters → Game Dev → Generate Normal Map (single) or Batch Normal Maps
- **Config:** strength multiplier, Y-axis inversion
- **Output:** `[name]_normal.png`

### palette_quantizer.py
Limit sprites to specific color palette.
- **Menu:** Filters → Game Dev → Quantize to Palette (single) or Batch Quantize Palette
- **Config:** palette name (must exist in GIMP), dithering method
- **Output:** `[name]_quantized.png`
- **Note:** Create or import palettes via Windows → Dockable Dialogs → Palettes

### crop-threshold-blur-export.py
Generate shadow sprites from layers.
- **Usage:** Run as Python script in GIMP console
- **Output:** `shadow_sprites/[name]_shadow.png`

### export_shadow_sprites.py
Batch export layers, optionally invert colors.
- **Usage:** Run `InvertAll()` or `ExportAll()` in GIMP console
- **Output:** `shadow_sprites/[layer_name]`

---

## Project Structure
```
python-fu/
├── tileset_slicer.py
├── normal_map_generator.py
├── palette_quantizer.py
├── crop-threshold-blur-export.py
└── export_shadow_sprites.py
```

---

**License:** MIT  
**Author:** seanbud  
**Repository:** [github.com/seanbud/python-fu-gimp-automations](https://github.com/seanbud/python-fu-gimp-automations)
