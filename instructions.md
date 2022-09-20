## Train an Object Detection Model in Azure Machine Learning

### Import in object detection codebase of interest
1. Download codebase locally: https://github.com/open-mmlab/mmdetection
2. Upload it to your workspace
![image](https://user-images.githubusercontent.com/62900532/191342347-8443a567-29d7-4075-aa77-bf2a4730e0e6.png)
3. Update the configs/_base_/datasets/coco_instance.py file to use the class id values for your dataset
![image](https://user-images.githubusercontent.com/62900532/191343523-da4a9012-b00a-4c26-ae2b-1ba9e0b2a64d.png)
