# Rock-Paper-Scissors Hand Gesture Classifier

Statistical pattern recognition system for classifying hand gestures 
(rock, paper, scissors) using HSV segmentation and a Bayesian classifier.

## Approach
Images are segmented by converting to HSV color space and thresholding 
on H and S channels to isolate skin regions — more robust to lighting 
variations than RGB-based methods. Three geometric features are extracted 
from each binary mask:
- f1: ratio of white pixels in the left half
- f2: width-to-height ratio of the mask
- f3: ratio of white pixels in the left quarter

Classification is done using a parametric Bayesian classifier (MAP rule) 
assuming Gaussian-distributed features per class.

## Results
| Metric   | Value  |
|----------|--------|
| Test accuracy | 94.15% |
| Classes  | rock, paper, scissors |
| Split    | 80/20 stratified |

## Files
- `po.ipynb` — full implementation notebook
- `report.pdf` — detailed project report (Serbian)

## Requirements
numpy, matplotlib, opencv-python, scikit-learn
