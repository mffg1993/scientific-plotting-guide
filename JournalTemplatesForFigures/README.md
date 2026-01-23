# 📐 Journal Figure Specifications

This folder contains a reference table and example SVG files documenting **figure size constraints and typography guidelines for different scientific journals**.

Each journal imposes slightly different requirements on:

- Maximum usable page width  
- Single-column vs double-column layouts  
- Recommended font sizes and legibility rules  
- Aspect ratios and margin constraints  
- Export formats (PDF, EPS, SVG, TIFF)

Even when journals share nominal column widths, **figures almost always require manual fine-tuning** (label spacing, font scaling, line thickness, legend layout, etc.) to match each template cleanly.

The goal of this folder is to:

- ✅ Centralize dimension references  
- ✅ Avoid repeated trial-and-error during submission  
- ✅ Enable reproducible figure scaling across projects  
- ✅ Provide visual examples (SVG) that can be reused or adapted  

---

## 📊 Journal Dimension Reference Table

> ⚠️ **Note:** Values are approximate and should always be cross-checked against the latest author guidelines before final submission.

| Journal Name | Page Width (mm) | Single Column Width (mm) | Double Column Width (mm) | Typical Font Size in Figures (pt) | Notes |
|---------------|------------------|----------------------------|-----------------------------|-------------------------------------|--------|
| Optics Express | ~210 | ~85 | ~170 | 7–9 | OSA/Optica layout |
| Physical Review (APS) | ~216 | ~86 | ~178 | 7–9 | Tight margins |
| Nature Communications | ~180 | ~89 | ~180 | 7–8 | Full-width figures common |
| Science Advances | ~216 | ~90 | ~180 | 7–9 | Similar to *Science* |
| Applied Physics Letters | ~216 | ~85 | ~170 | 7–9 | Two-column format |
| Optica | ~210 | ~85 | ~170 | 7–9 | OSA journal |
| IEEE Photonics | ~216 | ~88 | ~180 | 8–10 | Slightly larger labels |
| arXiv (default) | ~210 | ~85 | ~170 | 8–10 | Depends on class file |

You are encouraged to extend this table as new journals are encountered.

---

## 🖼️ Example Files

This folder also contains:

- **SVG templates** showing:
  - Correct figure widths  
  - Font scaling  
  - Line thickness choices  
  - Legend spacing  

- Example exports for sanity checking readability before submission.

These SVGs are intended to be opened directly in:

- Inkscape  
- Adobe Illustrator  
- Affinity Designer  
- Or embedded into LaTeX workflows  

---

## 🛠️ Practical Workflow Recommendation

1. Select target journal.
2. Set figure width using the table above.
3. Adjust:
   - Font size  
   - Line width  
   - Marker size  
   - Legend spacing  
4. Export as vector (PDF / SVG / EPS).
5. Verify readability at final printed size.

Avoid designing figures at arbitrary sizes and scaling afterward — this almost always leads to unreadable labels or inconsistent styling.

---
