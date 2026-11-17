# MS COCO Image Captioning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?logo=python&logoColor=white)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-CNN%20%2B%20RNN-6A1B9A)
![Dataset](https://img.shields.io/badge/Dataset-MS%20COCO-FF6F00)
![Platform](https://img.shields.io/badge/Platform-Kaggle-20BEFF?logo=kaggle&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Development-orange)

An end-to-end computer vision project for generating natural-language descriptions of images using a CNN-RNN architecture.

</div>

## Overview

This project explores automatic image captioning with the MS COCO dataset. A convolutional neural network is intended to extract visual features from an image, while a recurrent neural network decodes those features into a sequence of words.

The repository currently includes the initial Kaggle environment setup and COCO annotation-loading workflow. The model pipeline and evaluation are under active development.

## Key Features

- Loads MS COCO train images and annotation data
- Builds a Kaggle-compatible feature extraction workspace
- Uses NumPy and tqdm for numerical processing and progress tracking
- Provides a foundation for CNN-based visual encoding
- Includes a clear development path toward RNN/LSTM caption generation

## Project Architecture

```text
Input Image
    |
    v
CNN Feature Extractor
    |
    v
Encoded Image Representation
    |
    v
RNN / LSTM Decoder
    |
    v
Generated Caption
```

## Dataset

This project uses the [MS COCO 2014](https://cocodataset.org/) dataset.

Expected Kaggle paths:

```text
/kaggle/input/datasets/hariwh0/ms-coco-dataset/train2014/train2014
/kaggle/input/datasets/hariwh0/ms-coco-dataset/captions/annotations/captions_train2014.json
```

Extracted features are written to:

```text
/kaggle/working/features
```

## Technologies

- Python
- NumPy
- tqdm
- TensorFlow or PyTorch (planned)
- Kaggle Notebooks
- MS COCO 2014

## Getting Started

### Run on Kaggle

1. Upload `file_RNN_CNN.ipynb` to Kaggle.
2. Add the `hariwh0/ms-coco-dataset` dataset.
3. Enable the notebook's GPU accelerator, if available.
4. Run all cells.

### Run locally

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

Update `DATASET_PATH` in the notebook to the location of your local MS COCO installation.

## Repository Structure

```text
MS-COCO-Image-Captioning/
|-- file_RNN_CNN.ipynb
|-- README.md
|-- requirements.txt
`-- .gitignore
```

## Development Roadmap

- [x] Set up Kaggle dataset paths
- [x] Load and inspect COCO annotations
- [ ] Preprocess and tokenize captions
- [ ] Extract image features with a pretrained CNN
- [ ] Build an RNN/LSTM caption decoder
- [ ] Train and tune the model
- [ ] Add qualitative caption examples
- [ ] Evaluate with BLEU and CIDEr metrics

## Resume Summary

> Developed a Kaggle-based data pipeline for MS COCO image captioning, establishing the dataset integration and project foundation for a planned CNN feature encoder and RNN/LSTM sequence decoder.

## Contributing

Suggestions and contributions are welcome. Please open an issue before submitting a substantial change.

## Author

**Abdullah Mahmoud**

- GitHub: [@Abdullah-Mahmoud557](https://github.com/Abdullah-Mahmoud557)
