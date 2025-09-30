Linear Transformations and Visualizations
This project explores 2D linear transformations through practical coding exercises in Python. Computations are driven by NumPy, while Matplotlib creates the visual representations. Key operations like rotation, reflection, and shearing are represented as matrix multiplications and applied to vectors, point sets, and images.
Through side-by-side comparisons of original and transformed visuals, the project illustrates the role of linear algebra in modifying geometric forms and its relevance to fields such as computer graphics, computer vision, and data analysis.
Key Features

* Hand-crafted functions for transformations
* Testing of linearity axioms, such as T(u + v) = T(u) + T(v)
* Transformations via matrices, L(v) = A v
* Usage on standard basis vectors and image datasets
* Intuitive plots using Matplotlib for scatter-based displays


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


