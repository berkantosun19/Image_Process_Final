 Image Processing Tasks with Jupyter Notebook

This repository contains several basic image processing tasks implemented in Python using Jupyter Notebook. It focuses on techniques such as unsharp masking (in both spatial and frequency domains), noise analysis and removal, and contrast enhancement.

 How to Run This Notebook

 Clone the Repository

Make sure you have Git installed, then open Git Bash and type:


git clone https://github.com/berkantosun19/Image_Process_Final.git
cd Image_Process_Final

 Setup Python Environment

I recommend using a virtual environment:

python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate

 Install Required Libraries

You can install the necessary libraries with:

pip install opencv-python matplotlib numpy


Files & Usage

- The Jupyter Notebooks are found in the root directory.
- The images (`einstein.tif`, `moon.jpg`, `pcb.tif`, etc.) must be located in the same folder as the notebooks or in an `images/` subfolder depending on how the paths are set in each notebook.
- You can launch Jupyter Notebooks with:

jupyter notebook

Then open and run each cell step by step.

---
Notes on Each Task

- Pollen Image
  Checked and fixed low contrast using histogram equalization and CLAHE. Compared both methods to see which improved the image better.

- Einstein Image  
  This notebook shows unsharp masking in both spatial and frequency domain using different `k` values. You'll see how high-boost filtering sharpens edges, and we compare spatial vs. frequency domain results side by side.

-Moon Image  
  Another unsharp masking exercise but focusing on observing the effect of different `k` values in more detail. Uses both Gaussian blur and high-pass filters.

- Pout Image  
  This image is used for intensity transformation, showing contrast stretching and histogram equalization for enhancement.

- PCB Image  
  This task detects the type of noise visually and via histogram, then removes it using filters (median or Gaussian), depending on whether the noise is salt-and-pepper or Gaussian.

- Engineer Image  
  Focuses on spatial filtering techniques like Laplacian, unsharp masking, and high-boost filtering.

---

Common Error Note

If you get this error when running a cell like `plt.imshow(image, cmap='gray')`:

TypeError: Image data of dtype object cannot be converted to float

It usually means your image path is wrong and the image failed to load (i.e., `image` is `None`). Make sure the image file exists in the same directory or adjust the path accordingly.

---

Name : Berkan
Surname : Tosun
Student ID : B2280.011010
