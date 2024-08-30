<h1 align="center">BrainTumorNet: A Deep Learning Framework for Accurate Brain Tumor Detection </h1>
<p align = "center" style = "border-radius: 10px;"><img src="https://github.com/user-attachments/assets/72d4e560-7460-4414-b18d-c4ba406a4072" width = "700px" height="300px"></p>

## Summary 
- Developed **Convolutional Neural Networks (CNNs)** to analyze MRI images of the brain to detect the presence of tumors and minimize human error in diagnosis. 
- The project includes visualization of the model's performance using accuracy and loss plots, classification reports, and confusion matrices. 
- Final model performs with publication level results:
  - AUC = 0.9895
  - F1 = 0.9717
  - Recall = 0.98
  - Precision = 0.98
 
## Concolutional Neural Networks (CNNs) Model:
- The model is compiled with the categorical crossentropy loss function and the Adam optimizer, which are standard choices for classification tasks. 
- The architecture and layers used in this model help to automatically learn and extract relevant features from brain tumor images, making it suitable for detecting the presence of tumors with reduced human error.
  - **Model Initialization:** I began by initializing sequential model.
  - **Input Layer:** Then, the input layer is added with the specified input shape, which is (224, 224, 3). This shape represents 224x224 pixels with 3 color channels (RGB).
  - **First Convolutional Layer:** Next, Added a 2D convolutional layer with 32 filters of size 3x3 and ReLU activation function. Convolutional layers are used to detect local patterns.
  - **First Max Pooling Layer:** Added a max pooling layer with a pool size of 2x2 which reduces the spatial dimensions (height and width) of the input volume.
  - **Second Convolutional Layer:** Added another 2D convolutional layer with 32 filters of size 3x3, ReLU activation function, and He uniform kernel initializer. This layer also helps in detecting local patterns with a different initialization technique for weights.
  - **Second Max Pooling Layer:** Added a max pooling layer with a pool size of 2x2, similar to the first max pooling layer, to further reduce the spatial dimensions.
  - **Third Convolutional Layer:** Added a 2D convolutional layer with 64 filters of size 3x3, ReLU activation function, and He uniform kernel initializer. This layer captures more complex features.
  - **Third Max Pooling Layer:** Added a max pooling layer with a pool size of 2x2, further reducing the spatial dimensions.
  - **Flatten Layer:** Flattened the 2D matrix from the convolutional and pooling layers into a 1D vector, making it suitable for the fully connected (dense) layers.
  - **Dense Layer:** Added a fully connected layer with 64 neurons and ReLU activation function. Dense layers are used to perform high-level reasoning in the network.
  - **Dropout Layer:** Added a dropout layer with a 50% dropout rate to reduce overfitting by randomly setting half of the input units to 0 at each update during training time.
  - **Output Layer:** Added the output layer with 2 neurons (one for each class in binary classification) and softmax activation function. The softmax function outputs a probability distribution over the two classes.
  - Lastly, Compiled the model by specifying the loss function (categorical_crossentropy), optimizer (adam), and evaluation metric (accuracy).  

## Heatmap of the Confusion Matrix: 
visualized the performance of a machine learning model(CNNs) using a confusion matrix plotted as a heatmap. 
![Capture](https://github.com/user-attachments/assets/aa633b1a-d034-4086-8c47-6435350c832e)
As we can see in the above figure 98% of the time model predicts correct image. 123


