# dark_face_dataset_preprocessing

Explore point-wise transformations on low-light images to improve their quality.

The notebook `dark_image_preprocesing.ipynb` loads a dark image from `images/` and applies:

- Intensity adjustment
- Histogram equalization
- Arithmetic operators

Each technique is defined once as a function on a single channel and applied in two ways:

- **RGB per channel**: on R, G and B separately (may shift colors).
- **Luminance**: on the V channel of HSV, keeping H and S (preserves color).

Results are compared visually with histograms, plus mean, standard deviation and Shannon entropy of the luminance.

## How to run

1. Install the dependencies:

   ```bash
   pip install opencv-python numpy matplotlib jupyter
   ```

2. Open the notebook and run all cells:

   ```bash
   jupyter notebook dark_image_preprocesing.ipynb
   ```

Sample images are in `images/`. To use another image, change the path in the load cell (e.g. `images/225.png`).

## Dataset

Images come from the DARK FACE dataset:

Soumik Rakshit, *Dark Face Dataset*, Kaggle. https://www.kaggle.com/datasets/soumikrakshit/dark-face-dataset

Original work: Yuan, Ye, et al. "UG²+ Track 2: A Collective Benchmark Effort for Evaluating and Advancing Image Understanding in Poor Visibility Environments." arXiv:1904.04474, 2019.
