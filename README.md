# MRI-Scan-CNN

Dataframe containing image , mask and image id as input and perform 2 type of prediction on the image
Initially, image is passed through the classification network(ResNet) which predicts whether the image has defect or not, the model
predicts 98% accuracy that the image has defect or not (defect means tumor) , if the model labels the images as defect it passes the image to the
segmentation network (U-net build from scratch) then the  location of defect is found.

<img width="670" alt="image" src="https://github.com/user-attachments/assets/3e720c7c-2145-4960-aecd-6f41ee6d9ef6">

leveraging transfer learning with resunet architecture which was original trainned on imagenet dataset(1 million images) and 1000 classes we remove the head and add custom head for binary classification

<img width="630" alt="image" src="https://github.com/user-attachments/assets/7f46c57d-5378-4a12-924f-86bbabbba3a2">


![image](https://github.com/user-attachments/assets/0b929f85-8035-40dd-a86e-35edde82cd22)

<img width="326" alt="image" src="https://github.com/user-attachments/assets/1c29c17a-8ed6-462d-8951-4a6ff8a162d6">
<img width="653" alt="image" src="https://github.com/user-attachments/assets/50d1593a-1591-4889-90b4-81589aff53d6">
<img width="362" alt="image" src="https://github.com/user-attachments/assets/b72b93d3-43ae-459b-91ba-9e543db55377">
![Uploading image.png…]()

