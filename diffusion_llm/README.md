<div align="center">
  <!-- <h1><b> Time-LLM </b></h1> -->
  <!-- <h2><b> Time-LLM </b></h2> -->
  <h2><b> (ICLR'24) Time-LLM: Time Series Forecasting by Reprogramming Large Language Models </b></h2>
</div>

<div align="center">

![](https://img.shields.io/github/last-commit/KimMeen/Time-LLM?color=green)
![](https://img.shields.io/github/stars/KimMeen/Time-LLM?color=yellow)
![](https://img.shields.io/github/forks/KimMeen/Time-LLM?color=lightblue)
![](https://img.shields.io/badge/PRs-Welcome-green)

</div>

<div align="center">

**[<a href="https://arxiv.org/abs/2310.01728">Paper Page</a>]**
**[<a href="https://www.youtube.com/watch?v=6sFiNExS3nI">YouTube Talk 1</a>]**
**[<a href="https://www.youtube.com/watch?v=L-hRexVa32k">YouTube Talk 2</a>]**
**[<a href="https://medium.com/towards-data-science/time-llm-reprogram-an-llm-for-time-series-forecasting-e2558087b8ac">Medium Blog</a>]**

**[<a href="https://www.jiqizhixin.com/articles/2024-04-15?from=synced&keyword=TIME-LLM">机器之心中文解读</a>]**
**[<a href="https://mp.weixin.qq.com/s/UL_Kl0PzgfYHOnq7d3vM8Q">量子位中文解读</a>]**
**[<a href="https://mp.weixin.qq.com/s/FSxUdvPI713J2LiHnNaFCw">时序人中文解读</a>]**
**[<a href="https://mp.weixin.qq.com/s/nUiQGnHOkWznoBPqM0KHXg">AI算法厨房中文解读</a>]**
**[<a href="https://zhuanlan.zhihu.com/p/676256783">知乎中文解读</a>]**


</div>

<p align="center">

<img src="./figures/logo.png" width="70">

</p>

---
>
> 🙋 Please let us know if you find out a mistake or have any suggestions!
> 
> 🌟 If you find this resource helpful, please consider to star this repository and cite our research:

```


## Updates/News:

🚩 **News** (Aug. 2024): Time-LLM has been adopted by XiMou Optimization Technology Co., Ltd. (XMO) for Solar, Wind, and Weather Forecasting.

🚩 **News** (May 2024): Time-LLM has been included in [NeuralForecast](https://github.com/Nixtla/neuralforecast). Special thanks to the contributor @[JQGoh](https://github.com/JQGoh) and @[marcopeix](https://github.com/marcopeix)!

🚩 **News** (March 2024): Time-LLM has been upgraded to serve as a general framework for repurposing a wide range of language models to time series forecasting. It now defaults to supporting Llama-7B and includes compatibility with two additional smaller PLMs (GPT-2 and BERT). Simply adjust `--llm_model` and `--llm_dim` to switch backbones.

## Introduction
Time-LLM is a reprogramming framework to repurpose LLMs for general time series forecasting with the backbone language models kept intact.
Notably, we show that time series analysis (e.g., forecasting) can be cast as yet another "language task" that can be effectively tackled by an off-the-shelf LLM.

<p align="center">
<img src="./figures/framework.png" height = "360" alt="" align=center />
</p>

- Time-LLM comprises two key components: (1) reprogramming the input time series into text prototype representations that are more natural for the LLM, and (2) augmenting the input context with declarative prompts (e.g., domain expert knowledge and task instructions) to guide LLM reasoning.

<p align="center">
<img src="./figures/method-detailed-illustration.png" height = "190" alt="" align=center />
</p>

## Requirements
Use python 3.11 from MiniConda

- torch==2.2.2
- accelerate==0.28.0
- einops==0.7.0
- matplotlib==3.7.0
- numpy==1.23.5
- pandas==1.5.3
- scikit_learn==1.2.2
- scipy==1.12.0
- tqdm==4.65.0
- peft==0.4.0
- transformers==4.31.0
- deepspeed==0.14.0
- sentencepiece==0.2.0

To install all dependencies:
```
pip install -r requirements.txt
```

## Datasets
You can access the well pre-processed datasets from [[Google Drive]](https://drive.google.com/file/d/1NF7VEefXCmXuWNbnNe858WvQAkJ_7wuP/view?usp=sharing), then place the downloaded contents under `./dataset`

## Quick Demos
1. Download datasets and place them under `./dataset`
2. Tune the model. We provide five experiment scripts for demonstration purpose under the folder `./scripts`. For example, you can evaluate on ETT datasets by:

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