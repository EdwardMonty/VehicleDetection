# 车辆检测与识别（Simulink）

使用 Simulink 对视频流进行帧间差分，分离运动车辆与背景，完成车辆检测、识别与计数。

## 文件说明

| 文件 | 功能 |
|------|------|
| `frame_differencing_vehicle_detection.slx` | 帧间差分法检测运动车辆（对比前后帧，分离背景与运动物体） |
| `vehicle_identification.slx` | 车辆识别与计数 |
| `vehicle_counting_serial.slx` | 车辆计数，并通过串口将计数结果输出到 Arduino |

## 运行环境

- MATLAB R2015b 或更高
- Simulink
- Computer Vision System Toolbox
- Image Processing Toolbox
- `vehicle_counting_serial.slx` 额外需要 Simulink Support Package for Arduino Hardware 及 Arduino 开发板

## 运行说明

1. 打开任一 `.slx` 模型。
2. 视频来源为 Computer Vision Toolbox 自带的 `viptraffic.avi`。模型内 `From Multimedia File` 模块引用的是绝对路径，首次运行需重新指向本机该视频文件。
3. 点击运行，在 `Video Viewer` 中查看检测/识别结果。
