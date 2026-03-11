# Frequency Domain Image Filtering

## Overview

This project demonstrates basic **frequency domain image processing** using **OpenCV, NumPy, and Matplotlib**.  
The experiments involve analyzing image frequency components using **Discrete Fourier Transform (DFT)** and applying various **frequency domain filters** for smoothing and sharpening.

---

## Topics Covered

### 1. DFT and Spectrum Understanding
- Loading grayscale images
- Computing **2D Discrete Fourier Transform (DFT)**
- Visualizing:
  - Original image
  - Magnitude spectrum
  - Centered log-magnitude spectrum
- Observing low-frequency dominance in natural images
- Comparing spectra of **smooth vs textured images**

---

### 2. Frequency Domain Smoothing

Implementation and analysis of **Low Pass Filters**:

- **Ideal Low Pass Filter (ILPF)**
- **Gaussian Low Pass Filter (GLPF)**
- **Butterworth Low Pass Filter (BLPF)**

Experiments include:
- Applying filters with cutoff frequencies  
  `D0 = 10, 30, 60, 120`
- Observing blur progression
- Studying ringing artifacts
- Comparing smoothness between filters
- Varying **Butterworth filter order** (`n = 1,2,4,8`)

---

### 3. Frequency Domain Sharpening

Implementation of **High Pass Filters**:

- **Ideal High Pass Filter (IHPF)**
- **Gaussian High Pass Filter (GHPF)**
- **Butterworth High Pass Filter (BHPF)** (order = 2)

Experiments include:
- Applying filters with cutoff frequency `D0 = 60`
- Comparing sharpening strength
- Observing edge enhancement
- Studying noise amplification and artifacts

---

## Tools and Libraries

- **OpenCV** – image loading and preprocessing  
- **NumPy** – FFT computation and filter operations  
- **Matplotlib** – visualization of spectra, filters, and outputs

---

## Output

For each experiment, results were visualized using **Matplotlib**, including:

- Frequency spectra
- Filter masks
- Filtered images
- Sharpened outputs

###### To view and edit on Kaggle  
[Open the notebook on Kaggle](https://www.kaggle.com/code/shivsrijitverma/frequencydomainfiltering)
