# 📚 Resources for Scientific Plotting

This folder collects all supplementary materials that support consistent, publication-quality figure design across different platforms (Mathematica, Python, etc.).

---

## 🎨 Color and Accessibility

## 🎨 1. Color and Accessibility

Color is one of the most powerful yet misused elements in scientific visualization. Proper use enhances clarity, reproducibility, and inclusivity. This section consolidates guidelines for designing color-robust and perception-accurate figures.

---

### 🌈 1.1 Why Color Matters
- **Visual clarity:** Enhances perception of trends and contrasts.
- **Scientific accuracy:** Encodes data meaning quantitatively, not decoratively.
- **Accessibility:** Roughly 8 % of men and 0.5 % of women have some form of color-vision deficiency.
- **Print reproducibility:** Some journals still print in grayscale — figures must survive desaturation.

---

### 🎨 1.2 Recommended Colormaps

| Purpose | Recommended Colormap | Notes |
|----------|----------------------|-------|
| Sequential | **Viridis**, **Cividis**, **Plasma** | Perceptually uniform, grayscale-friendly |
| Diverging | **Coolwarm**, **RdBu**, **Balance** | Centered on zero or mean value |
| Categorical | **Okabe–Ito**, **Tableau 10**, **Set2** | Distinct hues, color-blind safe |
| Cyclic | **Twilight**, **Phase**, **HSV (modified)** | Smooth wrapping at endpoints |

🚫 *Avoid* outdated colormaps (`jet`, `rainbow`) which distort numerical perception.

---

### ♿ 1.3 Designing for Color-Blind Accessibility
1. **Simulate impairments:**  
   - [Coblis](https://www.color-blindness.com/coblis-color-blindness-simulator/)  
   - [Color Oracle](https://colororacle.org/)
2. **Verify grayscale readability.**
3. **Use redundant cues:** markers, line styles, or text labels.
4. **Adopt the Okabe–Ito palette** (color-universal design):

### Resources
- **[Scientific Colormaps](https://s-ink.org/scientific-colour-maps)**


---

## ✅ Figure Preparation Checklist
- **[FigureChecklist.md](FigureChecklist.md)** — a concise list to review before exporting figures:
  - Font consistency (Arial, Palatino, etc.)
  - Line thickness and marker size
  - Axis labeling, units, and legends
  - Color-blind accessibility
  - Export format, resolution, and padding

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

