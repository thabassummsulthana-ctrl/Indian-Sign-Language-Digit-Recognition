##Indian Sign Language Digit Recognition

This project is about building a real-time Indian Sign Language digit recognition system using deep learning and computer vision.
The main idea is to recognize hand gestures representing digits (0–9) through a webcam and predict them instantly. Instead of using a ready-made dataset, 
I created my own dataset using a webcam to make the project more practical and realistic.



##  Project Overview

In this project, I worked on the complete machine learning pipeline starting from data collection to real-time prediction.
I captured images of hand gestures using a webcam, trained a deep learning model on those images, and then used the trained model to predict digits in real time.
This project helped me understand how computer vision and deep learning can be combined to solve real-world problems like sign language recognition.



## Technologies Used

* Python – Used as the main programming language for the entire project
* OpenCV – Used for capturing images from the webcam, drawing the region of interest (ROI), and preprocessing images
* TensorFlow & Keras – Used for building, training, and saving the deep learning model
* CNN (Convolutional Neural Network) – Used for image classification (main model in this project)
* NumPy – Used for handling image arrays and preprocessing during prediction
* Matplotlib – Used for visualizing training and validation accuracy



##  Dataset Creation using OpenCV
I created my own dataset using OpenCV instead of downloading one.

* Captured images using the webcam
* Defined a fixed green box (ROI) to ensure consistent hand positioning
* Cropped only the hand region
* Resized images to 224 × 224
* Stored images in separate folders for each digit (0–9)

This step helped in creating a clean and structured dataset for training.



##  Model Building using CNN

I used a Convolutional Neural Network (CNN) because it is well-suited for image classification tasks.

### Step-by-step what I did in CNN:

1. Convolution Layer (Conv2D)

   * Extracted important features from images like edges, shapes, and patterns

2. MaxPooling Layer

   * Reduced image size and kept only important features
   * Helped in reducing computation and overfitting

3. Multiple Conv + Pool Layers

   * Learned more complex patterns (like finger shapes and gesture structure)

4. Flatten Layer

   * Converted 2D feature maps into a 1D vector

5. Dense Layer (Fully Connected)

   * Learned relationships between extracted features

6. Dropout Layer

   * Prevented overfitting by randomly disabling neurons

7. Output Layer (Softmax)

   * Predicted probabilities for digits (0–9)
   * Selected the digit with highest probability



## Model Training

* Used image data generator with rescaling
* Split dataset into training and validation (80–20)
* Trained model for multiple epochs
* Plotted training and validation accuracy using Matplotlib


##  Real-Time Prediction using OpenCV

After training the model, I implemented real-time prediction:

* Captured live video from webcam
* Displayed a bounding box for hand placement
* Cropped and resized the hand region
* Normalized the image
* Passed it to the trained model
* Displayed predicted digit and confidence

This made the project interactive and closer to real-world applications.

