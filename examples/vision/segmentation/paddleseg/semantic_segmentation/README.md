# PaddleSeg语义分割模型高性能全场景部署方案-FastDeploy

## 1. FastDeploy介绍
**[⚡️FastDeploy](https://github.com/PaddlePaddle/FastDeploy)**是一款**全场景**、**易用灵活**、**极致高效**的AI推理部署工具，支持**云边端**部署。使用FastDeploy可以简单高效的在X86 CPU、NVIDIA GPU、飞腾CPU、ARM CPU、Intel GPU、昆仑、昇腾、瑞芯微、晶晨、算能等10+款硬件上对PaddleSeg语义分割模型进行快速部署，并且支持Paddle Inference、Paddle Lite、TensorRT、OpenVINO、ONNXRuntime、RKNPU2、SOPHGO等多种推理后端。

## 2. 硬件支持列表

|硬件类型|该硬件是否支持|使用指南|Python|C++|
|:---:|:---:|:---:|:---:|:---:|
|X86 CPU|✅|[链接](cpu-gpu)|✅|✅|
|NVIDIA GPU|✅|[链接](cpu-gpu)|✅|✅|
|飞腾CPU|✅|[链接](cpu-gpu)|✅|✅|
|ARM CPU|✅|[链接](cpu-gpu)|✅|✅|
|Intel GPU(集成显卡)|✅|[链接](cpu-gpu)|✅|✅|  
|Intel GPU(独立显卡)|✅|[链接](cpu-gpu)|✅|✅|  
|昆仑|✅|[链接](kunlun)|✅|✅|
|昇腾|✅|[链接](ascend)|✅|✅|
|瑞芯微|✅|[链接](rockchip)|✅|✅|  
|晶晨|✅|[链接](amlogic)|--|✅|  
|算能|✅|[链接](sophgo)|✅|✅|  

## 3. 详细使用文档
- X86 CPU
  - [部署模型准备](cpu-gpu)  
  - [Python部署示例](cpu-gpu/python/)
  - [C++部署示例](cpu-gpu/cpp/)
- NVIDIA GPU
  - [部署模型准备](cpu-gpu)  
  - [Python部署示例](cpu-gpu/python/)
  - [C++部署示例](cpu-gpu/cpp/)
- 飞腾CPU
  - [部署模型准备](cpu-gpu)  
  - [Python部署示例](cpu-gpu/python/)
  - [C++部署示例](cpu-gpu/cpp/)
- ARM CPU
  - [部署模型准备](cpu-gpu)  
  - [Python部署示例](cpu-gpu/python/)
  - [C++部署示例](cpu-gpu/cpp/)  
- Intel GPU
  - [部署模型准备](cpu-gpu)  
  - [Python部署示例](cpu-gpu/python/)
  - [C++部署示例](cpu-gpu/cpp/)
- 昆仑 XPU
  - [部署模型准备](kunlun)  
  - [Python部署示例](kunlun/python/)
  - [C++部署示例](kunlun/cpp/)
- 昇腾 Ascend
  - [部署模型准备](ascend)  
  - [Python部署示例](ascend/python/)
  - [C++部署示例](ascend/cpp/)
- 瑞芯微 Rockchip
  - [部署模型准备](rockchip/)  
  - [Python部署示例](rockchip/rknpu2/)
  - [C++部署示例](rockchip/rknpu2/)
- 晶晨 Amlogic
  - [部署模型准备](amlogic/a311d/)  
  - [C++部署示例](amlogic/a311d/cpp/)  
- 算能 Sophgo
  - [部署模型准备](sophgo/)  
  - [Python部署示例](sophgo/python/)
  - [C++部署示例](sophgo/cpp/)  

## 4. 更多部署方式

- [Android ARM CPU部署](android)  
- [服务化Serving部署](serving)  
- [web部署](web)  
- [模型自动化压缩工具](quantize)

## 5. 常见问题

遇到问题可查看常见问题集合，搜索FastDeploy issue，*或给FastDeploy提交[issue](https://github.com/PaddlePaddle/FastDeploy/issues)*:

[常见问题集合](https://github.com/PaddlePaddle/FastDeploy/tree/develop/docs/cn/faq)  
[FastDeploy issues](https://github.com/PaddlePaddle/FastDeploy/issues)  
