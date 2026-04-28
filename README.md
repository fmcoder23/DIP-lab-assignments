# Digital Image Processing - Lab Assignments

**Course:** Digital Image Processing
**Semester:** Spring 2025
**Student:** Fozil Mamadaliev
**Institution:** Central Asian University

## Overview

This repository contains lab assignments and implementations for the Digital Image Processing course. Each week folder includes Jupyter notebooks with practical implementations of various image processing techniques.

## Course Reference

Course materials are based on the [DIP repository](https://github.com/b-kiani/DIP) by instructor Behnam Kiani.

## Repository Structure

```
.
├── week5/          # Week 5 assignments
├── week6/          # Week 6 - Image smoothing and sharpening
│   ├── lab6_image_filtering.ipynb
│   ├── noisy_image.jpeg
│   └── results/    # Generated output images
└── README.md
```

## Week 6: Image Smoothing and Sharpening

### Topics Covered
- Convolution operations
- Box filtering
- Gaussian filtering
- Unsharp masking for edge enhancement
- Histogram equalization
- Parameter exploration for image sharpening

### Objectives
- Understand and implement image filtering techniques
- Explore how filters affect image sharpness, blurring, and enhancement
- Analyze the impact of different filter parameters

### Lab Tasks
1. **Task 1:** Histogram equalization with before/after comparison
2. **Task 2:** Gaussian filter with multiple kernel sizes and sigma values
3. **Task 3:** Unsharp masking for image sharpening
4. **Task 4:** Parameter exploration (filter_size and k values)

### Technologies Used
- Python 3.9+
- OpenCV (`opencv-python`)
- NumPy
- Matplotlib
- scikit-image

## Setup and Installation

### Prerequisites
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install Dependencies
```bash
pip install opencv-python matplotlib numpy scikit-image jupyter
```

### Running Jupyter Notebooks
```bash
cd week6
jupyter notebook lab6_image_filtering.ipynb
```

## Key Concepts

### Histogram Equalization
Enhances image contrast by redistributing pixel intensities across the full dynamic range, particularly effective for poorly lit images.

### Gaussian Filtering
Superior to box filtering for creating natural-looking blur with weighted averaging that better preserves edges.

### Unsharp Masking
Enhances edges by:
1. Blurring the original image
2. Subtracting blur from original to extract high-frequency details
3. Adding amplified details back to the original

**Formula:** `Sharpened = Original + k × (Original - Blurred)`

### Parameter Effects

#### Filter Size
- **Small (3, 5):** Local detail enhancement
- **Medium (7, 9):** Balanced general-purpose sharpening
- **Large (11, 15):** Global enhancement with potential halos

#### K Value
- **Negative k:** Blurring effect
- **k = 0:** No change
- **0 < k < 1:** Mild sharpening
- **1 ≤ k ≤ 3:** Moderate to strong sharpening
- **k > 3:** Extreme sharpening with noise amplification

## Results

All generated images and visualizations are saved in the `week*/results/` directories.

## License

This is an educational project for academic purposes.

## Acknowledgments

- Instructor: Behnam Kiani
- Course repository: [b-kiani/DIP](https://github.com/b-kiani/DIP)
- Central Asian University
