# Linear Transformations & Visualizations in python


This project illustrates the application of 2D linear transformations through practical implementations in Python using NumPy for computation and Matplotlib for visualization. The core idea is to represent transformations such as scaling, rotation, reflection, and shearing as matrix operations, and then apply them to different data structures.

To make the concepts more intuitive, the transformations are demonstrated on sample vectors as well as on point clouds and images, highlighting how linear algebra techniques directly influence geometric structures. By visualizing before-and-after effects, the project provides a clear understanding of how linear transformations work in two dimensions and how they are foundational in fields like computer graphics, computer vision, and data science.
---

## 📌 Features

* Custom transformation functions implemented from scratch
* Linear transformation properties validation (e.g., linearity: `T(u+v) = T(u) + T(v)`)
* Matrix-based transformation (`L(v) = Av`)
* Transformations applied to vector bases and image data
* Clear visualization using `matplotlib` scatter plots

---

## 🧠 Transformations Covered

### ✅ Basic Transformations

* Custom transformation via element-wise operations
* Matrix-based transformation

### 🔄 Standard 2D Linear Transformations

* Horizontal Scaling
* Reflection across Y-axis
* Stretching
* Horizontal Shearing
* Rotation
* Rotation + Stretching Combined

Each transformation is applied to:

* Basis vectors
* A 2D image represented as point clouds
* Arbitrary vectors

---

## 📁 Folder Structure

```
├── data/
│   └── image.txt            # Input file for image coordinates
├── utils.py                 # Utility file for plotting transformations
├── transformations.py       # Contains the code (main script)
└── README.md                # This file
```

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/linear-transformations.git
cd linear-transformations
```

### 2. Install Dependencies

```bash
pip install numpy matplotlib pandas
```

### 3. Run the Script

Ensure `image.txt` is in `data/` directory and then run:

```bash
python transformations.py
```

---

## 📊 Visualization

Each transformation is visualized by:

* Plotting original image coordinates (black)
* Plotting transformed image coordinates (grey)
* Showing transformed basis vectors using custom `utils.plot_transformation()`

---

## 📦 Dependencies

* `numpy`
* `matplotlib`
* `pandas`

---

## 📎 Notes

* `image.txt` is expected to contain a 2×N matrix, where N is the number of points (columns).
* All transformations use matrix multiplication (`@`) for consistency with linear algebra principles.
* `utils.py` must contain a `plot_transformation` function that takes a transformation and two vectors as input.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
