# Jordans 1,5,11 classification

 The tools and dataset provided will be used to classify and idenitfy air jordans.

## Requirements

 must ``import pytorch`` and ```import torchvision``` 

## The Algorithm

The Algorithim is a method implemented in the AI to find patterns within datasets. The code works by depdning on pytorch and finding patterns within datasets.

## Running this project

step-1 install pytorch using ```./install-pytorch.sh```

step-2 download dataset via wget or manually 

step-3 when in jetson-inference/python/training/classification/data run ```python3 train.py --model-dir=models/jordans data/jordans  --batch-size=4 --workers=1 --epochs=30 data/jordans``` to train AI.

step-4 after training convert to ONNX with ```python3 onnx_export.py --model-dir=models/```

step-5 test images with renset using ```imagenet --model=models/jordans/resnet18.onnx --labels=data/jordans/labels.txt   --input_blob=input_0 --output_blob=output_0 data/jordans/test/<file of choice>/<image of choice>```

 
 
