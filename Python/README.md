# Python Figure Templates

This folder contains Python scripts and notebooks that demonstrate how to create **publication-quality scientific figures** using libraries such as **Matplotlib** and **NumPy**.  
All templates follow the visual and accessibility guidelines described in the main [Fast Guide to Scientific Figures](../FastGuideToScientificFigures.md).

---

## 📄 Contents

| File / Sub-folder | Description |
|------------------|-------------|
| `*.py` / `*.ipynb` | Example scripts or notebooks for generating line, bar, and scatter plots with consistent formatting. |
| `styles/` *(if present)* | Custom Matplotlib style sheets (`.mplstyle`) for unified fonts, colors, and sizes. |
| `export_settings/` *(optional)* | Recommended export configurations (resolution, DPI, vector formats). |
| `README.md` (this file) | Overview and usage notes for the Python plotting templates. |

---

## ✅ Why Use These Templates

- Establish a **consistent visual language** across all your figures (fonts, colors, line styles, legends).  
- Apply **color-blind-safe palettes** (e.g., Okabe–Ito or cividis) by default.  
- Ensure all figures are **ready for publication** — axis labels with units, readable text, no chartjunk.  
- Build figures quickly and reproducibly using standardized code blocks.

---

## 🚀 Usage Instructions

1. Install the required libraries (typically: `matplotlib`, `numpy`, `scipy`, and optionally `pandas`):  
   ```bash
   pip install matplotlib numpy scipy pandas

