# MS COCO Image Captioning

This repository contains a Kaggle notebook for loading and working with the MS COCO 2014 image-caption dataset.

## Overview

The current notebook:

- Loads training annotations from `captions_train2014.json`
- Defines paths for the training images and generated features
- Creates a feature-output directory
- Prints the top-level keys found in the COCO annotation JSON

The recorded annotation keys are:

```text
dict_keys(['info', 'images', 'licenses', 'annotations'])
```

## Results

The training run produced a training/validation loss curve over 10 epochs. The lowest recorded validation loss was **2.0831**, at **epoch 10**.

![Training versus validation loss](assets/training_curves.png)

## Caption Examples

The following examples compare beam-search-generated captions with human-reference captions.

### Example 1

![Beam-search and human-reference captions for a computer workstation](assets/caption_example_2.png)

### Example 2

![Beam-search and human-reference captions for horses in a field](assets/caption_example_3.png)

### Example 3

![Beam-search and human-reference captions for a kitchen](assets/caption_example_4.png)

### Example 4

![Beam-search and human-reference captions for people playing a video game](assets/caption_example_5.png)

### Example 5

![Beam-search and human-reference captions for a slice of cake](assets/caption_example_6.png)

### Example 6

![Beam-search and human-reference captions for surfers in the ocean](assets/caption_example_7.png)

## Dataset

The notebook uses the following Kaggle dataset paths:

- Dataset: `/kaggle/input/datasets/hariwh0/ms-coco-dataset`
- Training images: `/kaggle/input/datasets/hariwh0/ms-coco-dataset/train2014/train2014`
- Training captions: `/kaggle/input/datasets/hariwh0/ms-coco-dataset/captions/annotations/captions_train2014.json`
- Generated features: `/kaggle/working/features`

## Notebook

The repository notebook is `file_RNN_CNN.ipynb`.

It imports:

- `os`
- `json`
- `random`
- `numpy`
- `tqdm`

For the loss curve, the notebook uses Matplotlib and calculates the epochs from the recorded training history.

## Running the Notebook

1. Open `file_RNN_CNN.ipynb` in Kaggle.
2. Add the `hariwh0/ms-coco-dataset` dataset.
3. Run the notebook with the configured dataset paths.

The existing notebook requires access to `captions_train2014.json` at the Kaggle path shown above.

## Repository Structure

```text
MS-COCO-Image-Captioning/
|-- assets/
|   |-- caption_example_2.png
|   |-- caption_example_3.png
|   |-- caption_example_4.png
|   |-- caption_example_5.png
|   |-- caption_example_6.png
|   |-- caption_example_7.png
|   `-- training_curves.png
|-- file_RNN_CNN.ipynb
|-- README.md
|-- requirements.txt
`-- .gitignore
```
