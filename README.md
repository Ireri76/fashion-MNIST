README
Overview
This study utilizes the Fashion MNIST dataset, accessible from Fashion MNIST dataset. This dataset comprises 10 distinct fashion labels: T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, and Ankle boots. The project includes two major assignments:
1.	Convolutional Neural Network (CNN):
o	Develop a CNN with six layers using Keras in both Python and R to classify the Fashion MNIST dataset.
2.	Prediction:
o	Make predictions for at least two images from the dataset.


CNN Implementation
The CNN involved several key procedures:
1.	Loading and preprocessing data
2.	Building the model using Keras
3.	Training the model
4.	Saving the model to Google Drive
5.	Performing predictions and evaluating performance on the test dataset
The code for this project is adapted from the blog post, Classifying Fashion with a Keras CNN (Achieving 94% Accuracy) — Part 1 by Manish Bhobé on Medium. Modifications and improvements were made for this project, including:
•	Creating TensorFlow datasets for training, validation, and testing while incorporating batch size.
•	Adjusting the number of rows and columns for displaying sample predictions.
•	Adding a dropout function to reduce overfitting.
•	Enabling mixed precision and early stopping callbacks to automatically terminate training when performance plateaus.
•	Mounting Google Drive for model saving.
•	Including color coding to distinguish between correct and incorrect predictions.
•	Printing the number of batches processed.
•	Calling the prediction function from Google Drive.


Environment
The project was executed on Google Colab due to the complexity of the model and the extensive training time required. The lower tiers of the Anaconda platform could not accommodate the high CPU usage. Google Colab provided a faster and more convenient environment for saving all code and output from the analysis.
For instance, I encountered an issue when saving my final model on Google Drive after 12 epochs. This was resolved by executing only the saving code instead of retraining the entire model.
Dataset
The sample sizes for the project were as follows:
•	Training dataset: 60,000 images
•	Validation dataset: 8,000 images
•	Test dataset: 2,000 images

Results (Model with Early Stopping Callbacks)
The training accuracy over 12 epochs ranged from 78% to 97%. The cross-validation accuracy ranged from 88% to 93%, while the test accuracy varied between 78% and 93%. The 5% difference between training and cross-validation accuracy indicates potential overfitting. The divergence of the loss curves was observed between 2 to 4 epochs for both training and validation loss, as well as for training and validation accuracy.
The model was able to predict 78% of the images in the test dataset, which may be attributed to overfitting. If the training process had continued for the full 25 epochs without early stopping, the prediction accuracy could have improved. Future work may involve testing the model with techniques designed to address overfitting.

Results (Model with all the 25 epochs)
The training accuracy over 25 epochs ranged from 78% to 99%. The cross-validation accuracy ranged from 88% to 93%, while the test accuracy varied between 92% during training and 93% on test predictions. The 7% difference between training and cross-validation accuracy suggests potential overfitting. However, the model's accuracy improved from 78% at 12 epochs to 93% by 25 epochs. Thus, the model was able to correctly predict 93% of the images. Future work may involve testing the model with techniques aimed at addressing overfitting.


