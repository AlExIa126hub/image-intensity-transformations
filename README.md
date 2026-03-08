# Image Intensity Transformations

Digital Image Processing project exploring basic intensity transformations applied to grayscale images.

The project demonstrates how pixel intensity values can be modified using different transformation functions in order to enhance contrast and highlight image details.

---

# Project Structure

```
image-intensity-transformations/
│
├── notebooks/
│   └── intensity_transformations.ipynb
│
├── data/
│   └── example_image.jpg
│
└── README.md
```

---

# Project Overview

The goal of this project is to apply several **point-wise intensity transformations** to an image and analyse how they affect the visual appearance of the image.

Intensity transformations modify pixel values directly, without considering neighbouring pixels.  
These transformations are commonly used in image enhancement tasks such as contrast adjustment and brightness manipulation.

The notebook allows the user to upload an image and applies several transformations implemented manually in Python.

---

# Implemented Transformations

The following intensity transformations are implemented.

---

## 1. Image Negative

The negative transformation inverts pixel intensities.

For an image with intensity range \([0, L-1]\), the transformation is defined as:

```
s = (L - 1) - r
```

Where:

- `r` is the original pixel intensity
- `s` is the transformed intensity
- `L` is the number of possible intensity levels

This transformation is useful for highlighting bright details in dark regions.

---

## 2. Logarithmic Transformation

Logarithmic transformations expand dark pixel values while compressing brighter ones.

The transformation is defined as:

```
s = c * log(1 + r)
```

Where:

- `r` is the input pixel value
- `c` is a scaling constant

This transformation is useful for enhancing details in darker areas of the image.

---

## 3. Gamma Transformation

Gamma transformation adjusts image brightness using a power-law relationship:

```
s = c * r^γ
```

Where:

- `r` is the input intensity
- `γ` (gamma) controls the brightness transformation

Different gamma values produce different effects:

| Gamma value | Effect |
|-------------|--------|
| γ < 1       | Brightens the image |
| γ = 1       | No change |
| γ > 1       | Darkens the image |

Multiple gamma values are tested to observe how they affect image contrast.

---

# Results

The results illustrate how different transformations affect the appearance of the image.

Observations include:

- The **negative transformation** reverses intensity values and highlights bright structures.
- **Logarithmic transformation** enhances darker regions while compressing bright areas.
- **Gamma transformation** allows flexible brightness adjustment depending on the gamma parameter.

These transformations demonstrate how simple pixel-wise operations can significantly change image contrast and visibility.

---

# Technologies Used

- Python
- NumPy
- OpenCV
- Matplotlib
- Jupyter Notebook

---

# Running the Project

Clone the repository:

```
git clone <repository-url>
```

Install dependencies:

```
pip install numpy opencv-python matplotlib
```

Launch Jupyter Notebook:

```
jupyter notebook
```

Open and run:

```
notebooks/intensity_transformations.ipynb
```

---

# Concepts Demonstrated

This project demonstrates several fundamental image processing techniques:

- Pixel-wise intensity transformations
- Image negative transformation
- Logarithmic intensity mapping
- Gamma correction
- Image enhancement
