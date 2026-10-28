# Handwritten Digit Recognition Using CNN

A Deep Learning mini-project that recognizes handwritten digits (0–9) using a Convolutional Neural Network (CNN). The model is trained on the MNIST dataset using Python and TensorFlow/Keras.

## Project Overview

Handwritten digit recognition is a computer vision task in which a deep learning model identifies numerical digits from images. This project uses a CNN to learn visual patterns from handwritten digit images and predict the corresponding digit.

The model accepts a 28 × 28 grayscale image and classifies it into one of ten categories, from 0 to 9.

## Objectives

- Understand the fundamentals of Convolutional Neural Networks.
- Implement convolutional and pooling layers for image classification.
- Train a CNN using the MNIST handwritten digit dataset.
- Evaluate the model using test loss and accuracy.
- Visualize training and validation accuracy.
- Display predictions alongside the actual digit labels.

## Technologies Used

- **Programming language:** Python
- **Deep learning framework:** TensorFlow/Keras
- **Libraries:** NumPy, Matplotlib
- **Environment:** Google Colab / Jupyter Notebook
- **Dataset:** MNIST handwritten digits

## Dataset Description

The MNIST dataset contains 70,000 grayscale images of handwritten digits.

| Property | Description |
|---|---|
| Total images | 70,000 |
| Training images | 60,000 |
| Testing images | 10,000 |
| Image dimensions | 28 × 28 pixels |
| Color channels | 1 (grayscale) |
| Number of classes | 10 |
| Class labels | Digits 0–9 |

The images are normalized by dividing pixel values by 255, converting them to a range between 0 and 1.

## CNN Architecture

The model uses the following architecture:

```text
Input Image (28 × 28 × 1)
          |
          v
Convolutional Layer
32 filters, 3 × 3, ReLU
          |
          v
Max Pooling Layer (2 × 2)
          |
          v
Convolutional Layer
64 filters, 3 × 3, ReLU
          |
          v
Max Pooling Layer (2 × 2)
          |
          v
Flatten Layer
          |
          v
Dropout Layer (0.5)
          |
          v
Fully Connected Layer
10 neurons, Softmax
          |
          v
Predicted Digit (0–9)
```

### Layer Descriptions

1. **Input layer:** Accepts a 28 × 28 grayscale image.
2. **First convolutional layer:** Uses 32 filters to extract basic image features.
3. **First max pooling layer:** Reduces spatial dimensions while retaining important features.
4. **Second convolutional layer:** Uses 64 filters to learn more complex patterns.
5. **Second max pooling layer:** Further reduces the feature map dimensions.
6. **Flatten layer:** Converts the feature maps into a one-dimensional vector.
7. **Dropout layer:** Randomly disables 50% of selected activations during training to help reduce overfitting.
8. **Output layer:** Uses 10 neurons and softmax activation to produce class probabilities for digits 0–9.

## Model Training

The model is compiled using the Adam optimizer and categorical cross-entropy loss.

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Loss function | Categorical cross-entropy |
| Batch size | 128 |
| Training epochs | 15 |
| Validation split | 10% of training data |
| Evaluation metric | Accuracy |

## Results

The following values were obtained from the completed notebook.

| Metric | Result |
|---|---:|
| Test accuracy | 99.25% |
| Test loss | 0.02315 |
| Training epochs | 15 |

The training and validation accuracy graph shows that both accuracy curves remain high throughout training. The prediction visualization also demonstrates the model classifying sample handwritten digits correctly.

These results apply to the MNIST test dataset and do not guarantee the same performance on arbitrary photographs or handwritten images from other sources.

## Sample Predictions

The notebook displays ten test images with their predicted and actual digit labels.

In the recorded sample output, the predicted labels match the actual labels for all ten displayed images.

## How to Run the Project

1. Open the notebook in Google Colab.
2. Run the code cells sequentially.
3. Allow Keras to download the MNIST dataset.
4. Train the CNN model.
5. Evaluate the model on the test dataset.
6. Generate the training and validation accuracy graph.
7. Run the prediction visualization cell to view predicted and actual digits.

## Applications

- Handwritten digit recognition
- Automatic digit entry from scanned forms
- Postal code and number recognition
- Digit recognition in document processing
- Educational demonstrations of computer vision and deep learning

## Advantages

- Simple and effective CNN architecture.
- High test accuracy on the MNIST dataset.
- Automatic feature extraction through convolutional layers.
- Easy to implement and demonstrate using Google Colab.
- Supports visualization of predictions and training performance.

## Limitations

- The model is trained on MNIST's 28 × 28 grayscale images.
- Performance may decrease on noisy, rotated, or differently styled images.
- The current notebook demonstrates prediction on dataset images rather than a complete image-upload web application.

## Future Enhancements

- Add a drawing canvas for users to draw digits.
- Allow users to upload handwritten digit images.
- Build a simple web interface using Streamlit or Flask.
- Evaluate the model on additional handwritten digit datasets.
- Analyze misclassified images and improve generalization.

## Repository

GitHub: https://github.com/CherukuriRamCharan/handwritten-digit-recognition-cnn

## References

1. Keras, *Simple MNIST ConvNet*: https://keras.io/examples/vision/mnist_convnet/
2. Keras source code: https://github.com/keras-team/keras-io/blob/master/examples/vision/mnist_convnet.py
3. TensorFlow documentation: https://www.tensorflow.org/
4. MNIST database: http://yann.lecun.com/exdb/mnist/

## Author

**Ram Charan Cherukuri**  
B.Tech – Computer Science and Engineering  
Prasad V. Potluri Siddhartha Institute of Technology

Academic Year: 2026–2027
