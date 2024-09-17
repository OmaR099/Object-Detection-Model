# Object-Detection-Model
## Table of Contents  
- [Project Overview](#project-overview)  
- [Installation](#installation)
- [Usage](#usage)  
- [Dataset](#dataset)  
- [Evaluation](#evaluation)  
- [Results](#results)  
## Project Overview  
This project implements an object detection model using YOLOv8 to classify and detect objects for two tasks:  
1. **Rock-Paper-Scissors**: Detects hand signs for the classic game rock-paper-scissors.  
2. **Manufacturing Items**: Identifies various items used in manufacturing processes.  

This model aims to provide robust detection capabilities enhancing automation in gaming and industrial applications.  

## Installation  
To set up the project, clone this repository and install the required packages. 
```bash  
git clone https://github.com/yourusername/repo-name.git  
cd repo-name  
pip install -r requirements.txt.
```
 
**Requirements**
- Roboflow
- Ultralytics

## Usage
You can use the provided scripts to run inference or train the model on your datasets.

**Run Inference**

To run inference on an image or video, use the following command:
```bash  
python inference.py --source path/to/your/image_or_video
```

**Train the Model**

To train the model on your custom dataset, use the following command:
```bash  
!yolo task=detect mode=train model=yolov8n.pt data=data.yaml epochs=10 imgsz=640 plots=True
```

## Dataset
Provide information about the datasets used:

- **Rock-Paper-Scissors dataset**: The dataset used in this task, the rock-paper-scissors Computer Vision Project from Roboflow, includes 3129 images, and 3 classes, you can obtain it using this link https://universe.roboflow.com/roboflow-58fyf/rock-paper-scissors-sxsw.
- **Manufacturing items dataset**: The dataset used in this task, the cv-project-fins0 from Roboflow, includes 632 images, and 12 classes.

## Evaluation
Model's performance and how to evaluate it:

- Metrics used (mAP, precision, recall).
![image](https://github.com/user-attachments/assets/672293b1-421c-47e3-a32c-35dd5a144036)

- Example commands to display the confusion_matrix:
```bash  
from IPython.display import display, Image
Image(filename=f'/content/runs/detect/train2/confusion_matrix.png',width=600)
```
![image](https://github.com/user-attachments/assets/e3854d67-30c9-4636-bec4-64707a8d6c66)


## Results
Present the evaluation results quantitatively and visually. Include:

**Rock-Paper-Scissors dataset**:
- A summary of mAP scores: .
- Some samples of predicted images:



**Manufacturing items dataset**:
- A summary of mAP scores: 0.666 (66%).
- Some samples of predicted images:

   <img src="https://github.com/user-attachments/assets/b3f01219-754c-4ac2-adb8-a856924ecff6" alt="image" width="350" height="350" /> <img src="https://github.com/user-attachments/assets/0b5d6af4-0824-45df-9a28-c807a11a5861" alt="image" width="350" height="350" />
