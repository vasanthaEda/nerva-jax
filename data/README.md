# Dataset Preparation Script

This directory contains `prepare_data.py`, a utility script for downloading, preprocessing, and saving datasets used by the `mlp` training tool and others in this project.

## Supported Datasets

- **MNIST** (28x28 grayscale images of handwritten digits)
- **CIFAR-10** (32x32 color images from 10 categories)

## Usage

You can automatically download and preprocess a dataset using the `--download` flag:

```bash
python prepare_data.py --dataset=mnist --download
python prepare_data.py --dataset=cifar10 --download
```

This will:

*   Download the dataset to the current directory (or to `--data-dir` if specified),
*   Flatten and normalize the image data,
*   Save the result in a compressed .npz file: `mnist-flattened.npz` or `cifar10-flattened.npz`.

If the required .npz files already exist, the script will detect this and skip reprocessing. The generated .npz files can be used as input for the `mlp` command line tool.

## Maintainer

This project is maintained by Manmohan S., a Supply Chain Analyst with over 4 years of experience in data analysis, inventory planning, and operational reporting. With a focus on leveraging Python and SQL to improve operational visibility, this utility serves as part of a broader toolkit for streamlining data preparation workflows.

Contact:
- Email: manmohansangola1@gmail.com
- LinkedIn: https://www.linkedin.com/in/manmohan-sangola/