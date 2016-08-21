# VGG19_py_faster_rcnn

Here is VGG19 end to end training model for Py-Faster-Rcnn.
It performs slightly better than VGG16.


## How to use it for training ?


1. Copy models folder to your Py-Faster-Rcnn directory.
2. Download VGG19 model trained on ImageNet for fine tuning.
* go to data/imagenet_models
* download [VGG19_ILSVRC](http://www.robots.ox.ac.uk/~vgg/software/very_deep/caffe/VGG_ILSVRC_19_layers.caffemodel)
* save it as VGG19.v2.caffemodel

3. Run training:

```Shell
cd $FRCN_ROOT
./experiments/scripts/faster_rcnn_end2end.sh [GPU_ID] VGG19 pascal_voc
```

## Pretrained Faster R-CNN 

Model that was trained on VOC 2007 trainval is available for download [here](http://cb.cr/Kzgc). 

## Results:

 model                    | training data                          | test data            | mAP   |
:------------------------:|:--------------------------------------:|:--------------------:|:-----:|
 Faster RCNN, VGG-16      | VOC 2007 trainval                      | VOC 2007 test        | 69.5% |
 Faster RCNN, **VGG-19**  | VOC 2007 trainval                      | VOC 2007 test        | 70.4% |

## Per category results:

 category    | mAP VGG16 | mAP VGG19 |
:-----------:|:---------:|:---------:|
 aeroplane   | 69.1%     | 70.2%     |
 bicycle     | 78.3%     | 79.9%     |
 bird        | 68.9%     | 67.4%     |
 boat        | 55.7%     | 60.1%     |
 bottle      | 49.7%     | 53.5%     |
 bus         | 77.6%     | 76.1%     |
 car         | 79.7%     | 79.9%     |
 cat         | 85.0%     | 86.2%     |
 chair       | 51.0%     | 51.2%     |
 cow         | 76.1%     | 73.6%     |
 diningtable | 64.2%     | 68.1%     |
 dog         | 82.0%     | 83.6%     |
 horse       | 80.5%     | 80.3%     |
 motorbike   | 76.2%     | 77.5%     |
 person      | 75.8%     | 77.8%     |
 pottedplant | 38.4%     | 42.9%     |
 sheep       | 71.3%     | 66.9%     |
 sofa        | 65.4%     | 66.9%     |
 train       | 77.8%     | 77.1%     |
 tvmonitor   | 66.1%     | 67.9%     |




