# Virtual Gadolinium: Deep Learning-Based Virtual Contrast MRI Synthesis and Brain Tumor Segmentation

Deep learning-based virtual contrast MRI synthesis (T1 pre → T1 post) using a residual U-Net.

> **Note:** This repository contains the published paper only. Source code and trained models are not included.

## Publication

- **Journal:** Spectrum of Engineering Sciences, Vol. 4, Issue 5, 2026, pp. 1831–1857
- **DOI:** https://doi.org/10.5281/zenodo.20321580
- **Authors:** Samar Abbas, Muazzam Ali, Laiba Ghalib, Talha Aqeel, Reeba Waris Ali, Awais Ali, Zaeem Nazir (Department of Computer Science, University of Narowal)

## Summary

A residual U-Net that synthesizes gadolinium-enhanced T1-weighted MRI from unenhanced T1 images, so no contrast agent is needed. Trained on the UCSF-PDGM dataset (paired T1pre and T1post slices) with a combined SSIM + L1 loss.

| Set | PSNR | SSIM |
|---|---|---|
| Validation | 35.99 dB | 0.9693 |
| Test | 32.70 dB | 0.9540 |

## Pipeline

Data preprocessing (3D NIfTI to 2D slices) → residual U-Net training → inference → post-processing (upsampling, sharpening) → segmentation-guided visualization.

## My contribution

(Yahan apna kaam likho)

## Cite

Abbas, S., Ali, M., Ghalib, L., Aqeel, T., Ali, R. W., Ali, A., & Nazir, Z. (2026). Virtual Gadolinium: Deep Learning-Based Virtual Contrast MRI Synthesis and Brain Tumor Segmentation. *Spectrum of Engineering Sciences*, 4(5), 1831–1857. https://doi.org/10.5281/zenodo.20321580
