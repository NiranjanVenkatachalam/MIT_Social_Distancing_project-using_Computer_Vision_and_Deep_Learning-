This repository aims to compare the performance of object detection models when using OpenVINO versus running them natively without optimization. The focus is on measuring the frames per second (FPS) and latency of each approach to assess the impact of OpenVINO's inference acceleration.

## Prerequisites

To run the code and reproduce the performance comparison, the following prerequisites are required:

- Python (version 3.8.2 and above)
- OpenVINO toolkit (version 2022.3.1)
- Model weights and configurations (provide details on where to obtain or download the model)

# COVID19-Social-Distancing-Violation-Detector-Using-YOLOv5

Python implementation of YOLO v5 to detect if people are maintaining social distancing in public places.

## ABOUT YOLO v5
YOLOv5 is the most recent version of the well-known YOLO (You Only Look Once) series of real-time object identification algorithms. It is perfect for a variety of computer vision tasks since it provides cutting-edge performance in terms of speed and accuracy. The PyTorch deep learning framework is used to construct YOLOv5, which offers a user-friendly API for developing and deploying object detection models. The computer vision community has paid YOLOv5 a lot of attention due to its effective design and user-friendly interface, making it the go-to choice for object detection applications.

The YOLOv5 implementation has been done in Pytorch in contrast with the previous developments that used the DarkNet framework. This makes it easier to understand, train with it and deploy this model.

## YOLOv5 variants
YOLOv5 is available in four models, namely s, m, l, and x, each one of them offering different detection accuracy and performance as shown below.We are using yolov5 in this model.

## INSTRUCTIONS
1. git clone git@github.com:NiranjanVenkatachalam/social_distancing_detector.git
2. python detector.py --source inputs/mall_area.mp4 --yolo_model yolov5s
3.. python detector.py --source inputs/street_area.mp4 --yolo_model yolov5s


# COVID19-Social-Distancing-Violation-Detector-Using-Openvino

 OpenVINO is Intel's toolkit for optimizing and deploying deep learning models on Intel hardware, offering hardware 
 acceleration for high-performance inference. It converts models to an optimized format, reducing 
 memory usage and improving speed. With unified APIs and performance analysis tools, OpenVINO enables seamless 
 integration and efficient deployment for object detection and computer vision tasks
 

Integrate OpenVINO optimisations with the model, then compare performance metrics to a prior run.

Basic conversion and opimization steps are:
1. Model Selection: Choose the model you want to optimize and ensure it is compatible with Intel OpenVINO.
2. Model Optimization: Optimize the model using techniques like quantization and precision adjustment to improve performance and resource utilization.
3. Model Conversion: Use the OpenVINO Model Optimizer tool to convert the optimized model to the Intermediate Representation (IR) format.
4. Choose Target Device: Determine the target hardware device for inference, such as Intel CPUs, GPUs, or FPGAs.
Inference Code Integration: Integrate the converted model into your application using the OpenVINO Inference Engine APIs.

The model used for the performance comparison is YOLOv5s, a popular object detection model. YOLOv5 is a state-of-the-art real-time object detection model that achieves high accuracy while maintaining fast inference speeds.We have also used a pre-trained model of intel.
     

To execute the social distance model using openvino (if you have intel processor):


1)install openvino from 
    https://docs.openvino.ai/2023.0/openvino_docs_install_guides_overview.html?ENVIRONMENT=DEV_TOOLS&OP_SYSTEM=WINDOWS&VERSION=v_2023_0_1&DISTRIBUTION=PIP


2)Install openvino development tools
    https://docs.openvino.ai/2023.0/openvino_docs_install_guides_install_dev_tools.html


3)Other requirements:
    jupyter notebook, install opencv, load the xml and bin files path of the model, input video.


We consider that you have your models xml and bin file from the model converter.


If you dont have intel processor you can use intel edge devcloud jupyter notebook.However it is advised to use localcomputer with intel processor.



## Analyze the performance
Compare the performance metrics displayed after running the model with and without OpenVINO. Evaluate factors such as inference time, CPU/GPU utilization, and memory usage.

These performance metrics provide a comprehensive view of the model's performance when using OpenVINO compared to without OpenVINO. Monitoring and comparing these metrics help assess the impact of OpenVINO optimizations on speed, resource utilization, memory efficiency, scalability, and energy consumption.

1. Inference Time: OpenVINO optimizations can potentially improve the model's inference speed by 1.5x to 4x compared to running the model without OpenVINO.
2. CPU/GPU Utilization: OpenVINO optimizations can lead to higher CPU/GPU utilization, often ranging from 60% to 90%, indicating improved resource utilization.
3. Memory Usage: OpenVINO optimizations can sometimes reduce memory usage by up to 50% compared to running the model without OpenVINO. However, memory usage can vary depending on the model's architecture and the specific optimizations applied.
4. Throughput: With OpenVINO optimizations, the model's throughput can increase by approximately 2x to 5x compared to running the model without OpenVINO. This allows for processing a higher volume of data in a given timeframe.


We have considered FPS and latency as the main factors of optimization which are displayed on output video.


## Contact
For more information, please contact Manan Bhatt at niranjanvenkatachalam@gmail.com.















