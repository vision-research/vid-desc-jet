
# Offline Visually Impaired Assistive Tool 
This project aims to assist visually impaired individuals by generating audio descriptions of their environment using object detection and video description techniques. It has been tested and deployed on the NVIDIA Jetson Nano 4GB.


# Usage
Our project is implemented with PyTorch framework

### Environment
- Python = 3.6.9
- PyTorch = 1.8.
- OpenCV = 4.5.3 with GPU support

### Jetson Nan setup
For getting a Pre-installed frameworks with GPU support for the Jetson Nano board, download the Jetson Nano image file provided in the following repo: https://github.com/Qengineering/Jetson-Nano-image.git


### Software setup

1- Clone this repo https://github.com/vision-research/vid-desc-nano.git

2- In Yolov7 folder, Clone the yolov7 repo: https://github.com/WongKinYiu/yolov7.git

3- Replace the detect.py file with modified vesion in this repo to return an audio output rather than text

4- In piper folder, download an English model with its Confg file from the following link: https://github.com/rhasspy/piper/blob/master/VOICES.md

5- Download an English VOSK model using this link: https://alphacephei.com/vosk/models

6- In Video_Swin_Transformer folder, Clone the following repo: https://github.com/SwinTransformer/Video-Swin-Transformer.git

7- Run this file for obtaining audio description:
```bash
  python Inference.py
```

### For downloading MSVD videos use link in:
https://www.cs.utexas.edu/users/ml/clamp/videoDescription/

the texts file are located in data folder in this repo



### For downloading MS COCO dataset:
https://cocodataset.org/#download


### For video captioning training run   

```bash
  python training_vid_cap.py
```
or use the trained model in the checkpoints folder

### For feature extraction run   

```bash
  python Swin_feat_extraction.py
  python EffeB3_feat_extraction.py
```
# Hardware components




# Results



Video description



Object detection: a) yolov7-tiny  b) yolov7-W6

    
## Acknowledgements


- https://github.com/Qengineering/Jetson-Nano-image
- https://github.com/SwinTransformer/Video-Swin-Transformer
- https://github.com/haofanwang/video-swin-transformer-pytorch
- https://github.com/WongKinYiu/yolov7?tab=readme-ov-file
- https://github.com/rhasspy/piper
- https://alphacephei.com/vosk/

Some code in this project is based on the following repositories:
- https://github.com/hobincar/RecNet
- https://github.com/v-iashin/BMT