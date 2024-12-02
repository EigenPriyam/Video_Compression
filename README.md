# Video Compression Using Unsupervised Learning

This project focuses on compressing videos using unsupervised learning techniques. Key frames are identified through shot boundary detection, and color quantization using k-means clustering is applied to achieve effective compression while preserving visual quality.

---

## Features

### Key Highlights:
- **Image Compression**:
  - Developed an algorithm for image compression and decompression using k-means clustering for color quantization.
  
- **Shot Boundary Detection**:
  - Used techniques such as:
    - PySceneDetect
    - Histogram difference
    - Optical flow calculation
    - Clustering based on frame features

- **Key Frame Detection**:
  - Extracted key frames from videos using shot boundary detection.

- **Video Compression**:
  - Reduced the number of frames by 50\% using key frame extraction.
  - Applied color quantization with 64 clusters per frame.
  - Achieved:
    - **40\% reduction in video size**
    - **Mean Squared Error (MSE)**: 0.02
    - **Signal-to-Noise Ratio (SNR)**: 25 dB

---

## Project Workflow

### Step 1: Video Analysis and Preprocessing
1. Load the input video.
2. Perform shot boundary detection using:
   - PySceneDetect
   - Histogram differences
   - Optical flow
3. Identify key frames based on detected boundaries.

### Step 2: Key Frame Extraction
1. Extract and save key frames from the video.
2. Use these key frames for further processing to reduce redundancy.

### Step 3: Color Quantization
1. Apply k-means clustering for color quantization on each key frame:
   - Set the number of clusters to 64.
   - Replace pixel colors with the nearest cluster center.
2. Save the compressed key frames.

### Step 4: Reconstruction
1. Reconstruct the video using the compressed key frames.
2. Apply interpolation if needed to smooth transitions between key frames.

---

## Results
- Video size reduced by **40\%** with **50\% frame reduction**.
- Achieved an average:
  - **MSE (Mean Squared Error)**: 0.02
  - **SNR (Signal-to-Noise Ratio)**: 25 dB

---

## Requirements

### Python Libraries:
Install the required dependencies using pip:
```bash
pip install numpy scipy opencv-python scikit-learn pyscenedetect
