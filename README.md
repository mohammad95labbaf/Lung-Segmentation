# Lung-Segmentation

This repository contains code and resources for segmenting abnormal regions in chest X-ray images using deep learning techniques. The goal is to accurately identify pneumonia, tumors, or other lung-related abnormalities.

## Dataset
- The dataset used in this project is sourced from Kaggle and is named `nikhilpandey360/chest-xray-masks-and-labels`.
- It includes original chest X-ray images along with corresponding lung masks.
- Ensure you have downloaded the dataset before proceeding.

## Data Preparation
1. **Data Augmentation**:
    - Apply data augmentation techniques (e.g., flipping, rotation) to increase dataset diversity.
    - Augmented data helps improve model generalization.

2. **Preprocessing**:
    - Crop or resize images to focus on the lung area.
    - Normalize pixel values to a consistent range (e.g., [0, 1]).

## Model Architecture
- We experimented with two residual ResNets:
    1. **Conventional ResNet**:
        - Utilizes standard CNN layers.
        - Captures hierarchical features through residual connections.
    2. **Depthwise Separable ResNet**:
        - Employs depthwise separable convolutions for efficiency.
        - Reduces the number of parameters while maintaining performance.

## Performance Evaluation
- We assessed model performance using the **Dice coefficient** (F1 score).
- This metric quantifies the overlap between predicted and true positive regions.

## Visualization
- Created segmentation figures to visualize model predictions.
- Compare predicted masks with actual abnormalities in X-rays.

## Next Steps
- Fine-tune hyperparameters, explore additional architectures, or incorporate other evaluation metrics.
- Continue refining the model based on performance and domain-specific requirements.

## Instructions for Kaggle API
1. **Download Kaggle API**:
    - Install the Kaggle API by running `pip install kaggle`.

2. **Kaggle API Token**:
    - Go to your Kaggle account settings and generate an API token.
    - Save the token as `kaggle.json` in the root directory of this repository.

3. **Download Dataset**:
    - Use the Kaggle API to download the dataset:
        ```
        kaggle datasets download -d nikhilpandey360/chest-xray-masks-and-labels
        ```

4. **Upload Kaggle API Token to Colab/Notebook**:
    - If using Colab or Jupyter Notebook, upload the `kaggle.json` token to your environment.
    - Use the following code snippet:
        ```python
        from google.colab import files
        files.upload()
        ```

5. **Unzip Dataset**:
    - Unzip the downloaded dataset:
        ```
        unzip chest-xray-masks-and-labels.zip
        ```

Feel free to explore, contribute, and enhance this project! 🌟👩‍⚕️🔍
