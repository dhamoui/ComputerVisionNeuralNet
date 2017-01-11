# ComputerVisionNeuralNet
A Computer Vision Neural Net for the Kaggle Competition: The Nature Conservacies Fisheries Monitoring

The data for this competition can be found here: https://www.kaggle.com/c/the-nature-conservancy-fisheries-monitoring/data

** Requires latest version of keras for Inception_V3 **

1 - Use ```split_train_val.py``` to split the labed data into training and validation. 

2 - Use ```train.py``` to train the neural network. The best model and its weights will be saved as "weights.h5".

3 - Use ```predict.py``` to predict labels for testing images and generating the submission file "submit.csv".

4 - In order to improve our ranking, we use data augmentation for testing images. The intuition behind is similar to multi-crops,
which makes use of voting ideas. ```predict_average_augmentation.py``` implements.

5 - Note that there is still plenty of room for improvement. For example, we could split data into defferent training and valition data by cross-validation, e.g. k-fold. Then we train k models based on these splitted data. We average the predictions output by the k models as the final submission. 

6 - To improve ranking further, object detection is the next step.

** To use ```flow_from_directory()```, you must create a folder named **test_stg1** and put the original test_stg1 inside it.
