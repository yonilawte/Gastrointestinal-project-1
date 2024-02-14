# CVC-ClinicDB: Colonoscopy Polyp Detection

CVC-ClinicDB is a database of frames extracted from colonoscopy videos, containing examples of polyp frames along with corresponding ground truth masks. This repository contains the dataset, a UNet model with a ResNet34 encoder backbone trained for polyp detection, and evaluation metrics.

## Dataset Structure

The dataset consists of two main types of images:
1. **Original Images:** These are the frames extracted from colonoscopy videos and are located in the original directory. Each image is named according to its frame number, e.g., frame_number.tiff.
2. **Polyp Masks:** Corresponding ground truth masks indicating the region covered by polyps in the original images. These masks are located in the ground_truth directory and are also named based on their frame numbers, e.g., frame_number.tiff.
## Model Architecture
The polyp detection model utilizes the following architecture:

1. **UNet:** A convolutional neural network architecture commonly used for semantic segmentation tasks.
2. **ResNet34 Encoder Backbone:** The UNet model uses a ResNet34 pretrained encoder backbone to extract features from input images efficiently.
## Evaluation Metric

The evaluation metric used for assessing the model's performance is the Dice similarity coefficient (Dice). The Dice coefficient measures the overlap between the predicted and ground truth masks, providing a measure of segmentation accuracy.
## Results
The following results are provided:

1. **Image and Mask Examples:** Sample original images along with their corresponding ground truth masks.
2. **Loss and Dice Plots:** Visualization of the loss function and Dice coefficient during model training.
3. **Prediction Outputs:** Examples of the model's predictions, showcasing its ability to detect polyps.
## Frameworks and Dependencies
The project is implemented using the following frameworks and libraries:

1. **PyTorch:** Deep learning framework used for model development and training.
2. **smp:** Library providing pre-built implementations of various semantic segmentation models, including UNet.
3. **TorchMetrics:** Library for computing evaluation metrics, including the Dice coefficient.
4. **Plotly:** Visualization library used for generating interactive plots and graphs.
## Citation
If you use the CVC-ClinicDB dataset or the provided model in your research or work, please cite the relevant sources or publications.
