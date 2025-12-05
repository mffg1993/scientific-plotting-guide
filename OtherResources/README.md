# 📚 Resources for Scientific Plotting

This folder collects all supplementary materials that support consistent, publication-quality figure design across different platforms (Mathematica, Python, etc.).

---

## 🎨 1. Color and Accessibility

Color is one of the most powerful yet misused elements in scientific visualization. Proper use enhances clarity, reproducibility, and inclusivity. This section consolidates guidelines for designing color-robust and perception-accurate figures.

### 🌈 1.1 Why Color Matters? 
- **Visual clarity:** Enhances perception of trends and contrasts.
- **Scientific accuracy:** Encodes data meaning quantitatively, not decoratively.
- **Accessibility:** Roughly 8 % of men and 0.5 % of women have some form of color-vision deficiency.
- **Print reproducibility:** Some journals still print in grayscale — figures must survive desaturation.

### 🎨 1.2 Recommended Colormaps

| Purpose | Recommended Colormap | Notes |
|----------|----------------------|-------|
| Sequential | **Viridis**, **Cividis**, **Plasma** | Perceptually uniform, grayscale-friendly |
| Diverging | **Coolwarm**, **RdBu**, **Balance** | Centered on zero or mean value |
| Categorical | **Okabe–Ito**, **Tableau 10**, **Set2** | Distinct hues, color-blind safe |
| Cyclic | **Twilight**, **Phase**, **HSV (modified)** | Smooth wrapping at endpoints |

🚫 *Avoid* outdated colormaps (`jet`, `rainbow`) which distort numerical perception.

### ♿ 1.3 Designing for Color-Blind Accessibility
1. **Simulate impairments:**  
   - [Coblis](https://www.color-blindness.com/coblis-color-blindness-simulator/)  
   - [Color Oracle](https://colororacle.org/)
2. **Verify grayscale readability.**
3. **Use redundant cues:** markers, line styles, or text labels.
4. **Adopt the Okabe–Ito palette** (color-universal design):

### 1.4 Extra Resources
- **[Scientific Colormaps](https://s-ink.org/scientific-colour-maps)**

---

## ✅ 2. Figure Preparation Checklist

Producing publication-ready figures requires consistency, precision, and readability across software and formats. Use this checklist to ensure your plots meet both scientific and aesthetic standards.


### 🧩 2.1 Visual Design Basics
- **Consistency:** Maintain the same font, line width, and color scheme across all figures.  
- **Minimalism:** Remove unnecessary borders, background gradients, or 3D effects unless essential.  
- **Whitespace:** Leave enough padding so labels and legends never touch figure edges.  
- **Aspect ratio:** Preserve physically meaningful proportions (e.g., wavelength vs. angle plots).  
- **Text size:** Labels should remain legible when figures are reduced to ~8 cm width in print.

### 🔤 2.2 Typography and Labels
| Element | Recommendation | Notes |
|----------|----------------|-------|
| Font family | **Arial**, **Helvetica**, or **Palatino** | Journals often specify sans-serif for clarity |
| Axis titles | 24–30 pt for posters, 14–18 pt for manuscripts | Consistent across subplots |
| Tick labels | 2–4 pt smaller than axis titles | Use engineering notation (10³ not e3) |
| Units | Always include, in parentheses | e.g., *Intensity (a.u.)* |
| Symbols | Use LaTeX or Unicode for clarity | Avoid mixed fonts (e.g., italic Greek + normal text) |

### 📈 2.3 Data Representation
- Use **distinct markers** and **line styles** for overlapping datasets.  
- Always include **error bars** when applicable; explain their meaning in the caption.  
- For **logarithmic axes**, ensure minor ticks and zero-handling are correct.  
- Label data directly when possible — legends should complement, not duplicate.  
- Avoid using color alone to encode categories; combine with shape or pattern.

### 🧮 2.4 Layout and Composition
- Align subplots precisely using tools like `plt.subplots()` (Python) or `GraphicsGrid[]` (Mathematica).  
- Keep a consistent **margin** and **aspect ratio** between panels.  
- Use **letters (a), (b), (c)** in the top-left corners to label subfigures.  
- Match scales across comparable plots to avoid misinterpretation.  
- Verify alignment between colorbars, axes, and annotations.

### 💾 2.5 Exporting Figures
| Format | Use Case | Notes |
|---------|-----------|-------|
| **PDF/SVG** | Publication, vector editing | Infinite zoom, ideal for line art |
| **PNG** | Web or slides | 300 – 600 dpi recommended |
| **TIFF** | Journal submission | 600 dpi grayscale, 1200 dpi line art |
| **EPS** | Legacy typesetting | Ensure fonts are embedded |

**General tips:**
- Use **CMYK** conversion only at final print stage.  
- Always export with transparent or white background (avoid grey).  
- Verify text remains vector-based (not rasterized).  
- Save both **editable** (e.g., `.nb`, `.ipynb`, `.fig`) and **final** copies.

### 🧠 2.6 Consistency Across Platforms
- Test the same figure in **Mathematica**, **Matplotlib**, or **Illustrator**; verify color match.  
- Keep a small template file (`FigureTemplate.nb` or `FigureTemplate.py`) to standardize layout.  
- Include a short **metadata header** with version, date, and code used for generation.


### 🧾 2.7 Final Pre-Submission Checklist
✅ Fonts embedded and readable  
✅ Axes labeled with units  
✅ Legends consistent with caption terminology  
✅ Colors accessible and meaningful  
✅ Figure numbering matches manuscript references  
✅ Exported file passes publisher resolution checks  


### 📎 2.8 Related Resources
- [Nature Graphics Guide](https://www.nature.com/documents/nature-figures.pdf)  
- [Optica Publishing Group Figure Guidelines](https://opg.optica.org/submit/review/figures.cfm)  
- [IEEE Author Digital Toolbox](https://journals.ieeeauthorcenter.ieee.org/create-your-ieee-article/author-digital-toolbox/)  
- [Matplotlib Style Sheets](https://matplotlib.org/stable/gallery/style_sheets/style_sheets_reference.html)



---

## 🔗 Additional References
- **[Scientific Colormaps](https://s-ink.org/scientific-colour-maps)**
- **[Scientific Visualization: Python + Matplotlib by Nicolas P. Rougier](https://github.com/rougier/scientific-visualization-book)**
- **[InkScape](https://inkscape.org/)**
- 
---

## ✏️ Contributing
If you’d like to add a new guide (e.g., *“Typography.md”* or *“ColormapTesting.md”*), please:
1. Keep the file in this folder.  
2. Add a short description in this README.  
3. Update the main [`README.md`](../README.md) with the new link.

---

**Maintainer:** [Manuel Ferrer](https://github.com/mffg1993)  
**License:** CC-BY-SA 4.0 unless stated otherwise.

