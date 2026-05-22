# CNN Architecture Comparison on CIFAR-10

Comparing CNN architectures on the CIFAR-10 dataset to analyze the effect of 
architecture depth and design on image classification performance.

## Architectures Compared
| Architecture | Test Accuracy | Trainable Parameters | Training Time |
|---|---|---|---|
| Baseline CNN | 74.16% | 620,810 | 254.05s |
| ResNet18 | 67.23% | 11,181,642 | 306.58s |
| VGG11 | 60.09% | 9,359,882 | 290.77s |

## Key Finding
The Baseline CNN outperforms both ResNet18 and VGG11 on CIFAR-10. 
ResNet18 and VGG11 are designed for large images (224x224) and underperform 
on small 32x32 images due to aggressive downsampling.

## Setup
1. Clone the repo
2. Install dependencies: `pip install -r requirements.txt`
3. Run notebooks in `notebooks/` folder on Google Colab with T4 GPU

## Dataset
CIFAR-10 — 60,000 images across 10 classes, loaded via torchvision. 
No manual download needed.

## Hardware
All experiments run on Google Colab T4 GPU for consistency.