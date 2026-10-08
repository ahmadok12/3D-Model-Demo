# Unit 3332 Studio

An interactive 3D viewer for the `pixellabs-robot-3332` model, built with three.js.

## Features
- Free orbit, zoom and pan (drag, scroll, right-drag)
- 10 tagged robot parts with numbered pins and a details panel
- Three view modes: painted finish, line drawing and X-ray
- Cross-section with an adjustable cut
- Snapshots of the current view
- Light and dark themes, works on phones

## Files
| File | What it is |
| --- | --- |
| `index.html` | The whole app (HTML, CSS, JS). three.js loads from jsDelivr. |
| `robot.json` | The model as glTF JSON, with geometry embedded as base64 |
| `baseColor_1.webp`, `normal_1.webp`, `metallicRoughness_1.webp` | PBR textures (2048×2048) |

The original 44.6 MB `.glb` was optimized to about 3 MB by resizing textures from 4096 to 2048 and converting them to WebP.

## Run locally
The page loads files with `fetch`, so it needs a web server rather than opening the file directly:

```bash
python -m http.server 8000
# then open http://localhost:8000
```

## Publish with GitHub Pages
Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)`.
