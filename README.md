# FlashTCGaussian: Accelerating Gaussian Splatting with Tensor Core

## Environment Setup
To prepare the environment, 

1. Follow [3DGS](https://github.com/graphdeco-inria/gaussian-splatting) to install dependencies. 

2. Refer to the ```environment.yml``` for additional environment configuration.

## Dataset Structure

Please organize your dataset according to the directory structure shown in Round 2--eval_data_pinhole.

## Running Training
Run:
```
bash run_training.sh
```
Inside run_training.sh, you may edit:
* The path to your dataset
* The name of the image folder (default: images_gt_downsampled)

Training results will be saved automatically under the output/ directory.

## Running Rendering & Evaluation
Run:
```
bash run_evaluation.sh
```

This script performs:
* Rendering test_data
* Computing evaluation metrics (PSNR)

The PSNR scores and training time (metrics.json) will be saved inside the corresponding output/ subdirectory.

## Results
All experiment results are produced using an NVIDIA RTX 4090 GPU.
