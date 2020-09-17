# Object Detection:
In computer vision field, Object Detection is an important problem, which is used in various applications, namely Autonomous driving, Plate recognition, Face recognition, and Traffic jam estimation. A huge number of research has focused on improving object detection model in term of accuracy and speed. Before the deep learning era (from 2012 to now), almost methods utilize hand-craft features (SIFT [4], SURF [5], HOG [6], etc.) to search for regions containing objects. However, there is only a breakthrough when methods switch to deep learning. In 2017, authors in [7] proposed a framework named RetinaNet (see Fig. 7) which outperformed all previous classical methods by a large margin. RetinaNet is designed to predict objects in dense-multiscale style so that the deep network can deal with scale-invariance which classical cannot solve.

![Figure 7. RetinaNet architecture](https://github.com/anhocva214/learn-computer-vision/blob/master/images/Figure%207.%20RetinaNet%20Architecture.png)

***Figure 7. RetinaNet architecture***

Nevertheless, RetinaNet has a problem in its design: anchor-based. Concretely, during the training process, each anchor built on top of the network is assigned to a ground truth object if it overlaps with the ground truth box upper a threshold, otherwise, the anchor is considered as background. The weakness is there is a considerable number of ground truth objects which are not assigned to any anchor because the overlap does not exceed the defined threshold. This issue affects both the training and testing process, resulting in a low accuracy
at the end. To solve this problem, Zhi Tianet al. [8] propose a new object detection framework called FCOS.
FCOS, illustrated in Fig. 8, does not use anchors to match ground truth objects. Instead of anchor, FCOS is
trained with a new sampling strategy, in which, each location on the head of the network is assigned to a ground truth object if its corresponding location on the original image fall into the box. By changing the sampling strategy in conjunction with repealing the anchor design, FCOS cannot only run faster but also achieve higher accuracy (boost up to 4 mAP, comparing to RetinaNet).

![Figure 8. FCOS Architecture](https://github.com/anhocva214/learn-computer-vision/blob/master/images/Figure%208.%20FCOS%20Architecture.png)

***Figure 8. FCOS Architecture***

With this observing, PIF Lab has developed a new object detection model based on FCOS. Our target is a
new model which can obtain the same accuracy with the original FCOS, but run faster. Our strategy is replacing FCOS backbone (ResNet [9]) with other lightweight-yet-powerful backbones (MobileNetV2 [10], EfficientNet [11]). Besides, we also apply advanced loss functions to solve specific issues in the object detection problem: Focal loss [7], Adaptive Wing loss [12], Generalized IOU loss [13], etc. Currently, our object detection model can achieve the same accuracy with FCOS on the COCO dataset [14], but run four-time faster (60 FPS comparing to15 FPS).





