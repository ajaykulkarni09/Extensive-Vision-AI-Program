# Architectural Basics 

## Problem Statement:

Modified the code given in [MNIST Base Code](https://colab.research.google.com/drive/1uJZvJdi5VprOQHROtJIHy0mnY2afjNlx) to achieve 99.4% validation accuracy with 20k Parameters and in less than 20 Epochs.

## Model:

- Total trainable parameters: 9,320.
- Used Batch normalization, GAP layer & Drop out.
- Added a FC layer after GAP.
- Used Augmentation like image RandomRotation & RandomAffine.
- The model was trained with a learning rate of 0.01 amd momentum of 0.9.
- Network was trained for 12 epochs with batch size of 64 & StepLR Learning Rate Scheduler used.

![best_network](https://user-images.githubusercontent.com/48423396/137821052-27e114cb-e65c-43d1-b7a1-ea0dddd54ef1.png)


## Logs:

Epoch 1 : 
loss=0.3429986536502838 batch_id=937: 100%|██████████| 938/938 [00:41<00:00, 22.74it/s]Train set: Average loss: 0.603 Accuracy: 80.05

Test set: Average loss: 0.071 Accuracy: 97.78

Epoch 2 : 
loss=0.03419129550457001 batch_id=937: 100%|██████████| 938/938 [00:41<00:00, 22.55it/s]Train set: Average loss: 0.125 Accuracy: 96.44333333333333

Test set: Average loss: 0.059 Accuracy: 98.14

Epoch 3 : 
loss=0.16522426903247833 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.20it/s]Train set: Average loss: 0.095 Accuracy: 97.17666666666666

Test set: Average loss: 0.050 Accuracy: 98.48

Epoch 4 : 
loss=0.0651002749800682 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.02it/s]Train set: Average loss: 0.083 Accuracy: 97.5

Test set: Average loss: 0.035 Accuracy: 98.88

Epoch 5 : 
loss=0.03457719087600708 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.18it/s]Train set: Average loss: 0.075 Accuracy: 97.78833333333333

Test set: Average loss: 0.031 Accuracy: 98.98

Epoch 6 : 
loss=0.0825406014919281 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.13it/s]Train set: Average loss: 0.067 Accuracy: 97.945

Test set: Average loss: 0.028 Accuracy: 99.07

Epoch 7 : 
loss=0.03722963109612465 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.29it/s]Train set: Average loss: 0.064 Accuracy: 98.055

Test set: Average loss: 0.029 Accuracy: 99.06

Epoch 8 : 
loss=0.03204820677638054 batch_id=937: 100%|██████████| 938/938 [00:41<00:00, 22.38it/s]Train set: Average loss: 0.060 Accuracy: 98.14833333333333

Test set: Average loss: 0.031 Accuracy: 99.03

Epoch 9 : 
loss=0.029772572219371796 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.19it/s]Train set: Average loss: 0.048 Accuracy: 98.53833333333333

Test set: Average loss: 0.020 Accuracy: 99.38

Epoch 10 : 
loss=0.009376359172165394 batch_id=937: 100%|██████████| 938/938 [00:41<00:00, 22.37it/s]Train set: Average loss: 0.044 Accuracy: 98.64833333333333

Test set: Average loss: 0.019 Accuracy: 99.43

Epoch 11 : 
loss=0.058516353368759155 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 22.24it/s]Train set: Average loss: 0.044 Accuracy: 98.57166666666667

Test set: Average loss: 0.020 Accuracy: 99.4

Epoch 12 : 
loss=0.008633488789200783 batch_id=937: 100%|██████████| 938/938 [00:42<00:00, 21.96it/s]Train set: Average loss: 0.045 Accuracy: 98.63333333333334

Test set: Average loss: 0.019 Accuracy: 99.41

## Loss Function:

![image](https://user-images.githubusercontent.com/48423396/137821093-300e5a9c-3365-45bc-a496-17650737f87b.png)


## Results:

MNIST images classification with Average loss of 0.019 & Accuracy of 99.41 on Test data.
