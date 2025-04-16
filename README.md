# Custom Model and Ablation Testing for Retinal Disease [Journal Publication]
 

## Overview
This project involves the development and evaluation of a custom deep learning model for classifying retinal diseases using fundus images. The work appears to be part of research intended for journal publication, focusing on both model architecture design and ablation testing to understand the impact of different model components.

## Key Components

### 1. Custom CNN Model Architecture
- The models are 6,8,9,10,12-layers convolutional neural network with 5 convolutional blocks. All of these architectures have been run individually and Ablation Testing was performed.
- Architectures includes:
  - Conv blocks with increasing filters (16 → 32 → 48 → 64 → 96)
  - Max pooling layers between blocks
  - Two dense layers (512 units each) before the final softmax classification layer
  - Total parameters: ~2.9 million

### 2. Dataset
- Uses a retinal disease dataset with 4 classes:
  - CNV (Choroidal Neovascularization)
  - DME (Diabetic Macular Edema)
  - DRUSEN
  - Normal
- Training set: 63,588 images
- Validation set: 15,896 images (20% split from training)
- Test set: 4,000 images

### 3. Training and Evaluation
- Uses ImageDataGenerator for data augmentation (rotation, shifts, shear, zoom)
- Implements learning rate reduction on plateau
- Achieves 94.13% test accuracy
- Strong performance across all classes (precision/recall/F1 all >90%)

### 4. Ablation Testing
- The notebook name suggests this is part of ablation testing (removing/modifying model components to study their impact)
- Likely examines the effect of different layers or configurations in the 12-layer model

### 5. Journal Publication Focus
- The project appears to be preparing results for academic publication
- Includes comprehensive evaluation metrics (accuracy, precision, recall, F1-score)
- Generates classification reports and confusion matrices

## Technical Implementation
- Built with TensorFlow/Keras
- Uses additional metrics like F1-score, precision, and recall
- Implements Grad-CAM (Gradient-weighted Class Activation Mapping) for model interpretability
- Includes learning rate scheduling and model checkpointing

## GitHub Repository Recommendations
When uploading to GitHub:
1. Structure the repository clearly with separate folders for:
   - Code (Jupyter notebooks)
   - Dataset information (though likely not the actual dataset)
   - Results/figures
   - Documentation

2. Include:
   - Detailed README explaining the project
   - Requirements.txt for dependencies
   - Citation information for the intended publication
   - License information

3. Consider adding:
   - Model architecture diagrams
   - More details about the ablation studies
   - Comparison with baseline models
   - Clinical significance of the results

This project demonstrates a rigorous approach to developing a specialized CNN for retinal disease classification, with thorough evaluation suitable for academic publication.
