This package is based on [MMdetection](https://mmdetection.readthedocs.io/en/v2.0.0/) v2.0.

MMdetection installation and usage guidelines provided in it's documentation. A slightly modified dockerfile is also provided here.

To run the detector and test on images or videos, two main components are needed.
The first one are the configuration files which describe which detector is used. The second component are the trained models using that specific detector.
When providing the input to MMdetection, select the proper configuration file with its respective trained model. The list below describes that.
Use example to test an image or video as in [here](https://mmdetection.readthedocs.io/en/v2.0.0/getting_started.html#inference-with-pretrained-models). 

Exact correspondence is as follows:

> VA Beach Traffic Dataset

Config file: custom_configs/va_beach/faster_rcnn_x101_32x4d_fpn_1x_coco.py

Model file: va_beach.pth

Classes: classes_traffic.txt

> SHRP2 original split

Config file: custom_configs/shrp2/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco.py

Model file: SHRP2_original_split.pth

Classes: classes_shrp2_train.txt

> Extra Data only:
Config file: custom_configs/shrp2+extra/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco.py

Model file: extra_data_only.pth

Classes: classes_extra.txt

> SHRP2 original split + Extra Data (Outside Objects set)

Config file: custom_configs/shrp2+extra/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco.py

Model file: shrp2_original_split+extra_data_outside_objects.pth

Classes: classes_shrp2_extra.txt

> SHRP2 (with more SHRP2 images on test set) + Extra Data (Outside Objects set)

Config file: custom_configs/shrp2+extra/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco.py

Model file: shrp2_less_on_train_set+extra_data_outside_objects.pth

Classes: classes_shrp2_extra.txt

> Extra Data (Billboards only)

Config file: custom_configs/billboards/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco.py

Model file: billboards_only.pth

Classes: classes_billboard.txt

> Extra Data (Inside Objects set), each config file corresponds to each model and classes file with the same order.

Config file: 

custom_configs/extra_inside_objects/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco.py

custom_configs/extra_inside_objects/cascade_rcnn_r101_fpn_dconv_c3-c5_1x_coco2.py

custom_configs/extra_inside_objects/htc_x101_32x4d_fpn_16x1_20e_coco.py

Model file: 

more categories: inside_objects_1.pth

less categories: inside_objects_2.pth

less categories with mask: inside_objects_mask

Classes: 

classes_inside_objects.txt

classes_inside_objects2.txt

classes_inside_objects2.txt



