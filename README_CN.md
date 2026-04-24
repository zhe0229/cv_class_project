# 计算机视觉课程项目：基于 Real-ESRGAN 的图像超分辨率

本仓库是我们的计算机视觉课程项目，基于 Real-ESRGAN 框架开展图像超分辨率与图像修复实验。仓库中同时保留了课程过程中使用的实验文件、输入输出样例以及分析结果，便于展示、复现和撰写报告。

## 项目简介

本项目的目标是探索深度学习方法如何提升低质量图像的清晰度与分辨率，恢复更多细节信息。我们以 Real-ESRGAN 作为主要基线模型，并围绕课程需求组织了相关实验与结果整理。

本仓库中的主要工作包括：

- 运行图像超分辨率推理
- 测试不同图像类型和退化强度下的恢复效果
- 对不同样例的修复结果进行比较
- 整理课程展示或报告所需的实验输出

## 仓库结构

主要目录和文件如下：

- `realesrgan/`：核心模型代码
- `inference_realesrgan.py`：图像推理主脚本
- `inference_realesrgan_video.py`：视频推理脚本
- `weights/`：预训练模型权重
- `inputs/`：示例输入数据
- `results/`：生成的输出结果
- `paper_inputs/`：项目分析使用的输入数据
- `paper_results/`：实验图像与分析结果
- `baseline_experiment.ipynb`：项目实验 notebook
- `tests/`：测试文件与测试样例数据

## 环境配置

建议环境：

- Python 3.8 及以上
- PyTorch
- pip 或 conda

安装依赖：

```bash
pip install -r requirements.txt
python setup.py develop
```

## 运行方式

在默认输入文件夹上运行图像超分辨率：

```bash
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs -o results
```

如果需要启用人脸增强：

```bash
python inference_realesrgan.py -n RealESRGAN_x4plus -i inputs -o results --face_enhance
```

生成结果将保存在 `results/` 目录下。

## 项目产出

本仓库还包含以下课程项目材料：

- 实验 notebook
- 整理好的样例数据和输入图像
- 用于分析和展示的图表
- 中间结果与最终修复结果

这些内容被保留在仓库中，主要用于支持课程报告、结果展示与项目复现。

## 说明

- 仓库中包含预训练权重和实验输出，因此整体体积较大。
- 部分目录中保留了开发和分析过程中产生的实验文件。
- 本项目主要用于课程学习、实验与展示。

## 致谢

本项目基于原始 Real-ESRGAN 工作构建：

- Real-ESRGAN: https://github.com/xinntao/Real-ESRGAN

我们在原始框架基础上进行了课程项目相关的实验组织、结果整理和说明文档调整。
