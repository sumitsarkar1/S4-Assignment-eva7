# S4-Assignment-eva7
Part 1 : Exccel sheet has been uploaded
Part 2 :
1. The CNN Pipeline : The CNN Pipeline consists of 3 CNN layers each of 16, 32 and 50 channels respectively. Each channel has a BatchNormalization and MaxPooling step to it. Kernel size selected is 3x3 andpadding is set to 1 to preserve the resolution of the channels at each CNN layer. However the resolution is reduced using MaxPooling after each CNN layer.
2. The Fully Connected layer : The output of the CNNN Pipeline is fed to a fully connected layer of 10 nodes followed by a Dropout step. 
3. Data Augmentation : Images in the training set are given random affine transforms of rotation and scaling. Random affine trasforms are followed by some brightness and contrast changes. Both these data augmentations help to make the network robust to affine and intensity changes in the images.
4. Droput step is only used for the fully connected layer and not on CNN layers because CNN layers with dropout was giving a regularisation effect on the network and the network was not able to achieve higher accuracy in 19 epochs.
5. Training has been done on GPU
6. Learning rate has been reduced a bit from the usual lr=0.01 to lr=0.006 to counter the random fluctuation in accuracy after 99%
7. As per the problem statement, the total number of parameters of the network is 19,848 (< 20k) and the number of epochs trained is 19 (< 20 epochs)
8. The final accuracy (at the end of 19th epoch ) is 99.30 % 

