# CVC-ClinicDB: Colonoscopy Polyp Detection

<p align="center">
  <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/colonoscopy.png?raw=true" alt=""/>
</p>

CVC-ClinicDB is a database of frames extracted from colonoscopy videos, containing examples of polyp frames along with corresponding ground truth masks. This repository contains the dataset, a UNet model with a ResNet34 encoder backbone trained for polyp detection, and evaluation metrics.

## Acknowledgements

 - [Kaggle dataset](https://www.kaggle.com/datasets/balraj98/cvcclinicdb)

## Dataset Structure

The dataset consists of two main types of images:
  - **Original Images:** These are the frames extracted from colonoscopy videos and are located in the original directory. Each image is named according to its frame number, e.g., frame_number.tiff.
  - **Polyp Masks:** Corresponding ground truth masks indicating the region covered by polyps in the original images. These masks are located in the ground_truth directory and are also named based on their frame numbers, e.g., frame_number.tiff.

<p align="center">
    <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/im_mask.png?raw=true" alt=""/>
</p>

## Model Architecture
The polyp detection model utilizes the following architecture:

  - **UNet:** A convolutional neural network architecture commonly used for semantic segmentation tasks.
   
   <p align="center">
    <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/unet.png?raw=true" alt=""/>
  </p>
  
  - **ResNet34 Encoder Backbone:** The UNet model uses a ResNet34 pretrained encoder backbone to extract features from input images efficiently.

   <p align="center">
    <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/ResNet34.png?raw=true" alt=""/>
  </p>

   
## Evaluation Metric

The evaluation metric used for assessing the model's performance is the Dice similarity coefficient (Dice). The Dice coefficient measures the overlap between the predicted and ground truth masks, providing a measure of segmentation accuracy.

<p align="center">
  <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/dice.png?raw=true" alt=""/>
</p>

## Results
The following results are provided:

  - **Loss and Dice Plots:** Visualization of the loss function and Dice coefficient during model training.
  <p align="center">
    <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/loss.png?raw=true" alt=""/>
  </p>
  
  - **Prediction Outputs:** Examples of the model's predictions, showcasing its ability to detect polyps.
  <p align="center">
    <img src="https://github.com/yonilawte/Gastrointestinal-project-1/blob/main/images/predict.png?raw=true" alt=""/>
  </p>
  
## Frameworks and Dependencies
The project is implemented using the following frameworks and libraries:

  - **PyTorch:** Deep learning framework used for model development and training.
  - **smp:** Library providing pre-built implementations of various semantic segmentation models, including UNet.
  - **TorchMetrics:** Library for computing evaluation metrics, including the Dice coefficient.
  - **Plotly:** Visualization library used for generating interactive plots and graphs.

