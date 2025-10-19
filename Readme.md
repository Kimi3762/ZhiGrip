# Zhi Grip 智握

[English Version][./Readme-en.md]

语音驱动的三自由度视觉抓取机械臂

## 演示视频

[![Watch the video](//i1.hdslb.com/bfs/archive/d7e887a7b80215b01434efc77a01e3cdd8fa26f0.jpg)](https://www.bilibili.com/video/BV1MnWhzCEoF)

## 目录结构

- `3DParts`：3D 模型
- `Controller`： Python 上位机，负责视觉和控制
- `Control`：ESP32 Arduino 嵌入式代码，实现硬件驱动和末端位置维护
- `xiaozhi-server`：基于 [xiaozhi-esp32-server](https://github.com/xinnan-tech/xiaozhi-esp32-server) 的语音交互服务端
- `Joystick`：手柄控制脚本

## 项目架构

![机械结构](img/1.png)

![小智框架](img/2.png)

![系统框图](img/3.png)

## 注意

本项目使用了 **Git 子模块** 来管理各个子模块仓库。子模块允许将其他 Git 仓库嵌入到本仓库的特定目录中，保持模块独立，同时方便统一管理。

### 克隆项目

要正确克隆包含子模块的仓库，请使用：

```
git clone --recurse-submodules https://github.com/LanternCX/ZhiGrip.git
```

如果你已经克隆了仓库，但没有初始化子模块，可以运行：

```
git submodule update --init --recursive
```

------

### 更新子模块

当子模块远程仓库有更新时，可以执行：

```
git submodule update --remote
```

如果你在子模块目录中进行开发并提交，也可以在总仓库中记录子模块的最新提交：

```
git add <submodule_directory>
git commit -m "Update submodule"
```