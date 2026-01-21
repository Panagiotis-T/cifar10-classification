# CIFAR-10 Image Classification

This repository contains implementations of CIFAR-10 image classification using TensorFlow and Keras. The project explores two approaches: a custom Convolutional Neural Network (CNN) and transfer learning with MobileNetV2.

## Dataset

CIFAR-10 consists of 60,000 32x32 color images in 10 classes (airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck), with 6,000 images per class. There are 50,000 training images and 10,000 test images.

## Notebooks

### 1. `cifar10_cnn.ipynb`
- Implements a custom CNN from scratch.
- Includes data preprocessing, augmentation, model training, evaluation, and visualization.

### 2. `cifar10_mobilenetv2_transfer_learning.ipynb`
- Uses MobileNetV2 pre-trained on ImageNet with transfer learning.
- Includes feature extraction and fine-tuning phases.
- Demonstrates significant improvement with fine-tuning.
- Saved models are included in the `models/` directory.

## Requirements

- Python >= 3.11
- Dependencies listed in `pyproject.toml`

Install with uv:
```bash
uv sync
```

## Usage

Activate the environment:

```bash
uv run jupyter notebook
```


## Results

- **Custom CNN**: Accuracy on 100 random test samples: 60.00%
- **MobileNetV2 Transfer Learning**: Accuracy on 100 random test samples: 96.00%

## Project Structure

```
.
├── cifar10_cnn.ipynb                    # Custom CNN implementation
├── cifar10_densenet_transfer_learning.ipynb  # Transfer learning with MobileNetV2
├── models/                              # Saved Keras models
│   ├── mobilenetv2_base.keras
│   └── mobilenetv2_finetuned.keras
├── pyproject.toml                       # Project dependencies
└── uv.lock                              # Lock file
```

## License

MIT License
