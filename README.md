UCSD COGS 181 Deep Learning Final Project: Performance Analysis of Modern Pedestrian and Vehicle Detection Approaches
=======================================================

Author: Yichen Li, Suli Huang


Abstract:
=======================================================

We are here to present a investigation of influences of different meta-architectures, feature extractors and network hyper parameters to the speed and precision of the padestrian and vehicle detection and localization. Specifically, we perform three approaches: Faster R-CNN, Yolo and SSD, combining with two feature extractors: Darknet19, VGG16, and in Faster R-CNN algorithm, we use different image sizes and different object proposals. 

After the analysis, the major findings are: the precision depends largely on how deep (big) the feature extractor is; decreasing size of input image would increase the speed of Faster R-CNN but with a decreasing precision; decreasing number of object proposals would increase the speed of Faster R-CNN, with little effect on the precision.

Setup:
=======================================================

Here are some details of the test of three different meta- architecture:
1. Faster R-CNN: We used pretrained imagenet VGG16 model, and tested on voc2007 dataset.
2. Yolo: We used pretrained coco, VOC 2007+2012, dark- net19 model, and tested on voc2007 dataset.
3. SSD: We used pretrained VOC07+12+COCO trainval, SSD-300 VGG-based model, and tested on voc2007 dataset.

The initial hyper parameter for each meta-architecture:
Faster R-CNN
– Batch size: 1
– RPN batch size: 256
– Number of regional proposal: 300 – Image rescale: 600*1000
– Test NMS threshold: 0.3
Yolo
– Batch size: 64
– Threshold: 0.5 SSD
– Batch size: 1
– Nms threshold: 0.45
– Matching threshold: 0.5
SSD
– Batch size: 1
– Nms threshold: 0.45
– Matching threshold: 0.5


Report:
=======================================================

For more details of implementation and evaluation, please refer to COGS181_YichenLi.pdf

Codes & References:
=======================================================

1. https://github.com/liyichen7887/yolo.git 
2. https://github.com/liyichen7887/faster-rcnn.git 
3. https://github.com/huangsuli/SSD-Tensorflow
