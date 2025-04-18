# Visual Odometry + 3D Scene Reconstruction

This project implements a **classical monocular Visual Odometry (VO)** pipeline with optional **sparse 3D reconstruction** using triangulation — all in Python using OpenCV and Open3D. It is designed to work both **locally** and in the cloud via Binder.

> ORB Keypoints → Feature Matching → Essential Matrix → Pose Recovery → Trajectory Estimation → Triangulation

---

## What It Does

- Tracks camera motion from a sequence of monocular images  
- Plots a live 2D trajectory of the camera  
- Optionally reconstructs a sparse 3D point cloud using matched features  
- Shows dynamic feature tracking between frames  
- Runs fully on classical geometry (no learning, no deep models)

---

## Dataset

- Uses the **KITTI Odometry Dataset**  
- You can try a sample subset included (recommended for Binder), or run the full sequence locally

> `sample_data/` folder contains a subset of Sequence 00 for demo

---

## Try It in Your Browser (Binder)

Click below to launch the project **without any installation**:

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/DurgaDeepakValluri/VO-3D-Scene-Reconstruction/HEAD?urlpath=tree/Visual%20Odometry%20%2B%203D%20Scene%20Reconstruction%20%28Binder%20Version%29.ipynb)

> ⚠️ **Note:** While Binder lets you run the notebook online, it may experience issues with live plotting and rendering in some sessions. For best performance, we recommend running locally.

---

## Running Locally (Recommended)

1. **Clone the repo:**
   ```bash
   git clone https://github.com/DurgaDeepakValluri/VO-3D-Scene-Reconstruction.git
   cd VO-3D-Scene-Reconstruction
   ```

2. **Set up the environment:**
   ```bash
   conda env create -f environment.yml
   conda activate vo_env
   ```

3. **Launch the notebook:**
   ```bash
   jupyter notebook
   ```

4. Open the `Visual Odometry + 3D Scene Reconstruction.ipynb` (local version)

> The local version includes OpenCV visualizations like `cv2.imshow()` and native Open3D 3D viewers.

---

## Tech Stack

- Python 3.8  
- OpenCV (`cv2`)  
- NumPy, Matplotlib, Pandas  
- Open3D (for 3D visualization)  
- KITTI Dataset (Sequence 00)  
- Jupyter Notebook / Binder

---

## Notebooks

| Notebook                                             | Description                                 |
|------------------------------------------------------|---------------------------------------------|
| `Visual Odometry + 3D Scene Reconstruction.ipynb`    | Full-featured version for local use         |
| `Visual Odometry + 3D Scene Reconstruction (Binder Version).ipynb` | Binder-friendly version with inline plots  |

---

## Outputs

- Live camera trajectory (2D)  
- Live sparse point cloud (3D)  
- Per-frame feature matches  
- FPS, frame time, inlier ratios  
- Optional `.npy` and `.csv` output saving

---

## Acknowledgements

- [KITTI Dataset](http://www.cvlibs.net/datasets/kitti/)
- OpenCV & Open3D communities
- VO structure inspired by classic robotics curricula

---

## License

This project is licensed under the MIT License.
```
