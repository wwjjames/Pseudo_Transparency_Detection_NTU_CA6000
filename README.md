# 🕵️‍♀️ Pseudo-Transparency Image Detector | 伪透明背景检测器

> **NTU MCAAI CA6000 Final Assignment**
>
> A Deep Learning project to detect "pseudo-transparent" checkerboard backgrounds in images.
> 一个基于深度学习的项目，旨在识别图像中是否包含“伪透明”的灰白棋盘格背景。

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)

![screenshot](https://youke3.picui.cn/s1/2026/01/09/696105faef555.png)

## 📖 Introduction (项目介绍)

AI image models often misinterpret transparent backgrounds as gray-white or black-gray checkerboard patterns, resulting in images that lack a genuine alpha channel (transparency). This project aims to use **Convolutional Neural Networks (CNNs)** to identify the features of these "pseudo-transparent" images. The project has two primary objectives: first, to serve as an initial image filtering step for subsequent automatic background removal applications; and second, to explore the impact of different network depths, dataset sizes, and data processing strategies on model training.

AI图像模型常常将透明背景理解成为灰白/黑灰棋盘格的背景，使得用户得到的图片并不具有真正的透明通道。本项目旨在使用**卷积神经网络 (CNN)** 完成“伪透明”图片特征的识别，一是为后续自动抠图的应用实现第一步的图片过滤，二是探索不同深度、不同数据集规模及不同数据梳理方式对模型训练的影响。

## 🚀 Features (功能特点)

*   **Multi-Architecture Comparison**: Performance comparison between 2-layer, 3-layer (Baseline), and 4-layer CNNs.
    *   **多模型架构对比**：包含 2层、3层 (基准)、4层 CNN 的性能分析。
*   **Small Data Research**: Investigation of overfitting in few-shot scenarios (200 samples).
    *   **小样本学习研究**：探究了在仅有 200 张样本下的过拟合现象。
*   **Strong Augmentation Study**: The application of strong augmentation led to unexpected challenges, resulting in high variance and training difficulties despite mitigating overfitting.
    *   **强数据增强探究**：强力增强的应用导致了意料之外的挑战，虽然缓解了过拟合，但也造成了显著的高方差与训练困难。
*   **Interactive Demo**: A Web GUI built with Streamlit for real-time inference.
    *   **交互式 Demo**：基于 Streamlit 的 Web 界面，支持实时切换模型与检测。

## 📥 Download Resources (资源下载)

Due to GitHub file size limits, the **Model Weights** and **Dataset** are hosted on Hugging Face. Please download them before running the code.

由于 GitHub 文件大小限制，**模型权重**和**数据集**托管在 Hugging Face。请在使用前下载：

| Resource (资源) | Description (说明) | Link (下载链接) |
| :--- | :--- | :--- |
| **🤖 Models** | Trained `.pth` files (Baseline, Depth4, SmallData, etc.) <br> 包含所有训练好的模型权重 | [👉 Download Models on Hugging Face](https://huggingface.co/wwjjames/Pseudo_Transparency_Detection) |
| **📂 Dataset** | Training & Testing images (`dataset.zip`) <br> 包含训练和测试用的正负样本图片 | [👉 Download Dataset on Hugging Face](https://huggingface.co/datasets/wwjjames/Pseudo_Transparency_Detection) |

> **Note**: After downloading, place `.pth` files into the `models/` directory.
> 
> **注意**：下载后，请将 `.pth` 文件放入项目的 `models/` 文件夹中。

## 🛠️ Installation (安装与配置)

1. **Clone the repository (克隆项目)**
   ```bash
   git clone https://github.com/wwjjames/Pseudo_Transparency_Detection_NTU_CA6000.git
   cd Pseudo_Transparency_Detection_NTU_CA6000
   

2. **Install dependencies (安装依赖)**
   ```bash
   pip install -r requirements.txt
   
## 💻 Usage (如何运行)

Ensure you have placed the model files in the models/ folder.

确保你已经下载了模型文件并放在了 models/ 目录下。

1. **Run the Streamlit demo:**
   
   **运行 Streamlit 演示程序：**
   
   ```bash
   streamlit run demo.py
   
**What will happen:**

1)A browser window will open automatically. 2)Select a model from the sidebar (e.g., "Baseline" or "Small Data + Aug"). 3)Upload an image to check if it's "Pseudo-Transparent".

**运行效果：**

1)浏览器会自动打开页面。2)在侧边栏选择模型（如 Baseline 或 Small Data + Aug）。3)上传图片即可进行检测。

## 📂 Project Structure (项目结构)

1. Project Structure (项目结构)
   ```text
   .
   ├── demo.py              # Streamlit 交互式演示入口
   ├── notebook/            # Jupyter Notebook 训练代码与实验记录
   ├── models/              # [需下载] 存放 .pth 模型权重文件
   ├── dataset/             # [需下载] 存放原始图片数据
   ├── requirements.txt     # 项目依赖列表
   └── README.md            # 项目说明文档

## 📝 License

This project is open source.


