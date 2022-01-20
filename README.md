# YOLO5-helmet_detection
![photo_۲۰۲۲-۰۱-۲۰_۰۷-۴۲-۳۲ (2)](https://user-images.githubusercontent.com/80622132/150272115-e647fe9f-d911-4c98-b135-65eb64f4d839.jpg)
![media_images_BoundingBoxDebugger_19_9(2)](https://user-images.githubusercontent.com/80622132/150272269-4c321420-82af-4c12-a385-cf9cfbd4eb8c.png)
# Instalation
```
!pip install -U -r requirements.txt
```

# Dataset
Database in YOLO format with labels: 'helmet' as 1, and 'head as 0.
Split approximately train/valid/test 0.7/0.2/0.1
Datast link:[helmet](https://drive.google.com/file/d/1-9lFSOfk1lGW2pNi3rZpueEAw92StTrg/view?usp=sharing)

# Train

```
!python train.py --img 256 --batch 64 --epochs 20 --data helm.yaml --weights yolov5s.pt
```

- For train on your dataset, you must creat dataset.yaml file.
```
train: ./dataset/images/train/

val: ./dataset/images/valid/


# number of classes

nc: 2



# class names

names: ['head', 'helmet']
```

# Inference
 run the following command

```
!python inference.py --weights runs/train/exp10/weights/best.pt --img 640 --conf 0.4 --source inputs/helm_000197.jpg
```




