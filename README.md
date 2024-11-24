# Melanoma-Detection-Assignment

# Project Name
Melanoma Detection Assignment


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- Provide general information about your project here.
build a multiclass classification model using a custom convolutional neural network in TensorFlow. 

- What is the background of your project?

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. 


- What is the business probem that your project is trying to solve?
A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


- What is the dataset that is being used?

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.


The data set contains the following diseases:

Actinic keratosis
Basal cell carcinoma
Dermatofibroma
Melanoma
Nevus
Pigmented benign keratosis
Seborrheic keratosis
Squamous cell carcinoma
Vascular lesion



## Experiments & Conclusions



**- Experiment 1 :Adding 2 Conv2D layer, Flattening Layer,1 FC layer and adding dropput (0.5) after the FC layer**

**Conclusion 1**


1)Overfitting

Validation accuracy drops and validation loss increases after Epoch 19, despite improving training metrics. The model is becoming too specialized to the training data, losing generalization ability.

2)Early Improvements

Validation accuracy improves significantly up to Epoch 10 (55.13%), showing that the model was effectively learning patterns initially. Sudden Drops in Validation Performance (Epochs 17-18):

3)Validation Loss Spikes

Large losses (2.1990 and 2.1205) indicate the model struggled during these epochs.

**-Experiment 2 : Running the second experiment to add drop out of 0.25 after each Con2D layer**

**-Conclusion 2 from the analysis**

Poor Generalization:

Validation accuracy lags significantly behind training accuracy. Validation loss does not improve substantially, and there's no clear indication of the model adapting to the validation data.

Slow Learning Progress:

Both training and validation accuracies improve very slowly.

Overfitting:

The gap between training and validation performance suggests overfitting to the training data, especially by the later epochs.

Possible Dataset Issues:

Validation accuracy is unusually low.

**Experiment 3 : Remove the dropouts after the convolutional layers (but retain them in the FC layer). Also, use batch normalization after every convolutional layer.**


**Conclusion 3**

Initial Struggles (Epochs 1-6):

Training loss is very high (9.9553) in the first epoch, indicating either initialization issues or a challenging dataset. Validation accuracy fluctuates and remains low during this period.

Midpoint Stabilization (Epochs 7-16):

Training and validation metrics improve steadily. Validation accuracy peaks at 68.97% (Epoch 16), suggesting the model performs well on the validation set during this period.

Instability in Late Epochs:

Large validation loss spikes in Epochs 15 (5.8189) and 18 (2.4233), followed by recovery in Epoch 19 (0.8544). Indicates overfitting or sensitivity to specific batches.

Overfitting Signs:

By the end, training accuracy is higher (70.58%) compared to validation accuracy (56.47%). Validation loss begins to increase after reaching a low point in Epoch 19.


**Experiment 4 : Data Augmentation Strategy**

**Conclusion 4**

Training Accuracy:

Training accuracy increases slightly (to ~52.37%), but it's still low. Indicates the model is learning, but its capacity may not be sufficient for the dataset's complexity.

Validation Performance:

High validation loss suggests overfitting or insufficient generalization. Low validation accuracy (around 30%) shows the model struggles with unseen data.

Signs of Overfitting:

Training loss decreases steadily, but validation loss remains erratic. Validation accuracy does not consistently improve, suggesting overfitting or data imbalance.


**Experiment 5 : Class Imbalance and Remediation**

**Conclusion 5**

Training Accuracy:

Starts very low at ~25% (Epoch 1) and steadily improves to ~57.92% (Epoch 50). This indicates that the model is learning to recognize patterns in the training dataset but still has a long way to achieve good performance.

Validation Accuracy:

Begins low at ~9.72% (Epoch 1) but shows some improvement, ending at ~52.23% (Epoch 50). There are fluctuations in the middle epochs (e.g., dips around Epochs 8 and 44–48), which could indicate overfitting or instability.

Loss Behavior:

The training loss steadily decreases, showing that the model is minimizing the error on the training data. The validation loss, however, fluctuates and does not always follow the training loss pattern. For example: Epoch 6: Validation loss is 1.6271 (good). Epoch 30: Validation loss increases to 3.8588 (poor).

Class Imbalance

The results show gradual improvement in training accuracy and a decent final validation accuracy (52.23%), indicating that class rebalancing had a positive impact. However: The overall accuracy (57.92%) suggests that the model is still struggling to differentiate between classes effectively.




## Technologies Used
-Python
-Google Colab





## Contact
Created by [@Sandy494] - feel free to contact me!

