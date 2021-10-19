# S4-Assignment-eva7
Part 1 : 
Exccel sheet has been uploaded


Part 2 :
1. The CNN Pipeline : The CNN Pipeline consists of 3 CNN layers each of 16, 32 and 50 channels respectively. Each channel has a BatchNormalization and MaxPooling step to it. Kernel size selected is 3x3 and padding is set to 1 to preserve the resolution of the channels at each CNN layer. However the resolution is reduced using MaxPooling after each CNN layer.
2. The Fully Connected layer : The output of the CNN Pipeline is fed to a fully connected layer of 10 nodes. 
3. Data Augmentation : Images in the training set are given random affine transforms of rotation and scaling. Random affine trasforms are followed by some brightness and contrast changes. Both these data augmentations help to make the network robust to affine and intensity changes in the images.
4. Droput step is used at the end of all the CNN layers. Dropout values of 0.25 , 0.2, 0.1, 0.05, 0.01 has been experimented. 0.01 value helps in achieving test accuracies upto 99.30 % and more
5. Training has been done on GPU
6. Learning rate has been reduced a bit from the usual lr=0.01 to lr=0.008 to counter the stochastic fluctuations in accuracy after 99%. 
7. Momentum = 0.8
8. Batch size of 32, 64, 128, 256 were experimented. Out of all batch size of 64 produced the optimum result i.e. achieving above 99% accuracy in less than 20 epochs
9. As per the problem statement, the total number of parameters of the network is 19,848 (< 20k) and the number of epochs trained is 19 (< 20 epochs)
10. The average test accuracy for the last 4 epochs (of the all 19 epochs ) is 99.30 %

