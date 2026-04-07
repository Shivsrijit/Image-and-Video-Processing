# IVP Lab: Feature Extraction and Matching

This project explores two fundamental methods for extracting and matching features from images: **Histogram of Oriented Gradients (HOG)** and **Scale-Invariant Feature Transform (SIFT)**. These techniques are essential for tasks like object detection, image stitching, and robotic vision.

---

## I. HOG (Histogram of Oriented Gradients)
HOG is a structural descriptor used to capture the "shape" of objects within an image by summarizing the distribution of intensity gradients.

* **Gradient Computation:** Utilizes **Sobel operators** to calculate the horizontal and vertical derivatives ($G_x$ and $G_y$), which are then converted into edge magnitude and direction.
* **Orientation Binning:** Pixels "vote" into a 9-bin histogram ($0^\circ$ to $180^\circ$) where the weight of the vote is determined by the gradient magnitude.
* **Cell & Block Structure:** The image is divided into small local grids called **Cells** (typically $8 \times 8$ pixels). These are further grouped into larger **Blocks** ($2 \times 2$ cells).
* **Block Normalization:** Employs the **L2-norm** to normalize feature vectors within a block. This ensures the descriptor is resistant to changes in lighting and contrast.
* **Feature Descriptors:** The final output is a flattened 1D vector that represents the entire image's structural information.

---

## II. SIFT (Scale-Invariant Feature Transform)
SIFT is a robust algorithm used to detect and describe local features that are invariant to scaling, rotation, and illumination.

* **Scale-Space Extrema:** Identifies potential interest points (blobs/corners) by looking for local maxima/minima across different blur levels using **Difference of Gaussians (DoG)**.
* **Keypoint Localization:** Refines the list of points by discarding those with low contrast or those poorly localized along edges (filtering out noise).
* **Orientation Assignment:** Each keypoint is assigned a "master direction" based on local gradient orientations, ensuring the descriptor is **rotation-invariant**.
* **128-Dimensional Descriptors:** The neighborhood around a keypoint is summarized into a unique "digital fingerprint"—a 128-element vector used for high-accuracy matching.

---

## III. Image Transformations & Matching
Techniques used to simulate real-world changes and verify the strength of the feature extractors.

* **Affine Transformations:** Specifically using **Rotation Matrices** to simulate camera movement or object orientation changes.
* **Feature Matching:** Utilizing the **Brute-Force (BF) Matcher** to compare descriptors between two different images.
* **Distance Metrics:** Use of **Euclidean ($L2$) distance** to quantify the similarity between feature vectors.
* **Filtering Matches:** Implementing **cross-checking** and distance-based sorting to ensure only the most accurate point pairs are identified.

###### To view and edit on Kaggle  
[Open the notebook on Kaggle](https://www.kaggle.com/code/shivsrijitverma/feature-extraction-and-matching)

