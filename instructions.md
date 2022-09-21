## Train an Object Detection Model in Azure Machine Learning

### Prepare object detection codebase of interest
1. Download codebase locally: https://github.com/open-mmlab/mmdetection
2. Upload it to your workspace
![image](https://user-images.githubusercontent.com/62900532/191342347-8443a567-29d7-4075-aa77-bf2a4730e0e6.png)
3. Identify the model configuration file you wish to train. For this example, let's choose configs/swin/mask_rcnn_swin-t-p4-w7_fpn_1x_coco.py. From that configuration file identify the _base_/datasets file it uses to make the dataset. In this example, it is _base_/datasets/coco_instance.py.
![Screenshot 2022-09-20 201812](https://user-images.githubusercontent.com/62900532/191387190-2734734b-bf10-4100-98e3-efdb02ec0eb6.png)
5. Open the _base_/datasets/coco_instance.py file and specify the classes field to contain the class id values found in your coco dataset. Also, add the classes parameter to the pipeline section.
![Screenshot 2022-09-20 150612](https://user-images.githubusercontent.com/62900532/191344423-9f28b21d-b17a-4e49-9b8e-677cb3109f65.png)
5. Return to your model configuration file configs/swin/mask_rcnn_swin-t-p4-w7_fpn_1x_coco.py. From that configuration file identify the _base_/models file it uses to create the model architecture. In this example, it is _base_/models/coco_instance.py. 
![Screenshot 2022-09-20 201256](https://user-images.githubusercontent.com/62900532/191387071-6a672b4a-8543-457f-8423-acda851ba4b2.png)
6. For this particular model architecture, you will need to change the bbox_head.num_classes and mask_head.num_classes to match the number of classes in your dataset.
[Screenshot 2022-09-20 151844](https://user-images.githubusercontent.com/62900532/191345692-477fa1fe-78f9-4e39-9523-26c46f94190f.png)
7. If your model is going to use pretrained weights, copy the location pointing to the pretrained weights to your browser to download the file locally. 
![Screenshot 2022-09-20 201812](https://user-images.githubusercontent.com/62900532/191387266-a0cc9ef8-6380-4c09-91ac-58f60d4f7894.png)
8. Import it into your AML workspace and update the pretrained_weights path to point to the new location.
![Screenshot 2022-09-20 202936](https://user-images.githubusercontent.com/62900532/191388176-8f4a62d8-d7eb-4d2e-acb0-22372c358d60.png)
