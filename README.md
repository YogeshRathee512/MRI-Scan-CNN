# MRI-Scan-CNN

Dataframe containing image , mask and image id as input and perform 2 type of prediction on the image
Initially, image is passed through the classification network(ResNet) which predicts whether the image has defect or not, the model
predicts 98% accuracy that the image has defect or not (defect means tumor) , if the model labels the images as defect it passes the image to the
segmentation network (U-net build from scratch) then the  location of defect is found.

<img width="670" alt="image" src="https://github.com/user-attachments/assets/3e720c7c-2145-4960-aecd-6f41ee6d9ef6">

leveraging transfer learning with resunet architecture which was original trainned on imagenet dataset(1 million images) and 1000 classes we remove the head and add custom head for binary classification.

<img width="630" alt="image" src="https://github.com/user-attachments/assets/7f46c57d-5378-4a12-924f-86bbabbba3a2">

Here are the score of confusion matrix 
![image](https://github.com/user-attachments/assets/0b929f85-8035-40dd-a86e-35edde82cd22)

After the model makes prediction we draw a confusion matrix .
In medical diagnosis, precision maybe  more important than recall as false positives can lead to unnecessary treatments and procedures that carry risks for patients.
Whereas recall might be more important because it's important to catch as many positive cases as possible, even if it leads to some false positives.

<img width="326" alt="image" src="https://github.com/user-attachments/assets/1c29c17a-8ed6-462d-8951-4a6ff8a162d6">
Building a resblock that will be used while making U-NET From Scratch for Image Segmentation. Resblock generally has residual connection which are used to maintain input signal these residual connections enable as to make very deep residual networks .
<img width="653" alt="image" src="https://github.com/user-attachments/assets/50d1593a-1591-4889-90b4-81589aff53d6">
<img width="362" alt="image" src="https://github.com/user-attachments/assets/b72b93d3-43ae-459b-91ba-9e543db55377">
![Uploading image.png…]()

