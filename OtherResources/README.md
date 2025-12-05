# 🚀 A Fast Guide to Scientific Figures

 **A concise, practical reference for creating clear, consistent, and accessible scientific figures.**  This guide summarizes best practices for color use, typography, accessibility, multi-panel layouts, and export standards — based on principles from leading journals and visualization research.

---
<details>
<summary><b>📖 Table of Contents</b> (click to expand)</summary>

<br>

1. [🎨 Color and Accessibility](#-1-color-and-accessibility)  
   - [🌈 1.1 Why Color Matters](#-11-why-color-matters)  
   - [🎨 1.2 Recommended Colormaps for Photonics Figures](#-12-recommended-colormaps-for-photonics-figures)  
   - [🧭 Types of Colormaps](#-types-of-colormaps)  
   - [♿ 1.3 Designing for Color-Blind Accessibility](#-13-designing-for-color-blind-accessibility)  
   - [📏 Line and Marker Styles](#-line-and-marker-styles)  

2. [✏️ 2. Figure Preparation: Fonts, Axes, and Labels](#️-2-figure-preparation-fonts-axes-and-labels)  

3. [💾 3. Export and File Formats](#-3-export-and-file-formats)  
   - [🧱 3.1 Vector vs. Raster Formats](#-31-vector-vs-raster-formats)  
   - [🖼️ 3.2 Resolution and Scaling](#-32-resolution-and-scaling)  
   - [🌈 3.3 Color Modes and Contrast](#-33-color-modes-and-contrast)  
   - [🧩 3.4 File Naming and Organization](#-34-file-naming-and-organization)  
   - [🧠 3.5 Quick Checklist](#-35-quick-checklist)  
   - [⚙️ 3.6 Suggested Export Settings](#-36-suggested-export-settings)  

4. [🧩 4. Multi-Panel Figure Layout and Composition](#-4-multi-panel-figure-layout-and-composition)  
   - [🧱 4.1 Layout and Alignment](#-41-layout-and-alignment)  
   - [🔠 4.2 Panel Labeling](#-42-panel-labeling)  
   - [🧭 4.3 Consistency Across Panels](#-43-consistency-across-panels)  
   - [⚙️ 4.4 Scaling and Space Management](#-44-scaling-and-space-management)  
   - [📐 4.5 Practical Tools](#-45-practical-tools)  
   - [🧠 4.6 Quick Checklist](#-46-quick-checklist)  

5. [🔗 5. Related Resources](#-5-related-resources)  

</details>

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

#### **Choosing the Right Colormap Type**

| Data Property | Question to Ask | Recommended Type |
|----------------|-----------------|------------------|
| **Ordered values** | Does your data progress from low → high without wrapping or sign changes? | **Sequential** |  
| **Centered around a reference** | Do values diverge around a zero or mean (±)? | **Diverging**  |
| **Periodic or angular** | Do values wrap cyclically (e.g., 0 = 2π)? | **Cyclic** | 
| **Multiple sub-ranges** | Are there two or more ordered segments with distinct meanings? | **Multi-sequential** | 
| **Discrete categories** | Are data groups independent with no numeric order? | **Qualitative / Categorical** | 

💡 *Once you know the type, choose the palette based on your figure background (light or dark) and whether low-amplitude variations must remain visible.*


### ♿ **1.2 Designing for Color-Blind Accessibility**

Accessibility is a fundamental aspect of scientific visualization — not an afterthought.  Well-designed figures should communicate data **accurately and inclusively**, regardless of how viewers perceive color.  
Making visualizations accessible benefits everyone by:

- **Ensuring scientific integrity:** prevents misinterpretation of quantitative trends caused by misleading color scales.  
- **Supporting reproducibility:** keeps figures interpretable across displays, lighting conditions, and grayscale prints.  
- **Improving communication:** allows a broader audience — including readers with color-vision deficiencies or older displays — to fully understand your results.  

Roughly **8 % of men and 0.5 % of women** have some form of color-vision deficiency.  Designing figures with accessibility in mind ensures that your data remain clear in print, on screen, and during presentations.


#### 🧩 Practical Tips for Accessible Visualization
1. **Simulate impairments before publishing:**  
   Test your figures using online or desktop simulators such as  
   - [Coblis](https://www.color-blindness.com/coblis-color-blindness-simulator/)  
   - [Color Oracle](https://colororacle.org/)  
   These tools emulate how figures appear under various types of color-vision deficiency.

2. **Check grayscale readability:**  
   Convert the figure to grayscale (or print in black and white) — the structure and contrast should still be recognizable.

3. **Use redundant visual cues:**  
   Combine **line styles**, **markers**, and **annotations** to distinguish datasets.  
   For example, use dashed vs. solid lines, or add direct numeric labels rather than relying solely on a color legend.

4. **Adopt color-blind–safe palettes:**  
   Select palettes that remain distinguishable for all viewers and preserve perceptual uniformity. Recommended options include the **Okabe–Ito palette** and the [**Scientific Colormaps**](https://s-ink.org/scientific-colour-maps) collection, both designed for accessibility and quantitative accuracy.

5. **Maintain sufficient contrast:**  
Use dark colors on light backgrounds (or vice versa) and avoid problematic pairs such as red–green or blue–magenta.

6. **Label directly when possible:**  
Legends are useful, but direct annotations reduce confusion in dense or multi-panel plots.

### 🎨 **1.3 Recommended Colormaps for Optics+Photonics Figures**

In photonics, color is not only aesthetic — it carries **quantitative meaning**. Choosing the right colormap ensures that your figures remain **physically interpretable**, even under color-blind simulation, grayscale reproduction, or projection.

These recommendations cover colormaps that are well suited for the most common types of photonics figures.  They provide a reliable foundation for representing quantities such as intensity, phase, and spectral information in a clear and reproducible way. 

| Application | Description | Type | Matplotlib Colormap | Mathematica Colormap | Notes |
|--------------|-------------|------|--------------------|----------------------|-------|
| **Amplitude/Intensity distributions**  | Used for spatial light intensity or power maps in near/far field measurements, such as beam profiles, CCD images. | Sequential | `viridis`, `cividis`, `inferno` | `"Cividis"`, `"DeepSeaColors"`, `"SolarColors"` | Perceptually uniform; suitable for linear or log scaling. |
| **Phase distribution** | Represents optical phase (0–2π), or holographic reconstructions. | Cyclic | `twilight`, `phase`, `hsv` (modified) | `"Hue"`, `"PhaseColors"`, `"TwilightColors"` | Cyclic colormaps wrap continuously from 0 → 2π to avoid artificial discontinuities at 0/2π boundaries|
| **Variable-dependent plots** | Ideal for spectral power density, transmission/reflection spectra, or dispersion maps for multiple samples.| Qualitative/Categorical  | ``tab10`, `Set2`, `Paired` | `"AquaticColors"`, `"IslandColors"`, `"Pastel", `"SunsetColors"` | Discrete, color-blind-safe hues for clear group separation. Can be paired with different types of lines |
| **Matrix plots**  | Represent pairwise relationships or coupling strengths between modes, frequencies, or spatial channels. Some examples are correlations and crosstalk visualization. | Diverging / Sequential | `coolwarm`, `RdBu_r`, `viridis` | `"TemperatureMap"`, `"RedBlueTones"`, `"Cividis"` | Use diverging palettes when data contain both positive and negative correlations; sequential for absolute values only. |
| **Categorical data** | For discrete labels like TE/TM polarization, device types, or materials. | Qualitative | `tab10`, `Set2`, `Paired` | `"AquaticColors"`, `"IslandColors"`, `"Pastel"` | Discrete, color-blind-safe hues for clear group separation. |

For more complex visualizations — including phase–amplitude overlays, polarization-resolved fields, or multidimensional datasets — customized or composite palettes can be developed by combining cyclic and sequential schemes to capture all relevant parameters.

### 1.4 📏 **Line and Marker Styles**

Accessibility can also be achieved through the use of **line and marker styles**, which provide additional visual cues beyond color.  
By combining variations in line type, thickness, and marker shape, different datasets remain distinguishable even in grayscale prints or for viewers with color-vision deficiencies.

| Term | Description | Common Examples |
|------|--------------|-----------------|
| **Line style** | Defines the *pattern* of a line. | `solid`, `dashed`, `dotted`, `dashdot` |
| **Line type** | Synonym for line style; used interchangeably in many libraries. | Same as above |
| **Stroke style** | Used in vector graphics editors (e.g., SVG, Inkscape, Illustrator). | `stroke-dasharray`, `stroke-width` |
| **Line pattern** | Custom dash sequence controlling the dash–gap rhythm. | e.g., `[5, 2, 2, 2]` for a long–short–short dash |
| **Line width** | Controls the thickness of the line. | `linewidth`, `PlotStyle -> Thick` |
| **Marker style** | Defines the shape of data points or sample markers. | `circle`, `square`, `triangle`, etc. |


#### 🔧 Equivalent Syntax in Common Tools

| Style | Matplotlib (Python) | Mathematica | Example Plot |
|--------|--------------------|-------------|---------------|
| **Solid** | `linestyle='-'` | `PlotStyle -> {Thick}` | Continuous curve |
| **Dashed** | `linestyle='--'` | `PlotStyle -> {Dashed}` | Alternating dash pattern |
| **Dotted** | `linestyle=':'` | `PlotStyle -> {Dotted}` | Fine dotted line |
| **Dash–Dot** | `linestyle='-.'` | `PlotStyle -> {DotDashed}` | Dash and dot repeating |
| **Custom pattern** | `linestyle=(0, (5, 2, 1, 2))` | `Dashing[{0.02, 0.01, 0.005, 0.01}]` | User-defined pattern |
| **Line width** | `linewidth=2.5` | `Thickness[0.006]` | Adjusts thickness |
| **Marker** | `marker='o'`, `'s'`, `'D'` | `PlotMarkers -> Automatic` | Adds point symbols |

---

## ✏️ 2. Figure Preparation: Fonts, Axes, and Labels

Readable, consistent typography and well-defined axes are key to producing professional, publication-quality figures.  The goal is to maximize the space devoted to **data**, while ensuring that every label, tick, and symbol remains legible after scaling or printing.


### 🔤 2.1 Fonts and Text
- **Use sans-serif fonts:**
   - These remain clear in print and screen formats.
   - Some examples are *Arial*, *Helvetica* or *Myriad*.
- **Keep text sizes consistent:**
  - Apply consistent **thickness, font, and scale** across all figures in a manuscript.  
  - Main axis labels should be size similar in size to the size of the text in the main body.
  - Tick labels: 5-10% smaller than axis labels.  
  - Sub-panel letters (A, B, C…): 5-10% smaller than axis labels. Always placed in the upper-left corner. Style varies depending on the journal. 
- **Style conventions:**  
  - Capitalize only the first letter of each label (except proper nouns).  
- **Avoid color text** over color backgrounds; use **bold black or white** for contrast.  
- Embed all fonts when exporting to vector formats (EPS, PDF, SVG).  

### 📊 2.2 Axes and Scales
- **Keep axes tight** to the data range—avoid extending beyond plotted values.  
- **No redundant axes:** do not repeat y-labels on mirrored panels.  
- **Prefer major ticks only**; minor ticks and gridlines often add clutter.  
- Present large or small values as **powers of 10** (e.g., 10³ – 10⁵).  
- **Use consistent tick spacing** across panels within the same figure.  
- All micrographs or images **must include scale bars** with their numeric value in the figure or legend.  
- Avoid excessive whitespace—place sub-panels close together with aligned axes.
- Write exponents as 6 × 10⁻³ —not 6e-03.  

### 🧭 2.3 Labels and Legends
- Use *italics* for variables (*P*, *T*, *μ*), **bold roman** for vectors (**E**, **k**).
- Each axis must indicate the **quantity**, **symbol**, and **unit**:  
  > *Intensity (I)* (a.u.), *Wavelength (λ)* (nm)
- Always include **units in parentheses** and use **SI notation** (e.g., Pressure (MPa)).   
- Use **simple, solid, or open symbols** that remain legible when reduced.  
- Keep legends concise and positioned so they do not enlarge the figure unnecessarily.  
- When multiple panels share the same labels, **use common axis labels** instead of repeating them.  
- For multi-panel figures, label parts as **A, B, C** (uppercase, bold); avoid nested labels like C(i) or C′.  


### 🧠 2.5 Quick Reference
| Element | Recommendation | Notes |
|----------|----------------|-------|
| Font family | **Arial**, **Helvetica**, or **Palatino** | Journals often specify sans-serif for clarity |
| Axis titles | size similar in size to the size of the text in the main body | Consistent across subplots |
| Tick labels | 5-10% smaller than axis Labels | Use engineering notation (10³ not e3) |
| Units | Always include, in parentheses | e.g., *Intensity (a.u.)* |

---

## 💾 3. Export and File Formats

Preparing figures for publication requires attention to file type, resolution, and color mode.  The objective is to preserve **scalability**, **readability**, and **color accuracy** across platforms, from preprint to final print.

### 🧱 3.1 Vector vs. Raster Formats
- **Prefer vector formats** (`.pdf`, `.eps`, `.svg`, `.ai`) for all line art, graphs, and schematics.  
  These maintain sharpness at any zoom level and allow easy editing of text and symbols.  
- **Use raster formats** (`.tif`, `.png`, `.jpg`) only for photographic or pixel-based data such as microscope or camera images.  
- Never submit figures in presentation or word-processor formats (`.ppt`, `.docx`, `.key`); they are not publication-ready.  
- Each figure should be saved as a **single file** that includes all labeled sub-panels.

### 🖼️ 3.2 Resolution and Scaling
| Figure Type | Recommended Resolution | Notes |
|--------------|-----------------------|-------|
| **Line art** | ≥ 600 dpi | Black and white bitmap, not grayscale. |
| **Halftones (photographs)** | 264 dpi (grayscale) | Maintain smooth tonal transitions. |
| **Combinations (line + halftone)** | 600 dpi (grayscale) | Avoid aliasing or mismatched scaling. |
| **Color figures** | 300 dpi (CMYK or RGB) | RGB for online, CMYK for print. |

- Prepare figures **at final print size** to avoid scaling artifacts.  
  Typical journal widths: 3.5 in (single column), 5.0 in (1.5 columns), or 7.0 in (two columns).  

### 🌈 3.3 Color Modes and Contrast
- **RGB** (red-green-blue) for digital and online content.  
- **CMYK** (cyan-magenta-yellow-black) for print submissions.  

### 🧩 3.4 File Naming and Organization
- Use consistent, descriptive filenames following this format:  
  `Lastname_Fig1.pdf`, `Lastname_Fig2_Supplementary.tif`, etc.  
- Avoid splitting figures into multiple files (e.g., `Fig1A`, `Fig1B`); compile sub-panels into one complete figure.  
- Embed all fonts before exporting.  
- For collaborative or automated workflows, include figure metadata such as version, software, and color profile.

### ⚙️ 3.5 Suggested Export Settings

Export settings vary by software, but the goal is always to produce scalable, high-resolution figures with embedded fonts and consistent color profiles.  
The table below summarizes recommended parameters for common tools used in scientific visualization.

| Software | Preferred Export Format | Key Settings | Notes |
|-----------|------------------------|---------------|-------|
| **Matplotlib (Python)** | `.pdf`, `.svg`, `.eps` | `plt.savefig("Figure.pdf", dpi=600, bbox_inches='tight', transparent=True)` | Use vector formats for all line art. Set `dpi=300–600`. Ensure fonts are embedded (`pdf.fonttype = 42`). |
| **Mathematica** | `.pdf`, `.eps`, `.svg` | `Export["Figure.pdf", plot, ImageResolution -> 600, "AllowRasterization" -> False]` | Keep `AllowRasterization -> False` for pure vector output. Use consistent label fonts (`FontFamily -> "Arial"`). |
| **Adobe Illustrator / Inkscape** | `.pdf`, `.eps`, `.svg` | Embed fonts, export at 300–600 dpi; choose “High Quality Print” preset for PDF. | CMYK for print; RGB for digital. Ensure strokes and text remain editable. |
| **Image-based data** (microscopy, camera) | `.tif`, `.png` | 300 dpi (color) or 600 dpi (grayscale) | Avoid `.jpg` compression for analysis or publication. Include scale bar and legend in same file. |
| **Combined plots** (line + image) | `.pdf` or `.tif` | Vector for overlays, 600 dpi for image layer | Ensure consistent aspect ratio and no interpolation artifacts. |

#### 💡 Additional Tips
- Always **preview exported files** in an external viewer to verify scaling, text legibility, and color accuracy.  
- Keep a **master vector file** for each figure (`.svg` or `.pdf`) before producing raster versions for presentations.  
- Use **transparent backgrounds** when overlaying figures on colored layouts.  
- Store both a **print version** (CMYK, high DPI) and a **web version** (RGB, smaller file size).
-  Automate your export pipeline by defining consistent parameters (font, resolution, color mode) in your plotting scripts or templates — it guarantees reproducibility and professional results across all figures.

---
## 🧩 4. Multi-Panel Figure Layout and Composition

Complex datasets often require multi-panel figures to compare simulations, measurements, and analytical models.  A well-designed layout helps the reader follow your narrative while maintaining clarity and visual balance.  
Every panel should contribute to a single, coherent message. A multi-panel figure should read like a short story — each panel a sentence, together forming a clear, structured narrative that guides the reader from observation to conclusion.



### 🧱 4.1 Layout and Alignment
- Arrange panels **in logical reading order** (left-to-right, top-to-bottom).  
- Keep panels **tightly grouped** — excessive white space reduces visual cohesion.  
- **Align axes and colorbars** precisely using grid layouts or consistent margins.  
- Maintain **identical scales and axis limits** when panels are meant to be compared.  
- Use uniform aspect ratios to avoid visual distortion of relative trends.  
- Place common axis labels along shared edges to save space and avoid redundancy.  

### 🔠 4.2 Panel Labeling
- Label parts sequentially with **capital letters** (**A**, **B**, **C**, …) in **bold**, upper-left corner of each panel.  
- Keep label size consistent.  
- Do **not** use nested sub-labels such as C(i) or C′; continue the sequence instead.  
- For image panels, place labels **inside the boundary** of the figure area rather than in external margins.  
- Maintain alignment of labels horizontally and vertically for a clean, professional look.

### 🧭 4.3 Consistency Across Panels

A good practice is to efine figure templates (grid size, padding, colorbars) to maintain consistency across publications.  For example, 

| Element | Consistency Rule | Example |
|----------|------------------|----------|
| **Fonts** | Same family and size throughout | Arial 14 pt for all axes |
| **Line thickness** | Uniform across all plots | 1 pt lines for curves and boxes |
| **Color scheme** | Single, coherent palette | Okabe–Ito or Scientific Colormaps |
| **Axis limits** | Match when comparing quantities | same x/y range in (A) and (B) |
| **Tick spacing** | Regular and aligned | 0, 2, 4, 6 on both panels |
| **Legend format** | Identical location and order | bottom-right corner, two entries |
| **Background** | Neutral and uniform | white or transparent |


### ⚙️ 4.4 Scaling and Space Management
- Use the **same width** for all panels in a row to maintain symmetry.  
- For 2 × 2 layouts, keep equal spacing horizontally and vertically (e.g., 0.1–0.2 in).  
- Avoid overlapping colorbars or legends; align them to a grid or shared column.  
- When mixing plot types (images + graphs), balance visual weight — do not let one panel dominate.  
- Crop images tightly to the region of interest; avoid excess margins around data.
- Keep all panels within a **common bounding box** before export for consistent scaling.  
- Use **transparent backgrounds** for combining figures in post-processing.  


### 📐 4.5 Practical Tools
Different tools offer precise control for multi-panel figure layouts.  
The goal is to maintain **alignment, proportionality, and consistent export settings** regardless of the software used.

| Tool | Recommended Workflow | Key Commands / Notes |
|------|----------------------|----------------------|
| **Matplotlib (Python)** | Create panels programmatically using `plt.subplots()` or `GridSpec`. | Use `sharex=True, sharey=True` for alignment; export with `bbox_inches='tight'`. |
| **Mathematica** | Combine graphics using `GraphicsGrid` or `Grid`. | Control spacing via `Spacings -> {0.1, 0.1}`; use `ImagePadding` for uniform margins. |
| **MATLAB** | Use `tiledlayout()` (newer) or `subplot()` (legacy). | `tiledlayout(2,2); nexttile; plot(...)`; align colorbars with `colorbar.Layout.Tile`. |
| **Plotly / Dash** | Arrange subplots interactively or via JSON layout. | Use `make_subplots()` with `row_heights` and `column_widths` to balance space. |
| **Origin / OriginPro** | Combine graphs using the **Graph Merge** or **Layout Page** tool. | Ensure identical axis ranges; export as vector (`.eps`, `.pdf`). |
| **Adobe Illustrator / Inkscape** | Align panels precisely using grid snapping or smart guides. | Group related panels, keep consistent font embedding, verify scaling at 100 %. |
| **Affinity Designer** | Manage multi-panel layouts with artboards. | Use the “Arrange → Align” tools for perfect spacing; export to PDF with embedded fonts. |
| **LaTeX (Overleaf / TikZ / pgfplots)** | Arrange subplots within `figure*` environments or use `subcaption` package. | Use `\begin{subfigure}` blocks with identical width ratios; compile to PDF for vector output. |

---

## 🔗 5. Related Resources

The following resources provide deeper guidance on color design, figure preparation, accessibility, and data visualization standards used across scientific disciplines.

### 🎨 Color and Accessibility
- **[Scientific Colormaps](https://s-ink.org/scientific-colour-maps)** — a collection of perceptually uniform, color-blind–safe colormaps by Fabio Crameri.  
- **[ColorBrewer 2.0](https://colorbrewer2.org)** — interactive tool for selecting palettes for categorical, sequential, and diverging data.  
- **[Okabe–Ito Palette Reference](https://jfly.uni-koeln.de/color/)** — accessible palette widely used in scientific graphics.  
- **[Coblis – Color Blindness Simulator](https://www.color-blindness.com/coblis-color-blindness-simulator/)** — preview figures under different color-vision deficiencies.  
- **[Color Oracle](https://colororacle.org/)** — desktop simulator for color-blind accessibility testing.


### 🖋️ Figure Preparation and Typography
- **AIP Publishing Author Guide – Preparing Graphics**  
  ([AIP Author Services](https://authorservices.aip.org/services_pricing)) — detailed DPI, format, and vector export standards.  
- **Science Advances Figure Preparation Guidelines** — layout, font, and labeling standards for professional publications.  
- **Nature Research – Artwork and Figures**  
  ([Nature Author Portal](https://www.nature.com/nature-portfolio/editorial-policies/artwork)) — guidance on figure composition and print scaling.

### 📊 Visualization Tools and Repositories
- **[Matplotlib Documentation](https://matplotlib.org/stable/contents.html)** — official Python plotting library reference.  
- **[Wolfram Color Schemes](https://reference.wolfram.com/language/guide/ColorSchemes.html)** — built-in palettes for Mathematica.  
- **[Plotly Express](https://plotly.com/python/plotly-express/)** — interactive and publication-ready plotting interface for Python.  
- **[Inkscape](https://inkscape.org/)** — free, cross-platform vector graphics editor for figure layout and labeling.  
- **[Affinity Designer](https://affinity.serif.com/)** — lightweight alternative to Adobe Illustrator for scientific graphics.  


### 🧠 Data Visualization and Design References
- **Jambor, H. K.** *A checklist for designing and improving the visualization of scientific data.* **Nature Cell Biology** 27, 879–883 (2025). [https://doi.org/10.1038/s41556-025-01684-z](https://www.nature.com/articles/s41556-025-01684-z)
- **Rougier, N. P.** *Scientific Visualization: Python & Matplotlib.*  Open-access book and example repository. [https://github.com/rougier/scientific-visualization-book](https://github.com/rougier/scientific-visualization-book)
- **Crameri, F., Shephard, G. E., & Heron, P. J.** *The misuse of colour in science communication.*  **Nature Communications** 11, 5444 (2020).    [https://doi.org/10.1038/s41467-020-19160-7](https://doi.org/10.1038/s41467-020-19160-7)
- **Rougier, N. P., Droettboom, M., & Bourne, P. E.** *Ten Simple Rules for Better Figures.*  **PLOS Computational Biology** 10(9): e1003833 (2014).  [https://doi.org/10.1371/journal.pcbi.1003833](https://doi.org/10.1371/journal.pcbi.1003833)
- **Crameri, F.** *Visualisation: Principles and Practice.*  **Zenodo** (2023). [https://doi.org/10.5281/zenodo.7991761](https://doi.org/10.5281/zenodo.7991761)



**Maintainer:** [Manuel Ferrer](https://github.com/mffg1993)  
**License:** CC-BY-SA 4.0 unless stated otherwise.

