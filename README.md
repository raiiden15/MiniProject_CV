# MiniProject_CV
## SIFT Feature Matching – Taj Mahal (Different Viewpoints)

## 🔍 Project Overview
This project explores different computer vision algorithms to detect and compare feature points in high-resolution images. Specifically, we apply:
**SIFT (Scale-Invariant Feature Transform)**
**Shi Thomas Corner Detection**
**FAST algorithm for Corner Detection** 

**SIFT**
By extracting and comparing scale- and rotation-invariant features from both images, we show how SIFT can accurately map corresponding structures—even when the viewpoints and perspectives vary.
---
## 📸 Images Used

Two real-world images of the **Taj Mahal**:
- `tajMahal.jpg` – Frontal view
- `tajMahal2.jpg` – Angled/side view
- `Cube.jpg`  - A manually taken image of Cube, removed background.
- 
These images are ideal for testing SIFT because:
- They include rich textures and structural details
- The viewpoints differ, testing scale and rotation invariance
-
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
``fast_corners_tajmahal.png``

## 📁 Files

- `sift_tajmahal.py`: Python script using OpenCV's SIFT implementation
- `taj1.jpg`, `taj2.jpg`: Input images
- `results/matches_taj.png`: Output with matched keypoints
- `results/fast_algo_cube.png`: Output of Fast Algorithm for corner detection
- `README.md`: You're reading it 😊

---

## 💡 Key Takeaway

SIFT's ability to detect scale- and rotation-invariant features makes it ideal for real-world use cases like object recognition, panoramic stitching, and 3D reconstruction—even with images taken from different angles and distances.

---

## 🔧 Requirements

- Python 3.x
- OpenCV (with `opencv-contrib-python` for SIFT support)
- Matplotlib (for visualization)

Install dependencies:
```bash
pip install opencv-contrib-python matplotlib
