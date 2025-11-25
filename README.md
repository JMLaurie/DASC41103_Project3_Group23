DASC41103 Project 3 – Group 23
Overview:
This project uses a Convolutional Neural Network (CNN) to classify whether an image is the official Arkansas Razorback logo or not. The workflow includes:

Data collection, cleaning, and labeling

Model building and experimentation

Evaluation and metrics reporting

Recommendations for future improvements

Repository Structure
code/: ML_proj3_code.ipynb – main notebook for preprocessing, modeling, and evaluation

Razorback_Data/: Contains both official (*_AR.jpg) and unofficial (*_NA.jpg) logo images

output/: Saved models, evaluation metrics, and result visualizations

README.md: This project summary and responses to analysis questions

Analytical Questions & Answers
a. How did you create your dataset and determine the split of official logo versus not official logo?
Official logo images are labeled as *_AR.jpg; non-official as *_NA.jpg in the Razorback_Data folder.

All images were visually inspected for correctness; ambiguous cases were excluded to improve dataset clarity.

Stratified sampling was used to split the images into training, validation, and test datasets, preserving class balance.

b. Why did you choose the specific architecture for the final model?
CNNs are best suited for spatial pattern recognition, which is essential for logo image classification.

Our model features multiple convolutional and pooling layers for feature extraction, ReLU activations, dropout for overfitting control, and dense layers for binary classification.

This structure strikes a balance between capability and generalization while staying computationally efficient for our dataset.

c. How did you monitor and mitigate overfitting?
Overfitting was monitored by plotting both training and validation loss and accuracy after every training epoch.

Prevention techniques included:

Dropout layers to regularize model learning

Early stopping to halt training when validation loss stopped improving

Data augmentation with image flips and rotations (where used)

Careful parameter tuning

d. What future efforts do you recommend to improve model performance?
Expand the dataset with more images, especially diverse or ambiguous cases

Apply transfer learning by using pretrained CNNs (ResNet, VGG, etc.)

Incorporate advanced data augmentation

Broaden hyperparameter tuning with tools like Optuna or GridSearchCV

Use cross-validation for more robust results

Add model explainability tools (e.g., Grad-CAM) to visualize decisions

Authors
Jake Laurie and Jordan Short
