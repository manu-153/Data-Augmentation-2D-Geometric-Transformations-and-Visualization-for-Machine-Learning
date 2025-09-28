Linear Transformations & Visualizations
This project demonstrates 2D linear transformations with hands-on implementations in Python. NumPy powers the computations and Matplotlib handles the visualizations. Transformations such rotation, reflection, and shearing are expressed as matrix operations and applied to vectors, point clouds, and images.
By comparing before-and-after visuals, the project highlights how linear algebra shapes geometric structures and its applications in computer graphics, computer vision, and data science.

Features

* Custom-built transformation functions
* Verification of linearity properties T(u+v)=T(u)+T(v)
* Matrix-based transformations L(v)=Av
* Applications on basis vectors and image data
* Clear visualizations with Matplotlib scatter plots


Transformations Included
Basic

* Element-wise transformations
* Matrix-based transformations

Standard 2D Linear Transformations

* Horizontal scaling
* Reflection across the Y-axis
* Stretching
* Horizontal shearing
* Rotation
* Rotation combined with stretching

Each transformation is applied to:

* Basis vectors
* Point clouds representing images
* Arbitrary vectors


Project Structure
├── data/
│   └── image.txt            # Input file with image coordinates
├── utils.py                 # Helper functions for plotting
├── transformations.py       # Main implementation script
└── README.md                # Documentation


Getting Started

1. Clone the repository

bashDownloadCopy code Wrapgit clone https://github.com/yourusername/linear-transformations.git
cd linear-transformations

1. Install dependencies

bashDownloadCopy code Wrappip install numpy matplotlib pandas

1. Run the script

Make sure image.txt is in the data/ directory, then run:
bashDownloadCopy code Wrappython transformations.py

Visualization Output
Each transformation is visualized by:

* Plotting original coordinates (black)
* Plotting transformed coordinates (grey)
* Displaying transformed basis vectors using utils.plot_transformation()


Requirements

* numpy
* matplotlib
* pandas

Install with:
bashDownloadCopy code Wrappip install numpy matplotlib pandas

Additional Notes

* image.txt should contain a 2×N matrix, where N is the number of points.
* All transformations rely on matrix multiplication (@) for consistency with linear algebra.
* utils.py must include a plot_transformation function that takes a transformation and vectors as input.


Example Usage (snippet)
Include or adapt into your own script:
pythonDownloadCopy code Wrapimport numpy as np
from utils import plot_transformation

# Example transformation: rotate by theta
theta = np.pi / 4
A = np.array([[np.cos(theta), -np.sin(theta)],
              [np.sin(theta),  np.cos(theta)]])

# Apply to a set of points V (2 x N)
V_transformed = A @ V

# Visualize
plot_transformation(A, V)

License
This project is licensed under the MIT License — see the LICENSE file for details.


