# Virtual Gadolinium: Deep Learning-Based Virtual Contrast MRI Synthesis and Brain Tumor Segmentation

Deep learning-based virtual contrast MRI synthesis (T1 pre → T1 post) using a residual U-Net, so no gadolinium contrast agent is needed.

> **Note:** This repository contains the published paper only. Source code and trained models are not included.

## Publication

- **Journal:** Spectrum of Engineering Sciences, Vol. 4, Issue 5, 2026, pp. 1831–1857
- **DOI:** https://doi.org/10.5281/zenodo.20321580
- **Paper (PDF):** [Download](https://github.com/laibaghalib/virtual-gadolinium-mri/raw/main/virtual-gadolinium.pdf)
- **Authors:** Samar Abbas, Muazzam Ali, Laiba Ghalib, Talha Aqeel, Reeba Waris Ali, Awais Ali, Zaeem Nazir (Department of Computer Science, University of Narowal)

## Summary

A residual U-Net that synthesizes gadolinium-enhanced T1-weighted MRI from unenhanced T1 images. The pipeline also includes post-processing and segmentation-guided visualization.

**Test set results:**

| Metric | Value |
|---|---|
| PSNR | 32.70 dB |
| SSIM | 0.9540 |

## Dataset

UCSF-PDGM (v3), downloaded from Kaggle: 100+ patients with paired T1-weighted pre-contrast (T1pre) and post-contrast (T1post) brain MRI volumes. The 3D NIfTI volumes were converted to 2D axial slices (128×128) for training.

## Method

- Residual U-Net with 4 encoder and 4 decoder stages, about 5.14M parameters
- Loss: combined SSIM + L1 (α = 0.8)
- Metrics: PSNR, SSIM, MSE, MAE

## Pipeline

![Pipeline](pipeline.png)

*Figure from the paper.*

Data preprocessing (3D NIfTI to 2D slices) → residual U-Net training → inference → post-processing (upsampling, sharpening) → segmentation-guided visualization.

## Architecture

![Residual U-Net](unet.png)

*Figure from the paper.*

## Limitations

- The model was trained on low-resolution (128×128) images.
- Further validation on larger datasets and prospective clinical studies is still needed, as stated in the paper.

## License

The paper is published under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license. Please cite the paper if you use or share it.

## Cite

Abbas, S., Ali, M., Ghalib, L., Aqeel, T., Ali, R. W., Ali, A., & Nazir, Z. (2026). Virtual Gadolinium: Deep Learning-Based Virtual Contrast MRI Synthesis and Brain Tumor Segmentation. *Spectrum of Engineering Sciences*, 4(5), 1831–1857. https://doi.org/10.5281/zenodo.20321580
