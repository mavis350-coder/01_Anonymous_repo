Use diffusion_llm as the base folder.

To install all dependencies:

use the environment.yaml file provided.

## Datasets
You can access the well pre-processed datasets from [[Google Drive]](https://drive.google.com/file/d/1NF7VEefXCmXuWNbnNe858WvQAkJ_7wuP/view?usp=sharing), then place the downloaded contents under `./dataset`

## Quick Demos
1. Download datasets and place them under `./dataset`
2. Tune the model and the script according to the description in the paper if needed. We provide five experiment scripts for demonstration purpose under the folder `./scripts`. For example, you can evaluate on ETT datasets by:

```bash
bash ./scripts/TimeLLM_ETTh1.sh 
```
```bash
bash ./scripts/TimeLLM_ETTh2.sh 
```
```bash
bash ./scripts/TimeLLM_ETTm1.sh 
```
```bash
bash ./scripts/TimeLLM_ETTm2.sh
```

## Detailed usage

Please refer to ```run_main.py``` for the detailed description of each hyperparameter.

For transparency, we refer the seeds we have used in the experiments. We have mainly used the seeds 2021 as it is a standard practice in https://github.com/thuml/Time-Series-Library . Apart from this, we have alternated between the seeds 2001, 1789, 0 for different experiments to preserve randomness while keeping the results reproducible. 

