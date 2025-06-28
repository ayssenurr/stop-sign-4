# Stop Sign Detection with YOLOv5

This project aims to detect STOP signs using a deep learning-based object detection model (YOLOv5).

## Selected Model
- YOLOv5s (pre-trained on COCO dataset)
- Chosen for its lightweight structure and fast inference

## Training Parameters
- Epochs: 30  
- Batch size: 16  
- Image size: 640x640  
- Optimizer: SGD  
- Learning rate: 0.01  

## Testing
The model was tested on a dataset containing 5 STOP sign images.

```bash
!python detect.py \
  --weights runs/train/stop_sign_model/weights/best.pt \
  --img 640 \
  --conf 0.4 \
  --source stop_sign_dataset \
  --project runs/detect \
  --name stop_sign_test_output \
  --exist-ok
