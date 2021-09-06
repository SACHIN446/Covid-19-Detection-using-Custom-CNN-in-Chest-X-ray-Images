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




