# Automatic number-plate recognition with [YOLOv8](https://docs.ultralytics.com) & [EasyOCR](https://pypi.org/project/easyocr/)

![img](https://www.shaip.com/wp-content/uploads/2022/08/Blog_Automatic-Number-Plate-Recognition-ANPR.jpg)
[Automatic number-plate recognition](https://en.wikipedia.org/wiki/Automatic_number-plate_recognition) is a technology that uses optical character recognition on images to read vehicle registration plates to create vehicle location data. It can use existing closed-circuit television, road-rule enforcement cameras, or cameras specifically designed for the task. ANPR is used by police forces around the world for law enforcement purposes, including to check if a vehicle is registered or licensed.
 
## Approach
 - first of all detect cars using [YOLOv8 model](models/yolov8s.pt)
 - detect number-plate using [trained model](models/num-pal.pt)
 - extract text from number-plate image using EasyOCR

<hr>

### Datasets
Number-plate detection > [License Plate Recognition](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e)

### Train
 - model trained only for number-plate detection
 - Epochs = 10 | Precision = 0.975 | Recall = 0.95
 - [notebook](Train.ipynb)

### Test
 - [Main file](Main.ipynb) shows the usage of the model
 - you can check your test file yourself
 - code is also written for the file in video format

<hr>

### Disadvantages 
 1. Our model can detect number-plate from full image but used YOLOv8 model for more precision. This will cause the program to run slowly.
 2. EasyOCR does not perform well with low-quality images.

### Suggestions
 1. Build a comprehensive number-plate detection model using a large and high-quality dataset
 2. Use image to text extraction libraries other than EaseOCR
 
## Results
 <img src="https://github.com/Saidislombek-dev/automatic_number-plate_recognition/blob/main/images/result0.jpg" width="350"/> <img src="https://github.com/Saidislombek-dev/automatic_number-plate_recognition/blob/main/images/result1.jpg" width="370"/>
