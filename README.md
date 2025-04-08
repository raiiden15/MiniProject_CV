# MiniProject_CV
## SIFT Feature Matching – Taj Mahal (Different Viewpoints)

## 🔍 Project Overview
This project explores different computer vision algorithms to detect and compare feature points in high-resolution images. Specifically, we apply:
**SIFT (Scale-Invariant Feature Transform)**
**Shi-Tomasi Corner Detection** 
**FAST algorithm for Corner Detection** 

## 📸 Images Used

Two real-world images of the **Taj Mahal**:
- `tajMahal.jpg` – Frontal view
- `tajMahal2.jpg` – Angled/side view
- `Cube.jpg`  - A manually taken image of Cube, removed background.
  
These images are ideal for testing SIFT because:
- They include rich textures and structural details
- The viewpoints differ, testing scale and rotation invariance

The Cube image is ideal for FAST and Shi Thomas, since it is taken from an angle where many corners are visible 
---

## 🧠 Algorithms Used

### 1. ✅ SIFT Feature Matching

- **Detects** and **matches** keypoints between two different views of the Taj Mahal
- Uses Lowe’s ratio test to filter false matches
- Visualizes strong, consistent matches across scales and angles

📁 Output:
``matches_taj.png``

> Above: Matched keypoints correctly align the domes, arches, and edges of the Taj Mahal in both images, despite the difference in viewpoint. Also matched the trees to grasses (lol) 

---

### 2. ⚡ FAST Corner Detection (Best for Large Images)

- Ideal for high-resolution images (like 4000x4000)
- FAST detects **hundreds to thousands of corners** almost instantly
- No descriptor generation – just raw keypoint localization

📁 Output:
``fast_algo_cube.png``

### 3. Shi-Tomasi Corner Detection

- Very **precise** for clean images (used on a resized cube image)  
- Uses `cv2.goodFeaturesToTrack`  
- Slower on large images; needs resizing 

📁 Output:
``shi_thomas_cube.png``

## 📁 Files

- `implementations.ipynb`: Python script using OpenCV's SIFT implementation
- `tajMahal.jpg`, `tajMahak1.jpg`: Input images
- `results/matches_taj.png`: Output with matched keypoints
- `result/shi_thomas_cube.png`: Output of Shi Thomas Corner Detection 
- `results/fast_algo_cube.png`: Output of Fast Algorithm for corner detection
- `README.md`: You're reading it 😊

---


## 📊 Output Comparison

| Algorithm     | Speed        | Accuracy      | High-Res Compatible | Corners/Matches |
|---------------|--------------|---------------|----------------------|-----------------|
| **FAST**      | 🚀 Very Fast | ⚠️ Medium     | ✅ Yes               | ~800            |
| **Shi-Tomasi**| 🐢 Slower    | ✅ High       | ⚠️ Needs Resizing    | ~100            |
| **SIFT**      | ⚡ Moderate   | ✅✅ Very High | ✅ Yes               | Matched Points  |


## 🧠 Conclusion

- 🔹 **FAST** is great for speed and high-res images but less accurate.  
- 🔹 **Shi-Tomasi** gives better corner precision but slows down on large images.  
- 🔹 **SIFT** is best for matching across different views and transformations.  


