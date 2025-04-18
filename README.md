<h1 align = "center">
<img src="images/logo.png" alt="icon" style="width:50px; vertical-align:middle;" />
EyecareGPT: Boosting Comprehensive Ophthalmology
Understanding with Tailored Dataset, Benchmark and Model
</h1>

<div align="center">
Sijing Li<sup>1</sup>, Tianwei Lin<sup>1</sup>, Lingshuai Lin<sup>2</sup>, Wenqiao Zhang<sup>1</sup>, Jiang Liu<sup>1</sup>, Xiaoda Yang<sup>1</sup>, Juncheng Li<sup>1</sup>, Yucheng He<sup>3</sup>, Song xiaohui<sup>1</sup>, Jun Xiao<sup>1</sup>, Yueting Zhuang<sup>1</sup>, Beng Chin Ooi<sup>4</sup>
<br><br>

<sup>1</sup>Zhejiang University,
<sup>2</sup>Harbin Institute of Technology,
<sup>3</sup>Chenzhou No. 1 People's Hospital,
<sup>4</sup>National University of Singapore

<a href='https://huggingface.co/lintw/HealthGPT-M3'><img src='https://img.shields.io/badge/Model-Huggingface-yellow'></a>
<a><img src='https://img.shields.io/badge/Dataset-Coming Soon-E59FB6'></a>
<a href='https://llsuzy.github.io/HealthGPT.github.io/'><img src='https://img.shields.io/badge/Home-Page-green'></a>

</div>

## 🌟 Overview

Welcome to **EyecareGPT!** 🚀
This repository showcases the **Eyecare Kit**, a comprehensive solution designed to advance the adaptability and performance of Large Vision-Language Models (LVLMs) in the specialized domain of ophthalmology. Our work aims to  facilitate research on intelligent ophthalmic diagnosis field by introducing innovations across three key aspects: **Dataset**, **Benchmark**, and **Model**.

##### :clap: Key Highlights:

- **Eyecare-100K: The First Comprehensive Ophthalmic Visual Instruction Dataset.** We present a large-scale, diverse dataset comprising approximately **102,000** visual question answering (VQA) pairs, covering **8** imaging modalities, **3** tasks， over **15** anatomical structures, and more than **100** types of eye diseases.
- **Eyecare-Bench: A Systematic Benchmark for Intelligent Ophthalmic Diagnosis.** We introduce a novel benchmark for in-depth evaluation of Med-LVLMs on closed QA, open QA, and report generation tasks, featuring around 15,000 carefully selected examples.
- **EyecareGPT: An Adapted LVLM Architecture for Ophthalmology.** We present a model incorporating high-resolution visual feature extraction, an adaptive resolution mechanism, and dense feature integration, with scalable variants for real-world deployment.

## 🔥 News

- **[2025.02.17]** We have released the pre-trained weight on HuggingFace and dataset demo of Eyecare-100K.

### TODO

- [x] Release  pre-trained weight of the model.
- [x] Release the demo of  Eyecare-100K.
- [ ] Release the inference UI/UX.
- [ ] Release inference code (e.g. training scripts).

## 📚 Task Classification and Support

**Eyecare-100K** aggregates **real-world** ophthalmic data across **8** modalities, **15+** anatomical structures and **100+** eye diseases, supporting multi-modal report generation and fine-grained visual QA tasks.

<img src="images/eyecare.png" style="vertical-align:middle;" />

## :mailbox: Data collection and statistics

We develop an automated **multi-agent data engine** to create Eyecare-100K, converting categorized labels and raw reports into 3 kinds of structured VQA pairs: closed-QA, open-QA, report generation.

<img src="images/agent.png" style="width:50%;vertical-align:middle;" /><img src="images/dataset.png" style="width:50%;vertical-align:middle;" />

## :ferris_wheel: Architecture

**EyecareGPT**: We introduce an LVLM architecture adapted to complex, heterogeneous ophthalmic clinical imaging, achieving SoTA performance. **(i) High-Resolution Feature Extraction:** Employ SigLIP to enhance local lesion perception.  **(ii) Adaptive Resolution Mechanism:** Accommodate variable resolutions in clinical ophthalmic imaging. **(iii) Layer-wise Dense Connector (LDC):** Densely integrate multi-scale visual features and preserve fine-grained structural information.

<img src="images/model.png" style="width:60%;vertical-align:middle;" />

## 🛠️ Getting Started

**EyecareGPT**  is our ophthalmology-specialized LVLM, built on **Eyecare-100K**. We have released our model in two configurations, **EyecareGPT-3.8B** and **EyecareGPT-7B**, to suit different requirements and resource availability:

- EyecareGPT-3.8B: A smaller version optimized for speed and reduced memory usage.
- EyecareGPT-7B: A larger version designed for higher Performance.

**Model Access：**

|      Model      |                         Download                         |
| :-------------: | :------------------------------------------------------: |
| EyecareGPT-3.8B | [HF Link](https://huggingface.co/LLSuzy/EyecareGPT-3.8B) |
|  EyecareGPT-7B  |  [HF Link](https://huggingface.co/LLSuzy/EyecareGPT-7B)  |

EyecareGPT utilizes `siglip-so400m-patch14-384` as the visual encoder and employs `Phi-3.5-mini-instruct` and `Qwen2.5-VL-7B-Instruct` as the pre-trained LLM base models for EyecareGPT-3.8B and EyecareGPT-7B, respectively. Please download the corresponding weights:

|          Model Type          |         Model Name          |                           Download                           |
| :--------------------------: | :-------------------------: | :----------------------------------------------------------: |
|             ViT              | `siglip-so400m-patch14-384` | [Download](https://huggingface.co/google/siglip-so400m-patch14-384) |
| Base Model (EyecareGPT-3.8B) |   `Phi-3.5-mini-instruct`   | [Download](https://huggingface.co/microsoft/Phi-3.5-mini-instruct) |
|  Base Model (EyecareGPT-7B)  |  `Qwen2.5-VL-7B-Instruct`   | [Download](https://huggingface.co/Qwen/Qwen2.5-VL-7B-Instruct) |

 Training and testing scripts code is coming soon...

