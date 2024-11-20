# Neural-Network-for-Object-Detection-and-Image-Classification-in-Autonomous-Driving-System


The title of my project is "CNN for Object Detection and Image Classification in Autonomous Driving Systems."

A Convolutional Neural Network (CNN) is a type of deep learning model that processes real-time visual data from vehicle-mounted cameras. It identifies objects such as pedestrians, vehicles, road signs, and lane markers. This helps autonomous vehicles make decisions, navigate safely, and respond appropriately to their surroundings.

The system mainly operates in two phases:

Object Detection: Achieved using cameras mounted on vehicles and sensors like LiDAR, which measures distances between objects and the vehicle.
Image Classification: After detecting objects, the system classifies them—for instance, identifying whether an object is a pedestrian, an animal, or another vehicle.
Front-End of the CNN System
The front-end of the system involves three key steps:

Data Acquisition

Data is collected using cameras mounted on vehicles.
Sensors like LiDAR measure the distance between objects and the vehicle.
Data Preprocessing

Raw images are prepared for CNN processing through the following:
Resizing images to a uniform size.
Normalizing pixel values for consistent input.
Data Augmentation, which includes transformations like flipping, rotating, or adjusting images to improve the system's robustness.
Feature Extraction with CNN Layers

The initial layers of the CNN extract basic features such as edges, textures, and shapes.
Deeper layers identify more abstract patterns and relationships.
We used OpenCV, an open-source computer vision library, for these tasks. OpenCV provides tools for real-time image and video processing and is essential for preprocessing data before feeding it into the CNN.

Back-End of the CNN System
Image Classification and Recognition

After classifying images, the system uses Bounding Box Regression to accurately locate objects in the frame.
For this, we employed TensorFlow, a powerful, end-to-end machine learning platform developed by Google. TensorFlow is widely used for training and deploying neural networks effectively.
Real-Time Decision-Making

Initially, we implemented the SSD (Single Shot MultiBox Detector) framework. While SSD balances speed and accuracy, it struggled to make accurate decisions at high vehicle speeds.
To address this, we switched to YOLO (You Only Look Once). YOLO's architecture uses bounding box regression for real-time object detection, making it more suitable for high-speed scenarios in autonomous driving systems.
Training the Neural Network
Training a neural network involves teaching it to learn patterns from data so it can make accurate predictions. It starts with preparing the data, where images or other inputs are resized, normalized, and sometimes augmented with changes like flipping or rotating to improve the model's robustness. The data is then passed through the network in a process called forward propagation, where each layer processes the input, applies mathematical operations, and generates an output. The network's predictions are compared to the correct answers using a loss function, which measures how far off the predictions are.

To improve, the network uses backpropagation, a method to calculate how much each part of the network contributed to the error. This information is used by an optimizer (like SGD or Adam) to adjust the network’s weights and biases, gradually reducing the error. This process is repeated many times, over several rounds called epochs, until the network becomes good at recognizing patterns in the data. During training, the model is tested on separate data to ensure it performs well and doesn’t just memorize the training data. Once trained, the network can make predictions on new, unseen data.

Development Tools
For developing this project, we primarily used:

Programming Language: Python, due to its extensive support for libraries like TensorFlow, OpenCV, and PyTorch.
Frameworks:
TensorFlow: Used for training and deploying neural networks.
YOLO: Utilized for real-time object detection.
Conclusion
This was an overview of my final year project, "CNN for Object Detection and Image Classification in Autonomous Driving Systems." This project provided me with hands-on experience in deep learning, computer vision, and real-time decision-making systems.
