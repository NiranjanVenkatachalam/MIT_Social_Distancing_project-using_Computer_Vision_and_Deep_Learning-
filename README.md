This repository aims to compare the performance of object detection models when using OpenVINO versus running them natively without optimization. The focus is on measuring the frames per second (FPS) and latency of each approach to assess the impact of OpenVINO's inference acceleration.

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

  OpenVINO is Intel's toolkit for optimizing and deploying deep learning models on Intel hardware, offering hardware acceleration for high-performance inference. It converts models to an optimized format, reducing 
  memory usage and improving speed. With unified APIs and performance analysis tools, OpenVINO enables seamless integration and efficient deployment for object detection and computer vision tasks

     

To execute the social distance model using openvino (if you have intel processor):


1)install openvino from 
    https://docs.openvino.ai/2023.0/openvino_docs_install_guides_overview.html?ENVIRONMENT=DEV_TOOLS&OP_SYSTEM=WINDOWS&VERSION=v_2023_0_1&DISTRIBUTION=PIP


2)Install openvino development tools
    https://docs.openvino.ai/2023.0/openvino_docs_install_guides_install_dev_tools.html


3)Other requirements:
    jupyter notebook, install opencv, load the xml and bin files path of the model, input video.


We consider that you have your models xml and bin file from the model converter.


If you dont have intel processor you can use intel edge devcloud jupyter notebook.However it is advised to use localcomputer with intel processor.





















