# Cell Architecture Studio

Interactive 3D Cell Biology Explorer — built with Three.js.

## Overview

Explore 8 types of biological cells with high-fidelity 3D models, interactive organelle inspection, and educational content. Switch between code-generated models and imported GLB specimens from the [NIH 3D Print Exchange](https://3d.nih.gov).

![Screenshot](docs/screenshot.png)

## Features

- **8 Cell Types**: Plant, White Blood Cell, Neuron, Epithelial, Bacteria, Animal, Muscle, Red Blood Cell
- **High-Fidelity GLB Models**: 5 professional specimens (from NIH 3D Print Exchange and community contributions)
- **Interactive Organelle Explorer**: Click any organelle to enter Focus Mode with detailed biology info
- **Microscope Views**: Simulated Light Microscope, Stained, and Electron Microscope renderings
- **Cell Comparison**: Side-by-side comparison between cell types
- **Custom Model Import**: Drag & drop your own `.glb` / `.gltf` files
- **Code-Generated Fallback**: Cells without GLB models use procedural Three.js geometry
- **Responsive Design**: Works on desktop and mobile browsers

## Tech Stack

| Layer | Technology |
|---|---|
| 3D Rendering | Three.js r128 |
| Models | GLTFLoader (`.glb` / `.gltf`) |
| Labels | CSS2DRenderer |
| Controls | OrbitControls |
| UI | Vanilla HTML/CSS/JS |

## Quick Start

### Option 1: Open Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/3DArchitectureStudio.git
   cd 3DArchitectureStudio
   ```

2. Start a local server:
   ```bash
   # Python 3
   python -m http.server 8080
   
   # Node.js (npx)
   npx serve .
   
   # Or use any static file server
   ```

3. Open `http://localhost:8080/Cell%20Architecture%20Studio.html` in your browser.

### Option 2: GitHub Pages

1. Go to your repository **Settings > Pages**
2. Set source to **main branch / root**
3. Visit `https://yourusername.github.io/3DArchitectureStudio/`

## Model Assets

### Preloaded GLB Models

| Cell Type | File | Size | Source |
|---|---|---|---|
| Animal Cell | `models/animal-cell-nih.glb` | 1.5 MB | NIH 3D Print Exchange |
| Bacteria | `models/bacteria-wall-nih.glb` | 482 KB | NIH 3D Print Exchange |
| Neuron | `models/neuron-nih.glb` | 2.9 MB | NIH 3D Print Exchange |
| Plant Cell | `models/plant-cell-first001.glb` | 59 MB | Community contribution |
| White Blood Cell | `models/white-blood-cell-user.glb` | 56 MB | Community contribution |

### Code-Generated Models (No GLB Required)

| Cell Type | Description |
|---|---|
| Muscle Cell | Procedural myofibrils, nuclei, mitochondria, sarcoplasmic reticulum |
| Epithelial Cell | Procedural flattened cell with Golgi, nucleus, mitochondria |
| Red Blood Cell | Procedural biconcave disc with hemoglobin particles |

### Import Your Own Models

Click the **📦 Import GLB** button in the toolbar to upload custom `.glb` or `.gltf` files. The model will be automatically centered, scaled, and displayed in the viewport.

## Cell Data Reference

Detailed organelle information, dimensions, and biology notes for each cell type are embedded in the `CT` (cell types) and `ORG` (organelles) JavaScript data structures at the top of the HTML file.

Key data fields per organelle:
- `nm` — Name
- `st` — Subtitle (short description)
- `cl` — Color
- `at` — Attributes array (Size, Location, etc.)
- `nt` — Full biology note
- `ft` — Fun Fact

## License

This project is open source. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Three.js** — [threejs.org](https://threejs.org)
- **NIH 3D Print Exchange** — [3d.nih.gov](https://3d.nih.gov) for open scientific 3D models
- **cclank/cell-architecture-studio** — Inspiration for the React + R3F reference implementation

---

Built with ❤️ for science education.
