# Rock-Paper-Scissors Classifier
Statistical pattern recognition system for classifying hand gestures
(rock, paper, scissors) using HSV segmentation and a Bayesian classifier.

## Pipeline
1. **Segmentation** - images are segmented by converting to HSV color space and thresholding 
on H and S channels to isolate skin regions - more robust to lighting 
variations than RGB-based methods.
2. **Feature extraction** - three geometric features are extracted 
from each binary mask, all on the same scale, no normalization needed:
- f1: ratio of white pixels in the left half
- f2: width-to-height ratio of the mask
- f3: ratio of white pixels in the left quarter
3. **Classification** - parametric Bayesian classifier (MAP rule) 
assuming Gaussian-distributed features per class.

## Results

| Metric        | Value  |
|---------------|--------|
| Test accuracy | 94.15% |
| Split         | 80/20 stratified |

## Files
- `po1.ipynb` — full implementation notebook
- `po1.pdf` — detailed project report (Serbian)

## Requirements
numpy, matplotlib, scikit-image, scikit-learn
