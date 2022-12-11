# Deep-Learning-Classification---Application-Electric-Motor-
An application of convolutional neural networks to classify images into different categories. A CNN model is built, trained, validated and tested.

A convolutional neural network is built and trained which can be used for inspection of electric motors.
First of all, some basic libraries are imported.There are different images belonging to different categories.
One image from complete category is manually printed. The shape of the image is 1024*1024*3.

A function has been written to get all the images and their respective labels from the stored folder.
All the images are loaded as features and their categories as labels. The total number of images is 117.

Some images from the tree categories are printed in grid.
Complete category has all the screws as well as cover intact.Though some screws are not fully screwed, they are still included in the complete category.
In the missing cover category the cover of coil is missing and in missing screws category one or more screws are missing.

Total number of images for each category is printed.61 in incomplete category, 42 in missing screw category.And only 14 in missing cover category.
the whole data is split in the training and testing sets in ratio of 70 to 30 And then the labels are encoded using one hot encoder.

ACNN model is created using Keras.In this, three convolution layers and two dense layers have been added. In the summary, the shape of the output of each layer can be seen.The model is trained on total 9331 parameters.

The model is compiled with Adam Optimizer cross entropy loss and accuracy metrics. the model is trained using training data over 25 epochs with batch size 32 in each epoch.

It can be observed that the accuracy of model over training data is increasing. Also over the validation data accuracy is fluctuating but gradually increasing.
Finally, at the end, training accuracy has reached 100% with validation accuracy of around 78%. 

A function has been written to evaluate the model using confusion matrix and classification report. performance of the model on the testing data can be seen.
Accuracy corresponding to F1-score is around 70%. This is a good accuracy.

Next, accuracy is improved using augmentation.

