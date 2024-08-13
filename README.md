# MRI-Scan-CNN 🧠

This project involves developing a deep learning pipeline that processes MRI scans to detect and locate brain tumors. The process is divided into two main tasks:

1. **Classification**: Identify whether the MRI scan contains a defect (tumor).
2. **Segmentation**: If a defect is detected, precisely locate it within the image.

## Project Pipeline Overview 🔄

Initially, the MRI scan is passed through a classification network (ResNet) to determine if the image contains a defect. If a defect is detected, the image is then passed to a segmentation network (U-Net) to identify the exact location of the defect.

<p align="center">
  <img width="670" alt="Project Pipeline" src="https://github.com/user-attachments/assets/3e720c7c-2145-4960-aecd-6f41ee6d9ef6">
</p>

## Transfer Learning with ResUNet 🌐

We leverage transfer learning using the ResUNet architecture, originally trained on the ImageNet dataset (1 million images, 1000 classes). The head is removed, and a custom head is added for binary classification.

<p align="center">
  <img width="630" alt="ResUNet Architecture" src="https://github.com/user-attachments/assets/7f46c57d-5378-4a12-924f-86bbabbba3a2">
</p>

## Model Performance and Evaluation 📊

After the model makes predictions, a confusion matrix is drawn to evaluate its performance. In medical diagnosis, precision might be more critical than recall because false positives can lead to unnecessary treatments. However, recall is also crucial to ensure all possible positive cases are caught.

<p align="center">
  <img width="326" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/0b929f85-8035-40dd-a86e-35edde82cd22">
</p>

<p align="center">
  ![Screenshot 2024-08-10 165621](https://github.com/user-attachments/assets/881a5ddf-97df-4617-ade2-7bd67a3f7fb9)
</p>

## Building the ResBlock 🧱

ResBlocks with residual connections are used to maintain input signals. These residual connections enable the creation of very deep residual networks, essential for the U-Net architecture.

<p align="center">
  <img width="653" alt="ResBlock" src="https://github.com/user-attachments/assets/50d1593a-1591-4889-90b4-81589aff53d6">
</p>

## ResUNet Structure 🏗️

The ResUNet structure consists of four downsampling blocks, one forward block, and four upsampling blocks. This design ensures the network can capture both high-level and detailed features necessary for accurate segmentation.

<p align="center">
  <img width="362" alt="ResUNet Structure" src="https://github.com/user-attachments/assets/b72b93d3-43ae-459b-91ba-9e543db55377">
</p>

## Results of Applying the CNN 🎯

The model successfully classifies and segments tumors in MRI scans. Below is an example of the output from our model, showing the detected and segmented tumor regions.

<p align="center">
  <img width="841" alt="Model Output" src="https://github.com/user-attachments/assets/ba12c66f-e842-4fa9-b35a-679c21853716">
</p>

The confusion matrix demonstrates the model's performance. With an accuracy of 98%, the classification model is highly reliable. In medical diagnosis, precision is critical as false positives can lead to unnecessary treatments. However, high recall is also essential to ensure no positive cases are missed.

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/mri-scan-cnn.git
   cd mri-scan-cnn
