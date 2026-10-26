# Face Emotion Recognition Using Neural Networks

## Overview
This project uses a neural network to classify facial expressions into seven emotions: **Angry, Disgust, Fear, Happy, Neutral, Sad, and Surprise**.

Users can upload an image or use their webcam to predict emotions and view confidence scores.

## 1. Data Loading and Preprocessing
- Loaded training and testing images using Keras.
- Separated images (**X**) and labels (**y**).
- Resized images to **48 × 48 pixels** and normalized pixel values.
- Inspected images and class distributions.
- Identified class imbalance, particularly in the **Disgust** category.

## 2. Baseline Model
Built a neural network using `Sequential`, `Flatten`, and two hidden `Dense` layers with **ReLU** activation.

The output layer used **Softmax** for seven-class classification.

**Baseline Accuracy: ~25%**

## 3. Model Improvement
Experimented with:
- Additional Dense layers and neurons.
- Adam optimizer and learning rate.
- Epochs, batch size, and shuffling.
- Class weights for imbalanced data.
- EarlyStopping callback and Dropout.

Class weights improved minority-class recognition but reduced overall accuracy.

**Best Test Accuracy: ~33.5%**

## 4. Model Evaluation
Evaluated the model using:
- Accuracy
- Precision, Recall, and F1-score
- Confusion Matrix
- Training and Validation Accuracy Graphs

The model performed better on **Happy, Neutral, and Surprise**, but struggled with Angry, Fear, and Disgust.

## 5. Application
Developed an interactive application using **Gradio**, allowing users to:
- Upload facial images.
- Capture images using a webcam.
- Predict emotions.
- View confidence scores for all seven classes.

## 6. Limitations and Challenges
This was my first experience working with **image datasets and Gradio**. Reading image files, preparing features and labels, and building the interactive application were challenging but valuable learning experiences.

The dataset was imbalanced, and some facial expressions were difficult to distinguish, limiting the model's accuracy.

## Tools Used
`Python` `Jupyter Notebook` `Keras` `TensorFlow` `NumPy` `Pandas` `Matplotlib` `Scikit-learn` `Gradio`

## References
- [Keras Documentation](https://keras.io/)
- [Gradio Documentation](https://www.gradio.app/docs)
- [Dataset] (https://www.kaggle.com/datasets/msambare/fer2013)
