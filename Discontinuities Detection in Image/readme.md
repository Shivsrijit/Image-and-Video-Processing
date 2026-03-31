# Image Processing Topics Summary

## 1. Image Derivatives & Finite Differences
- First-order derivatives using finite differences
- Approximation of gradients in discrete images

## 2. Point Detection
- 4-Neighbor Laplacian
- 8-Neighbor Laplacian

## 3. Line Detection
- Horizontal masks
- Vertical masks
- Diagonal masks

## 4. Edge Detection Operators

### Roberts Cross
- Diagonal gradient approximation

### Prewitt Operator
- Horizontal ($g_x$) and vertical ($g_y$) gradients

### Sobel Operator
- Weighted gradients:
  - $g_x$
  - $g_y$
- Gradient magnitude:
  - $|G| = \sqrt{g_x^2 + g_y^2}$ (or approximation)

## 5. Advanced Edge Detection

### Laplacian of Gaussian (LoG)
- Combines smoothing + second derivative
- Edge detection via zero-crossings

### Canny Edge Detection
- Multi-stage process:
  - Gaussian smoothing
  - Gradient computation
  - Non-Maximum Suppression
  - Double Thresholding
  - Hysteresis

## 6. Harris Corner Detection
- Second Moment Matrix:
  - $M$
- Response Score:
  - $R = \det(M) - k(\text{trace}(M))^2$

## 7. Hough Transform
- Line detection using:
  - Polar coordinates $(\rho, \theta)$
- Accumulator-based voting

## 8. Image Preprocessing & Post-processing

### Preprocessing
- Grayscale conversion
- Gaussian blurring / smoothing

### Thresholding
- Global thresholding
- Local (adaptive) thresholding

### Post-processing Considerations
- Absolute value vs clamping:
  - Negative values → set to zero (clamping)
  - Or use absolute magnitude

###### To view and edit on Kaggle  
[Open the notebook on Kaggle](https://www.kaggle.com/code/shivsrijitverma/discontinuities-detction-in-images)

