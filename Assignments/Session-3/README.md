# Problem Statement:

## Write a Neural Network that can:
Take 2 inputs:

- An image from the MNIST dataset (say 5), and
- A random number between 0 and 9, (say 7)

and gives two outputs:
- The "number" that was represented by the MNIST image (predict 5), and
- The "sum" of this number with the random number that was input to the network (predict 5 + 7 = 13, accuracy is not really important for the sum)

![image](https://user-images.githubusercontent.com/48423396/137637066-e5a4294f-ab4a-4803-8266-d604c0660b0d.png)

Network can be written with fully connected layers and convolution layers.

## Data representation:

The data is represented into 4 parts:
- An image from MNIST dataset is used as one of the input to the model. It contains 70,000 images of handwritten digits: 60,000 for training and 10,000 for testing.
- The label of the image.
- A random number.
- The Sum. 

Custom dataset returns the same:
```python
return image, label, rand_num_ohe, sum
```

## Data Generation:

Custom dataset is generated with help of MNIST dataset using '\_\_getitem\_\_' method to get:
- The image (28x28).
- label.
- A random number (0-9) which is represented by one-hot encoding.
- The Sum (label+random number). 

## Model

The **NeuralNetwork** model developed involves both Convolution and Fully Connected layers. The Convolution part classifies the MNIST image i.e. output1, that also produce 1x10 vector which is concatenated with the one-hot encoded random number (1x10) to create a 1x20 vector which is then passed to a Fully Connected layer and finaly a 1x19 vector which is the prediction of sum (ranges between 0 to 18) i.e. output2.

Total trainable parameters: 6384925

## Device (GPU)
![image](https://user-images.githubusercontent.com/48423396/137644564-66f86caf-8cfd-4885-aeec-0e76f55ca973.png)


## Model Evaluation:
The accuracy of the model on Test data i.e. the percentage of the MNIST images classified correctly and the actual Sum of the MNIST number and the Randomn number generated.

## Loss Function:
Negative log likelihood loss (nll_loss). Since it is a multi class classification problem.

## Logs

Epoch 1 : 
loss=2.4098801612854004 batch_id=467: 100%|██████████| 468/468 [00:39<00:00, 11.75it/s]
Test set: Average loss: 2.394 MNist Accuracy: 56.34 Sum_Accuracy: 9.94

Epoch 2 : 
loss=1.2987701892852783 batch_id=467: 100%|██████████| 468/468 [00:39<00:00, 11.82it/s]
Test set: Average loss: 1.296 MNist Accuracy: 94.29 Sum_Accuracy: 14.32

Epoch 3 : 
loss=1.185538411140442 batch_id=467: 100%|██████████| 468/468 [00:39<00:00, 11.78it/s]
Test set: Average loss: 1.207 MNist Accuracy: 96.57 Sum_Accuracy: 18.48

.

.

.

Epoch 18 : 
loss=0.11908458918333054 batch_id=467: 100%|██████████| 468/468 [00:39<00:00, 11.82it/s]
Test set: Average loss: 0.142 MNist Accuracy: 98.99 Sum_Accuracy: 98.72

Epoch 19 : 
loss=0.11350075155496597 batch_id=467: 100%|██████████| 468/468 [00:39<00:00, 11.83it/s]
Test set: Average loss: 0.129 MNist Accuracy: 98.9 Sum_Accuracy: 98.54

Epoch 20 : 
loss=0.1045355424284935 batch_id=467: 100%|██████████| 468/468 [00:39<00:00, 11.79it/s]
Test set: Average loss: 0.110 MNist Accuracy: 98.96 Sum_Accuracy: 98.83

![image](https://user-images.githubusercontent.com/48423396/137644339-7fbed1e3-6251-452e-8fb6-6d0ffdf8c36b.png)

## Results
MNIST images classification accuracy: 98.96, Sum accuracy: 98.83 on Test data.

## Inference
![image](https://user-images.githubusercontent.com/48423396/137644235-c523ba0b-c451-4818-a494-21a72b676ba6.png)

