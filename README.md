# TinyML-Activity-Recognition

CNN Model Description: Predicting user activity based on XYZ accelerometer readings (trained using PyTorch)
-	Training data:
o	Dataset of 104,000 accelerometer XYZ readings (sampling rate of 200) from 33 different participants
o	Activity labels: Sitting, Standing, Walking, Upstairs, Downstairs, Running 
o	Post processing features (9): Xavg, Yavg, Zavg, Xabsdiff, Yabsdiff, Zabsdiff, Xstanddev, Ystanddev, Zstanddev, Resultant Vector 
o	Z-score normalization applied to dataset
o	Training and testing data split into 80% and 20% respectively 
-	Model Architecture
o	3 convolutional layers 
o	2 max pooling layers
o	Dropout regularization layer (p = 0.5)
-	Model hyperparameters 
o	100 epochs 
o	Learning rate = 0.001
o	Weight decay = 0.0001
o	Adam optimizer 
-	Training results over 100 epochs 
o	96.5% training and 94.6% validation accuracy 
o	0.1079 training and  0.2660 validation loss
-	10-fold cross validation (K folds):
o	Average Validation Accuracy: 91.65%
o	Standard Deviation of Validation Accuracy: 1.53%
o	Training Accuracy: 93.00%
o	No significant overfitting detected.
