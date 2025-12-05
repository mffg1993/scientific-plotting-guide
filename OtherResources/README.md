# 📚 Resources for Scientific Plotting

This folder collects all supplementary materials that support consistent, publication-quality figure design across different platforms (Mathematica, Python, etc.).

---

## 🎨 1. Color and Accessibility

Color is one of the most powerful yet misused elements in scientific visualization. Proper use enhances clarity, reproducibility, and inclusivity. This section consolidates guidelines for designing color-robust and perception-accurate figures.

### 🌈 **1.1 Why Color Matters**

A well-designed plot should be immediately understandable. Each dataset or data point must be **visually distinguishable**, guiding the reader’s eye toward the key findings.  
The thoughtful use of a color palette not only improves the aesthetic appeal of a figure, but also serves as a **powerful visual aid** to emphasize patterns, trends, and contrasts in your results.  

When selecting colors, remember that **clarity and accessibility are as important as beauty**. A good palette communicates information effectively to *everyone*, including readers with color-vision deficiencies or those viewing the figure in grayscale.  

Key aspects to consider:

- **Visual clarity:** Colors should make it easy to perceive differences and trends at a glance.  
- **Scientific accuracy:** Use color to represent data meaningfully, not decoratively.  
- **Accessibility:** Around 8 % of men and 0.5 % of women experience color-vision deficiencies — avoid relying solely on hue to convey information.  
- **Print reproducibility:** Many journals or print copies render in grayscale; ensure distinctions remain visible when colors are removed.

Selecting an appropriate colormap starts with understanding the **structure of the data** being visualized.  
Different datasets convey different relationships — some vary smoothly from low to high values, others oscillate periodically, and some contain distinct, unordered categories.  
Recognizing these patterns is the first step toward assigning color meaningfully, ensuring that the visualization conveys both the data’s **quantitative range** and its **conceptual structure** rather than simply adding decoration.

**Choosing the Right Colormap Type**

| Data Property | Question to Ask | Recommended Type |
|----------------|-----------------|------------------|
| **Ordered values** | Does your data progress from low → high without wrapping or sign changes? | **Sequential** |  
| **Centered around a reference** | Do values diverge around a zero or mean (±)? | **Diverging**  |
| **Periodic or angular** | Do values wrap cyclically (e.g., 0 = 2π)? | **Cyclic** | 
| **Multiple sub-ranges** | Are there two or more ordered segments with distinct meanings? | **Multi-sequential** | 
| **Discrete categories** | Are data groups independent with no numeric order? | **Qualitative / Categorical** | 

💡 *Once you know the type, choose the palette based on your figure background (light or dark) and whether low-amplitude variations must remain visible.*


### 🎨 **1.2 Recommended Colormaps for Optics+Photonics Figures**

In photonics, color is not only aesthetic — it carries **quantitative meaning**. Choosing the right colormap ensures that your figures remain **physically interpretable**, even under color-blind simulation, grayscale reproduction, or projection.

These recommendations cover colormaps that are well suited for the most common types of photonics figures.  They provide a reliable foundation for representing quantities such as intensity, phase, and spectral information in a clear and reproducible way. 


| Application | Description | Type | Matplotlib Colormap | Mathematica Colormap | Notes |
|--------------|-------------|------|--------------------|----------------------|-------|
| **Amplitude/Intensity distributions**  | Used for spatial light intensity or power maps in near/far field measurements, such as beam profiles, CCD images. | Sequential | `viridis`, `cividis`, `inferno` | `"Cividis"`, `"DeepSeaColors"`, `"SolarColors"` | Perceptually uniform; suitable for linear or log scaling. |
| **Phase distribution** | Represents optical phase (0–2π), or holographic reconstructions. | Cyclic | `twilight`, `phase`, `hsv` (modified) | `"Hue"`, `"PhaseColors"`, `"TwilightColors"` | Cyclic colormaps wrap continuously from 0 → 2π. |
| **Variable-dependent plots** | Ideal for spectral power density, transmission/reflection spectra, or dispersion maps for multiple samples.| Qualitative Categorical  | `plasma`, `turbo`, `parula` | `"AvocadoColors"`, `"Rainbow"` (modified), `"SunsetColors"` | Smooth color transitions preserving neighbor contrast. |
| **Diverging quantities** (Δn, reflectivity change, difference maps) | For signed data centered on a neutral baseline (e.g., phase shift or refractive index variation). | Diverging | `coolwarm`, `RdBu`, `balance` | `"RedBlueTones"`, `"TemperatureMap"` | Highlights both positive and negative deviations. |
| **Categorical data** (polarizations, samples, materials) | For discrete labels like TE/TM polarization, device types, or materials. | Qualitative | `tab10`, `Set2`, `Paired` | `"AquaticColors"`, `"IslandColors"`, `"Pastel"` | Discrete, color-blind-safe hues for clear group separation. |

For more complex visualizations — including phase–amplitude overlays, polarization-resolved fields, or multidimensional datasets — customized or composite palettes can be developed by combining cyclic and sequential schemes to capture all relevant parameters.
---

#### 🧠 Practical Notes for Photonics
- **Phase plots:** Always use cyclic colormaps to avoid artificial discontinuities at 0/2π boundaries.  
- **Spectral data:** When mapping wavelength, remember that perceived hue ≠ physical wavelength — choose palettes that remain monotonic in luminance.  
- **Beam profiles:** For publication clarity, overlay contour lines or normalization ticks instead of relying purely on color brightness.  
- **Logarithmic intensity maps:** Prefer `Inferno` or `Cividis` — both preserve detail in dark regions, unlike `Viridis`, which compresses near-zero values.  

---

#### 🧩 Implementation Examples

**Matplotlib (Python):**
```python
import matplotlib.pyplot as plt
plt.imshow(beam_profile, cmap='inferno', origin='lower')
plt.colorbar(label='Normalized Intensity')
plt.xlabel('x (μm)')
plt.ylabel('y (μm)')
plt.show()












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

