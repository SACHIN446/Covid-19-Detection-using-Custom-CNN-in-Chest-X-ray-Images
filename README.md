# Covid-19 Detection in Chest X-Ray Images using Deep Neural Network
## 1. INTRODUCTION
This is a Deep Neural Network Model designed using CNN, MaxPooling, Dense, Flatten and other layers. It classifies the X-Ray images of lung parenchyma into three classes namely NiCT, pCT and nCT. pCT means Positive CT Scan images and it refers to image of Covid19 patient, nCT means Negative CT Scan images i.e Normal Person and NiCT means Non-informative CT Scan images i.e no decision can be made for this kind of image because of very less informative features present in image.

In Simple term NiCT, pCT and nCT represents three classes as non-informative sample, Positive case and negative case for covid19. The Model we build extract the features from X-Ray image and uses final layer as Dense with three Neuron to predict the target class out of three (NiCT, nCT, pCT) discussed above.

Over normal training with epoch value equals to 20 model reached at accuracy of 96.83% and when tested on Testing Data accuracy is 98.91% and loss of model is reduced to nearly 4% i.e from 1 to 4.28. Good choice of Activation Function, Loss Function, Optimizers affect the performance of the Neural Network to a great extent. Normally for multiclass classification sigmoid works best but more ever, it also depend on dataset. Using appropriate Loss Function helps to reduce the loss computed by Neural Network at faster rate and hence increases the accuracy in less Epoch value. Since the Accuracy of our Model is very Good i.e 96% and even on random training for just 20 epochs, the accuracy goes up between 97% to 99%, it means the parameter that we have selected are perfect for our Model. Anyone who is unable to decide the number of neuron to use in Model, they can take help from Hyper-Parameter Tuning technique.

All the results were obtained on 64 bit System with 8GB RAM, Core i5 7th Generation Intel Processor, Clock Speed of 2.5 - 2.71 GHz having Nvidia GeForce 920MX GPU.
## 2.ABOUT THE DATASET:
Dataset contains X-Ray image of Lung Parenchyma divided into three class NiCT, nCT, pCT. Figure 1.1 shows the number of samples, classes available in Dataset. It has total size of 4.0 GB.

![image](https://user-images.githubusercontent.com/46420929/132246405-75ee05d5-3e7c-45be-8526-170cf45ee1af.png)

Data were collected from 2 hospitals, Union Hospital (HUST-UH) and Liyuan Hospital (HUST-LH) which is describes in detail in the paper iCTCF: An integrative resource of chest computed tomography images and clinical features of patients with covid-19 pneumonia[3]. 

The authors of the above paper classified individual CT images into three types- 
(I) 5705 non-informative CT (NiCT) images where lung parenchyma was not captured for any judgment. 
(ii) 4001 positive CT (pCT) images where imaging features associated with COVID-19 pneumonia could be unambiguously discerned, and 
(iii) 9979 negative CT (nCT) images where imaging features in both lungs were irrelevant to COVID-19 pneumonia.

Some sample images are shown in below figure 2.1 with their labels.

![image](https://user-images.githubusercontent.com/46420929/132246550-8bf272f4-02ab-4cdd-a186-0fe1840ebd74.png)

## 3.Network Architecture (I/O Dimension)

Analyzing the Input and Output Dimension to each layer:

![image](https://user-images.githubusercontent.com/46420929/132246667-f36caaa4-8b9c-402d-b559-47154344a2ca.png)

## 4. OUTPUTS AND RESULT

Final Dense Layer with three Neuron gives the class to which the particular X-Ray image belongs, and using activation function as Softmax which give the probability distribution for all target class and the class with maximum probability will be considered as output.

Below figure shows the graph of epoch versus accuracy during training, the Training accuracy value start from approx. 0.4 and slightly converging toward value 1.0 i.e 100% accuracy.

![image](https://user-images.githubusercontent.com/46420929/132246757-c9eaa2ad-6ca4-433b-ab02-2a50fd75598a.png)

Below figure shows the decrease in Training and Validation loss value with increase of number of epochs. Loss value is approaching downward. With increased in epoch, both Training and Validation loss can be minimized to very lower extent.

![image](https://user-images.githubusercontent.com/46420929/132246841-419902e1-afa7-4ff0-ae59-cc99dab7c100.png)

Finally Training Accuracy, Validation Accuracy, Training loss and Validation loss are plotted together in Below figure.

![image](https://user-images.githubusercontent.com/46420929/132247021-620c7e56-eb2b-433f-b1e1-32d71e313664.png)

Confusion Matrix for Testing Dataset is shown here.

![image](https://user-images.githubusercontent.com/46420929/132247136-1cef2707-8ed7-4463-af7a-9d1aab8eae54.png)

## 5. CONCLUSION
Model’s maximum accuracy is about 96% during training, this accuracy can further be increased by increasing epoch value, Hyper-tuning of model, selecting the right learning rate and many more factor are there which decides the model performance. Loss is reduced to 0.6 for just 20 epochs and decreasing slowly, using the above techniques, loss value can be decreased to greater extent i.e equals to zero. 

Model performance over the testing dataset is also good, about 98% testing accuracy with 40% of loss. Confusion Matrix is also being shown above in figure 4.5 with corresponding Precision and Recall values for all the three classes, using this also we can calculate the accuracy for correct classification in each classes.
Various plots in Section 4 “Outputs and Results” show the behavior of Model over Training Data, Validation Data and Testing Data.

This model can find application in medical for detecting Covid-19 infected or non-infected lungs and after that we can judge whether the person have Covid-19 or not. Only the X-Ray image of lung parenchyma is required as input and model can give the output. 

For every training, accuracy changes and the maximum accuracy encountered during random training was about 99% so by changing the some layer architecture, model accuracy can easily cross the Accuracy value of 99%. Above results shows that model does not require any hyper parameter tuning but still we can go for if model accuracy decreases for higher epoch values and more dataset are added as input.





