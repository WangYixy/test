# FlashTCGaussian: Accelerating Gaussian Splatting with Tensor Core

## Environment Setup
To prepare the environment, 

1. Follow [3DGS](https://github.com/graphdeco-inria/gaussian-splatting) to install dependencies. 

2. Refer to the ```environment.yml``` for additional environment configuration.

## Running Comand

To convert video files from the original dataset into image files suitable for training, set the data paths in ```convertimage.py``` to your local data folder, and run，
```
python train_dash.py -s YOUR/PATH/TO/DATASET/ --optimizer_type sparse_adam
```

* ```--optimizer_type sparse_adam``` Use the Sparse Adam optimizer. 
 

## Results
The following experiment results are produced with a personal NVIDIA RTX 4090 GPU.
The average of rendering quality metrics, number of Gaussian primitives in the optimized 3DGS model, and training time, are reported. 
### 
|  scene  | PSNR | N_GS | Time (sec) |
|-----|-----|-----|-----|
| 1747834320424  | 24.47 | 376,243 | 54.0 |
| 1750342304509  | 24.88 | 392,151 | 57.2 | 
| 1748748200211  | 24.53 | 379,967 | 54.8 | 
