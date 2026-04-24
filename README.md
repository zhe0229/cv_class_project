# CV Course Project: Image Super-Resolution with Real-ESRGAN

This repository contains our computer vision course project based on Real-ESRGAN. The project focuses on image super-resolution and restoration, with additional experiments, inputs, outputs, and analysis files collected during coursework.

## Project Overview

The goal of this project is to explore how deep learning can improve low-quality images by recovering sharper details and producing higher-resolution outputs. We used the Real-ESRGAN framework as the main baseline and organized our own experiments around it.

Main tasks in this repository include:

- running image super-resolution inference
- testing different input domains and degradation settings
- comparing restoration results across examples
- documenting outputs for course presentation or report writing

## Repository Structure

Key folders and files:

- `realesrgan/`: core model code
- `inference_realesrgan.py`: main inference script for images
- `inference_realesrgan_video.py`: inference script for videos
- `weights/`: pretrained model weights
- `inputs/`: sample input data
- `results/`: generated output images
- `paper_inputs/`: inputs prepared for project analysis
- `paper_results/`: figures and outputs used in experiments
- `baseline_experiment.ipynb`: notebook for project experiments
- `tests/`: test files and sample test data

## Environment Setup

Recommended environment:

- Python 3.8+
- PyTorch
- pip or conda

Install dependencies:

```bash
pip install -r requirements.txt
python setup.py develop
```

## How to Run

Run image super-resolution on the default input folder:

```bash
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs -o results
```

Run with face enhancement if needed:

```bash
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs -o results --face_enhance
```

The restored images will be saved in the `results/` directory.

## Project Outputs

This repository also includes:

- experiment notebooks
- prepared datasets and sample images
- generated figures for analysis
- intermediate and final restoration outputs

These materials were kept in the repository to support the course report and presentation workflow.

## Notes

- The repository contains pretrained weights and generated outputs, so the project size is relatively large.
- Some folders include experiment artifacts created during development and analysis.
- This project is intended for academic coursework and demonstration purposes.

## Acknowledgement

This project is built on top of the original Real-ESRGAN work:

- Real-ESRGAN: https://github.com/xinntao/Real-ESRGAN

We adapted the framework and project files for course use, experiments, and reporting.
