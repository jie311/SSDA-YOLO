# SDA-YOLO
Codes for my paper "SDA-YOLO: Semi-supervised Domain Adaptive YOLO for Cross-Domain Object Detection" for ICME2022

## Abstarct

*The cross-domain discrepancy has always been what domain adaptive object detection aims to alleviate. This problem is more prominent when a significant distribution difference appearing between the source data used for training and the target data from the real application scenario. In this paper, we propose a novel semi-supervised domain adaptive YOLO (SDA-YOLO) method to improve cross-domain detection performance by integrating the efficient YOLOv5. Specifically, we adapt knowledge distillation to assist the student model obtain the instance-level features in the unlabeled target domain. We also draw support from style transfer to cross-generate pseudo images in different domains for remedying the image-level differences. We evaluate our proposed SDA-YOLO on public benchmarks including PascalVOC, Clipart1k, Cityscapes, and Foggy Cityscapes. Moreover, the experimental details on the yawning detection dataset collected in various schools and classrooms are also reported. The final results show the impressive improvement of our method in cross-domain obejct detection task.*

## Brief Description

SDA-YOLO is designed for domain adaptative cross-domain object detection based on the knowledge distillation framework and robust `YOLOv5`. The network architecture is as below. 

![example1](./images/figure1.png)

So far, we have trained and evaluated it on two adaptation tasks: **PascalVOC → Clipart1K**, **CityScapes → CityScapes Foggy**.

## Installition

**Environment:** Anaconda, Python3.8, PyTorch1.10.0(CUDA11.2), wandb

```bash
$ git clone https://github.com/hnuzhy/SDA-YOLO.git
$ pip install -r requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

# I have only test my codes on GTX3090 with CUDA11.2 and PyTorch1.10.0. You can install the same verison if needed
$ pip3 install torch==1.10.0+cu111 torchvision==0.11.1+cu111 torchaudio==0.10.0+cu111 -f https://download.pytorch.org/whl/cu111/torch_stable.html
or
$ wget https://download.pytorch.org/whl/cu111/torch-1.10.0%2Bcu111-cp38-cp38-linux_x86_64.whl
$ wget https://download.pytorch.org/whl/cu111/torchvision-0.11.1%2Bcu111-cp38-cp38-linux_x86_64.whl
$ wget https://download.pytorch.org/whl/cu111/torchaudio-0.10.0%2Bcu111-cp38-cp38-linux_x86_64.whl
$ pip3 install torch*.whl
```

## Dataset Preparing

## Test and Train


## References

* [YOLOv5 🚀 in PyTorch > ONNX > CoreML > TFLite](https://github.com/ultralytics/yolov5)
* [UMT(A Pytorch Implementation of Unbiased Mean Teacher for Cross-domain Object Detection (CVPR 2021))](https://github.com/kinredon/umt)


