# Hybrid Content-Based Image Retrieval (CBIR) 🔍

A robust computer vision system that retrieves visually similar images from a database by combining local keypoint descriptors with global color and shape features.

## 🚀 Core Features & Algorithms
1. **Local Features (SIFT + RANSAC):** 
   - Extracts Scale-Invariant Feature Transform (SIFT) keypoints.
   - Uses Brute-Force KNN matching with Lowe's ratio test.
   - Applies RANSAC to compute Homography and filter out geometric outliers (inliers counting).
2. **Color Features (HSV Histogram):** 
   - Removes background using Gaussian Blur and Otsu's Adaptive Thresholding.
   - Computes normalized HSV color histograms and measures similarity using Histogram Intersection.
3. **Shape Features (Hu Moments):** 
   - Extracts 7 log-transformed Hu Moments from the object mask.
   - Measures shape similarity using the Inverse Euclidean Distance.
4. **Hybrid Scoring Engine:** 
   - Normalizes and fuses SIFT, Color, and Shape scores using a weighted mathematical model to rank the top matched images.

## 🛠️ Technologies
- Python 3
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## 📂 Repository Structure
- `Hybrid_CBIR_System.ipynb`: The main executable Jupyter Notebook containing the database construction and retrieval logic.
- `database/`: Contains 60 sample dataset images.
- `query/`: Contains sample query images for testing.

## 📊 Result Visualization
*(Upload a screenshot of your Matplotlib output grid showing the Query Image and Top 5 matches here)*
