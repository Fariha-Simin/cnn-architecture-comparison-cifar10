# CNN Architecture Comparison on CIFAR-10 and CIFAR-100

Comparing CNN architectures on CIFAR-10 and CIFAR-100 datasets to analyze 
the effect of architecture depth and design on image classification performance.

## Architectures Compared
| Architecture | Dataset | Test Accuracy | Trainable Parameters | Training Time |
|---|---|---|---|---|
| Baseline CNN | CIFAR-10 | 74.16% | 620,810 | 254.05 seconds(4.234 minutes) |
| ResNet18 | CIFAR-10 | 67.23% | 11,181,642 | 306.58 seconds(5.10966667 minutes) |
| VGG11 | CIFAR-10 | 60.09% | 9,359,882 | 290.77 seconds(4.84616667 minutes) |
| Baseline CNN | CIFAR-100 | 39.05% | 620,810 | 257.80 seconds(4.29666667 minutes) |
| ResNet18 | CIFAR-100 | 31.25% | 11,227,812 | 321.36305.75 seconds(5.09583333 minutes) |
| VGG11 | CIFAR-100 | 10.45% | 93,83,012 | 278.19 seconds(4.6365 minutes) |

## Key Findings
- Baseline CNN outperforms ResNet18 and VGG11 on both datasets
- ResNet18 and VGG11 are designed for large images (224x224) and underperform 
on small 32x32 images due to aggressive downsampling
- All architectures show significant accuracy drop on CIFAR-100 due to 
10x less training samples per class and harder fine-grained categories

## Setup
1. Clone the repo
2. Install dependencies: `pip install -r requirements.txt`
3. Run notebooks in `notebooks/` folder on Google Colab with T4 GPU

## Dataset
- **CIFAR-10** — 60,000 images, 10 classes
- **CIFAR-100** — 60,000 images, 100 classes
- Both loaded via torchvision, no manual download needed

## Hardware
All experiments run on Google Colab T4 GPU for consistency.