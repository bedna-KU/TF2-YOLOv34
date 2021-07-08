# TensorFlow-2.x-YOLOv3 and YOLOv4 

YOLOv3 and YOLOv4 implementation in TensorFlow 2.x, with support for training, transfer training, object tracking mAP and so on...

## Installation
First, clone or download this GitHub repository.
Install requirements and download pretrained weights:
```
pip install -r ./requirements.txt

# yolov3
wget -P model_data https://pjreddie.com/media/files/yolov3.weights

# yolov3-tiny
wget -P model_data https://pjreddie.com/media/files/yolov3-tiny.weights

# yolov4
wget -P model_data https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights

# yolov4-tiny
wget -P model_data https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights
```
### Save images and XMLs from Labelimg (or other)
Files save to directory DATA

### Divide to train and test
python3 tools_new/divide.py -i DATA/dataset/ -o dataset

## Thanks

https://github.com/pythonlessons/TensorFlow-2.x-YOLOv3

