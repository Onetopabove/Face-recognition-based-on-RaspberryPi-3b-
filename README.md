# 基于树莓派3b+的人脸的动态检测定位
## Outline
- **Introduction**
  - The general description of the ideas
  - The highlights of this program
- **Platform** 
  - Hardware 
  - Software
- **Implementation**
  - The whole system
  - Hardware (Describe the main steps for hardware)
  - Software (Demonstrate the steps of face recognition)
- **Test**
  - Initial test
  - Adjustment
- **Reference**
  - Hardware
  - Software

## Introduction
- The general description of the ideas
1. 实现图片的人脸检测、定位、识别
2. 动态实现
3. 性能优化
- The highlights of this program
1. 简单----适用于初学图像处理相关知识
2. 从下到上----结构足够清晰
3. 成本低----用现有硬件
## Platform
### Hardware
1. [树莓派3B+](https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/)
2. 500万像素的树莓派摄像头(OV5647)
### Software
1. [Raspberry Pi OS with desktop](https://www.raspberrypi.org/software/operating-systems/#raspberry-pi-os-32-bit)
	- Release date: December 2nd 2020
	- Kernel version: 5.4
	- Size: 1,177MB
2. OpenCV
## Implementation
### The whole system

![Overview](.\picture\Overview.jpg)

* 考虑到USB摄像头会在速度上有一定的降低，摄像头通过CSI接口与树莓派3B+相连。
* TF卡是系统的硬盘。
* OpenCV通过CSI接口控制摄像头，获取数据后可存储至TF卡或进行处理、处理后通过VNC(服务端)发送至局域网内的VNC(客户端)。
* 运行在树莓派上的Raspberry Pi OS承载了上述软件的需求。







## Reference
### Hardware
- [树莓派实验室](https://shumeipai.nxez.com)
- [Raspberry Pi 3 Model B+](https://www.raspberrypi.org/products/raspberry-pi-3-model-b-plus/)

### Software
