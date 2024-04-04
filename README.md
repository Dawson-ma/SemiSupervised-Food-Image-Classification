# Semi-Supervised Learning - Food Image Classification

Classifying 11 types of food images utilize semi-supervised learning techniques with a non-pretrained ResNet18 model. The model has demonstrated a commendable accuracy rate of **79.14%** on the task.

## Data Preparation

The dataset is divided into training, validation, and unlabeled sets for model training and evaluation.

## Model Training

The [ResNet18](https://pytorch.org/vision/main/models/generated/torchvision.models.resnet18.html) architecture serves as the model backbone.

### Training Procedure

1. **Training on Labeled Data**: The model is initially trained on the labeled portion of the dataset.
2. **Prediction on Unlabeled Data**: The trained model is then used to predict labels for the unlabeled data.
3. **Thresholding**: Predictions on the unlabeled data are thresholded, and samples with confident predictions are considered for pseudo-labeling.
4. **Incorporating Unlabeled Data**: The original dataset is augmented with the pseudo-labeled data obtained from the previous step.
5. **Iterative Process**: The process is repeated iteratively to refine the model's performance.

## Dataset

The dataset can be accessed [here](https://drive.google.com/file/d/1vufDjKxj4IwRni11uxjM0CSim5WehscA/view?usp=sharing).

For detailed implementation and usage instructions, please refer to the provided [code](https://github.com/Dawson-ma/SemiSupervised-Food-Image-Classification/blob/main/Semisupervised_food_classification.ipynb).
