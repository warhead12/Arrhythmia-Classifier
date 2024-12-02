# Introduction
 The proposed work explores the effectiveness of hybrid deep learning models combining long short-term memory networks and convolutional neural networks for classifying electrocardiogram signals and 
 predicting heart diseases. The study utilizes a comprehensive dataset of ECG recordings and employs rigorous training and evaluation processes to assess the model’s performance.

# Dataset
The proposed work utilizes a 12-lead ECG dataset, which provides 12 different heart views using 10 electrodes attached to the body. This allows for a more comprehensive and accurate arrhythmia diagnosis by covering more than 10,000 patients, created under the auspices of Chapman University and Shaoxing People’s Hospital.

Dataset Link :- https://www.nature.com/articles/s41597-022-01403-5

# Methodology
For binary and multi-class arrhythmia detection, we have applied a sequential neural network which consists of :-
 1.  Two initial CNN layers followed by two LSTM layers
 2.  Two additional CNN layers are introduced, each followed by a MaxPooling layer
 3.  A flattening layer is then added to convert the learned features to a vector format
 4.  Two fully connected layers with their activation function

For performing the federated learning approach, we have applied the following method to both models :-
 1.   Generating client devices through data shards
 2.   Transfer fo global model’s weights to all local models in each communication round to serve as initial weights
 3.   Aggregation of updates received from all local models at global model
 4.   Testing the global model using the updated weights in each round

 # Results
  For the federated learning model, the multiclass classification model achieves an impressive global model accuracy of 85.14%, accompanied by a global loss of 1.755. The binary classification model also 
  performs exceptionally well, achieving an accuracy of 95.7%, with a global loss of 0.425. The training was done for 20 communication rounds.
  Notably, the binary arrhythmia detection achieved a remarkable accuracy of 94.4%, outperforming the multiclass detection with an accuracy of 86.17%.
