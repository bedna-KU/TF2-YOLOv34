# TensorFlow 2.x YOLOv3 and YOLOv4

YOLOv3 and YOLOv4 implementation in TensorFlow 2.x, with support for training, transfer training

## Installation
First, clone or download this GitHub repository.
Install requirements and download pretrained weights:
```
pip install -r ./requirements.txt
```
### Load learmed weights

```
# yolov3
wget -P model_data https://pjreddie.com/media/files/yolov3.weights

# yolov3-tiny
wget -P model_data https://pjreddie.com/media/files/yolov3-tiny.weights

# yolov4
wget -P model_data https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v3_optimal/yolov4.weights

# yolov4-tiny
wget -P model_data https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights
```
## Train/Detect with your own DATASET

### Divide images and XMLs to train and test
```python
python3 tools/divide.py -i ../dataset/name
```
Data is now in directory DATASET

### Make YOLOv3 list from images and XMLs
```python
python3 tools/XML_to_YOLOv3.py
```
You will find the data in the DATASET directory.
Here you will find the files:
* list.names
* list_test.txt
* list_train.txt

### Run training
```python
python3 tools/XML_to_YOLOv3.py
```
### Detect objects in image
```python
python3 detection_image.py
```
### Detect objects in video
```python
python3 detection_video.py
```

## Thanks

https://github.com/pythonlessons/TensorFlow-2.x-YOLOv3

