## YOLO Models:Object Detection with Qualcomm RB5 ( IMAGE )

## Overview of YOLO
YOLO (You Only Look Once) is a cutting-edge object detection system designed for real-time processing. On a Pascal Titan X GPU, it achieves 30 frames per second (FPS) and a mean Average Precision (mAP) of 57.9% on the COCO test-dev dataset.

## Performance Comparison
YOLOv3 stands out for its speed and accuracy. When evaluated with mAP at 0.5 IOU, YOLOv3 matches the accuracy of Focal Loss but is approximately four times faster. Additionally, you can easily balance speed and accuracy by adjusting the model size without the need for retraining.

## How YOLO Works
Unlike traditional detection systems that use classifiers or localizers on an image at multiple locations and scales, YOLO applies a single neural network to the entire image. This network splits the image into regions and predicts bounding boxes and probabilities for each region, considering the whole image context for predictions. This approach allows YOLO to perform detections with a single network evaluation, making it significantly faster than models like R-CNN and Fast R-CNN.

## YOLOv3 Improvements
YOLOv3 introduces several enhancements such as multi-scale predictions, an improved backbone classifier, and more. For detailed information, refer to the YOLOv3 paper.

## Using Pre-Trained Models
To detect objects using a pre-trained YOLO model, follow these steps:

1. Clone the Darknet repository:
   ```bash
   git clone https://github.com/pjreddie/darknet
   cd darknet
   make
2. Download the pre-trained weights:
   ```bash
   wget https://pjreddie.com/media/files/yolov3.weights
3. Run the detector:
```bash
./darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg

## Using Pre-Trained Models
