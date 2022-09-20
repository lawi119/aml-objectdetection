## Train an Object Detection Model in Azure Machine Learning

### Import in object detection codebase of interest
1. Download codebase locally: https://github.com/open-mmlab/mmdetection
2. Upload it to your workspace
![image](https://user-images.githubusercontent.com/62900532/191342347-8443a567-29d7-4075-aa77-bf2a4730e0e6.png)
3. Update the configs/_base_/datasets/coco_instance.py file to use the class id values for your dataset and to specify the custom classes in the pipeline sections
![Screenshot 2022-09-20 150612](https://user-images.githubusercontent.com/62900532/191344423-9f28b21d-b17a-4e49-9b8e-677cb3109f65.png)
4. For the config you wish to train you will have to change the number of classes in the given network architecture to match the number of classes in your dataset![Screenshot 2022-09-20 151844](https://user-images.githubusercontent.com/62900532/191345692-477fa1fe-78f9-4e39-9523-26c46f94190f.png)
