# Image Compression with Singular Value Decomposition (SVD)

## Introduction
Singular Value Decomposition (SVD) is a mathematical technique for factorizing a matrix into three components: **U**, **Σ (Sigma)**, and **Vᵀ**. SVD can be used for image compression by reducing the rank of the image matrix, effectively retaining the most important features while discarding less significant information.

---

## Dataset
This project uses an example image for compression and analysis. The input image is converted to grayscale for simplicity, but the same method can be extended to RGB images by applying SVD to each color channel separately.

- **Input Format**: Grayscale PNG/JPG
- **Resolution**: Variable
- **Channels**: 1 (grayscale) or 3 (RGB)

---

## Algorithm
### Singular Value Decomposition (SVD)
For a grayscale image represented as a matrix **A**:
- **A = UΣVᵀ**
  - **U**: Left singular vectors (captures row relationships)
  - **Σ**: Diagonal matrix of singular values (represents image features)
  - **Vᵀ**: Right singular vectors (captures column relationships)

### Compression Steps
1. Perform SVD on the image matrix.
2. Retain the top `k` singular values to reconstruct the image.
3. Compute the compression ratio and reconstruction error for analysis.

---

## Implementation
The implementation includes:
1. **Image Loading**:
   - Handles images with 4 channels (RGBA) by removing the Alpha channel.
   - Converts RGB images to grayscale for processing.
2. **SVD Compression**:
   - Decomposes the image matrix into `U`, `Σ`, and `Vᵀ`.
   - Reconstructs the image using the top `k` singular values.
3. **Metrics**:
   - **Compression Ratio**: Measures how effectively the image size is reduced.
   - **Reconstruction Error**: Quantifies the quality loss after compression.
4. **Visualization**:
   - Displays the original and compressed images for different `k` values.
   - Outputs metrics for each compression level.

---

## Results
### Visualization
1. **Original Image**:
   - Displays the input image in grayscale.
2. **Compressed Images**:
   - Shows reconstructed images using different values of `k` (e.g., 5, 20, 50, 100).


### Observations
- **Compression Ratio** decreases as `k` increases.
- **Reconstruction Error** decreases as more singular values are used.


