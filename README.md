# Steps to recreate

clone yolo v5

git clone https://github.com/ultralytics/yolov5.git

We need data in Darknet format

class x_center y_center height width

move to yolov5 directory create wheat_data folder and inside it create images and labels and inside this create valdiation and train folder

Run below commands

pip3 install -U -r requirements.txt

python3 processData.py

python3 train.py --img 1024 --batch 8 --epochs 100 --data wheat.yaml --cfg models/yolov5s.yaml --name wheat_model


for inference python3 detect.py --source /Users/gauravsrivastava/Desktop/ksolve/Kaggle/global-wheat-detection/test --weights /Users/gauravsrivastava/PycharmProjects/WheatHead/yolov5/runs/exp0_wheat_model/weights/best_yolov5x_0.pt

for video inference python3 detect.py -- source "source_folder"

for webcam inference python3 detect.py -- source 0


#Results saved to /Users/gauravsrivastava/PycharmProjects/WheatHead/yolov5/inference/output
