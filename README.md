# Linear Transformations and Visualizations

This project explores **2D linear transformations** through practical coding exercises in Python. It leverages **NumPy** for computations and **Matplotlib** for visualizations. The project demonstrates how linear algebra operations (e.g., matrix multiplication) transform geometric structures, with applications in computer graphics, computer vision, and data science.

---

## Overview

- **Key Transformations**: Rotation, reflection, shearing, scaling, and combined operations.
- **Linearity Verification**: Tests axioms like `T(u + v) = T(u) + T(v)`.
- **Visual Comparison**: Side-by-side plots of original and transformed data.
- **Applications**: Applied to basis vectors, point clouds, and image data.

---

## Key Features

- **Custom Transformation Functions**: Hand-crafted implementations of linear transformations.
- **Linearity Verification**: Validates properties like `T(u + v) = T(u) + T(v)`.
- **Matrix-Based Operations**: Transformations expressed as `L(v) = A @ v`.
- **Multi-Data Support**: Works with basis vectors, point clouds, and image datasets.
- **Intuitive Visualization**: Matplotlib scatter plots for clear before-and-after comparisons.

---

## Transformations Included

### **Basic**
- Element-wise transformations
- Matrix-based transformations

### **Standard 2D Linear Transformations**
- Horizontal scaling
- Reflection across the Y-axis
- Stretching
- Horizontal shearing
- Rotation
- Rotation combined with stretching

**Each transformation is applied to**:
- Basis vectors (`e₁`, `e₂`)
- Point clouds (e.g., images from `data/image.txt`)
- Arbitrary vectors

---

## Project Structure
linear-transformations/
├── data/
│   └── image.txt            # Input file with image coordinates (2×N matrix)
├── utils.py                 # Helper functions for plotting
├── transformations.py       # Main implementation script
��── README.md                # Project documentation

---

##  Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/linear-transformations.git
cd linear-transformations

2. Install Dependencies
bashDownloadCopy code Wrappip install numpy matplotlib pandas
3. Run the Script
Ensure data/image.txt exists, then execute:
bashDownloadCopy code Wrappython transformations.py

�� Visualization Output
Each transformation generates plots that:

* Display original coordinates (black)
* Show transformed coordinates (gray)
* Highlight transformed basis vectors using utils.plot_transformation().


�� Requirements

* Python 3.x
* Libraries:

numpy
matplotlib
pandas



Install dependencies with:
bashDownloadCopy code Wrappip install numpy matplotlib pandas

 Additional Notes

* 
image.txt Format:
The file should contain a 2×N matrix where N is the number of points (e.g.,
1 0
0 1
2 3
...


* 
Matrix Operations:
All transformations use matrix multiplication (@) for consistency with linear algebra principles.

* 
Helper Function:
utils.py includes plot_transformation(A, vectors), which visualizes transformations.



�� Example Usage
pythonDownloadCopy code Wrapimport numpy as np
from utils import plot_transformation

# Rotate by theta (e.g., 45 degrees)
theta = np.pi / 4
A = np.array([
    [np.cos(theta), -np.sin(theta)],
    [np.sin(theta),  np.cos(theta)]
])

# Load points from data/image.txt (shape: 2 x N)
V = np.loadtxt('data/image.txt')

# Apply transformation
V_transformed = A @ V

# Visualize
plot_transformation(A, V)

�� License
This project is licensed under the MIT License — see the LICENSE file for details.

