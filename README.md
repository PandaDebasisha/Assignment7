# Assignment_7
## Best Model : Model_4 
**Target:**
Stable model test accuracy to be > 99.4% over >7  Epochs.
Result Retained at Last Epoch also.

**Results:**
1. Parameters: **7774**
2. Best Train Accuracy: **99.41%**
3. Best Test Accuracy: **99.44%**

**Analysis:**
1. Model Architecture is tuned with less Filter size to reduce  not only total Parameter also we can manage 28*28 image with less filters
2. Learning Rate is Tuned with STepLR to acheive better consistent accuracy
3. Augmentation is used like Color Jitter Random Rotaion for **+/-5%** and Normalization
4. Best part of Model 1 is : Least gap and Costinency is observed between train and test accuracy 
5. Loss Covergence is Quite good

## Model_1 Details

**Target:**

Stable model test accuracy to be > 99.4% over multiple epochs. 

**Results:**
1. Parameters: **8246**
2. Best Train Accuracy: **99.42%**
3. Best Test Accuracy: **99.38%**

**Analysis:**
1. Model Architecture is tuned with less Filter size to reduce (but could not be <**8K**>) not only total Parameter also we can manage 28*28 image with less filters
2. Learning Rate is Tuned with STepLR to acheive better consistent accuracy
3. Augmentation is used like Color Jitter Random Rotaion for **+/-7%** and Normalization
4. Best part of Model 1 is : Least gap and Costinency is observed between train and test accuracy 

**Model-1 Summary**
```
Requirement already satisfied: torchsummary in c:\users\91702\anaconda3\lib\site-packages (1.5.1)
cuda
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 10, 26, 26]              90
              ReLU-2           [-1, 10, 26, 26]               0
       BatchNorm2d-3           [-1, 10, 26, 26]              20
           Dropout-4           [-1, 10, 26, 26]               0
            Conv2d-5           [-1, 12, 24, 24]           1,080
              ReLU-6           [-1, 12, 24, 24]               0
       BatchNorm2d-7           [-1, 12, 24, 24]              24
           Dropout-8           [-1, 12, 24, 24]               0
            Conv2d-9           [-1, 10, 24, 24]             120
        MaxPool2d-10           [-1, 10, 12, 12]               0
           Conv2d-11           [-1, 10, 10, 10]             900
             ReLU-12           [-1, 10, 10, 10]               0
      BatchNorm2d-13           [-1, 10, 10, 10]              20
          Dropout-14           [-1, 10, 10, 10]               0
           Conv2d-15             [-1, 16, 8, 8]           1,440
             ReLU-16             [-1, 16, 8, 8]               0
      BatchNorm2d-17             [-1, 16, 8, 8]              32
          Dropout-18             [-1, 16, 8, 8]               0
           Conv2d-19             [-1, 16, 6, 6]           2,304
             ReLU-20             [-1, 16, 6, 6]               0
      BatchNorm2d-21             [-1, 16, 6, 6]              32
          Dropout-22             [-1, 16, 6, 6]               0
           Conv2d-23             [-1, 14, 6, 6]           2,016
             ReLU-24             [-1, 14, 6, 6]               0
      BatchNorm2d-25             [-1, 14, 6, 6]              28
          Dropout-26             [-1, 14, 6, 6]               0
        AvgPool2d-27             [-1, 14, 1, 1]               0
           Conv2d-28             [-1, 10, 1, 1]             140
================================================================
Total params: 8,246
Trainable params: 8,246
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.57
Params size (MB): 0.03
Estimated Total Size (MB): 0.60
------------------------------------------------------------------------------------
```
## Model-2 Details

**Target:**

Model test accuracy to be > 99.4% with consistent over  multiple epochs. 

**Results:**
1. Parameters: **7934**
2. Best Train Accuracy: **98.96%**
3. Best Test Accuracy: **99.41%**

**Analysis:**
1. Model Architecture is tuned with less Filter size to reduice not only total Parameter also we can manage 28*28 image with less filters
2. Learning Rate is Tuned to acheive better consistent accuracy
3. Middle man Augmentation is sufficient like Color Jitter and Random Rotaion for **+/-5%** and Normalization

**Model_2 Summary**
```
Requirement already satisfied: torchsummary in c:\users\91702\anaconda3\lib\site-packages (1.5.1)
cuda
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 10, 26, 26]              90
              ReLU-2           [-1, 10, 26, 26]               0
       BatchNorm2d-3           [-1, 10, 26, 26]              20
           Dropout-4           [-1, 10, 26, 26]               0
            Conv2d-5           [-1, 12, 24, 24]           1,080
              ReLU-6           [-1, 12, 24, 24]               0
       BatchNorm2d-7           [-1, 12, 24, 24]              24
           Dropout-8           [-1, 12, 24, 24]               0
            Conv2d-9           [-1, 10, 24, 24]             120
        MaxPool2d-10           [-1, 10, 12, 12]               0
           Conv2d-11           [-1, 10, 10, 10]             900
             ReLU-12           [-1, 10, 10, 10]               0
      BatchNorm2d-13           [-1, 10, 10, 10]              20
          Dropout-14           [-1, 10, 10, 10]               0
           Conv2d-15             [-1, 16, 8, 8]           1,440
             ReLU-16             [-1, 16, 8, 8]               0
      BatchNorm2d-17             [-1, 16, 8, 8]              32
          Dropout-18             [-1, 16, 8, 8]               0
           Conv2d-19             [-1, 16, 6, 6]           2,304
             ReLU-20             [-1, 16, 6, 6]               0
      BatchNorm2d-21             [-1, 16, 6, 6]              32
          Dropout-22             [-1, 16, 6, 6]               0
           Conv2d-23             [-1, 12, 6, 6]           1,728
             ReLU-24             [-1, 12, 6, 6]               0
      BatchNorm2d-25             [-1, 12, 6, 6]              24
          Dropout-26             [-1, 12, 6, 6]               0
        AvgPool2d-27             [-1, 12, 1, 1]               0
           Conv2d-28             [-1, 10, 1, 1]             120
================================================================
Total params: 7,934
Trainable params: 7,934
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.56
Params size (MB): 0.03
Estimated Total Size (MB): 0.60```

------------------------------------------------------------------------------------
```
## Model_3 Details

**Target:**

Stable model test accuracy to be > 99.4% over multiple epochs. 

**Results:**
1. Parameters: **7934**
2. Best Train Accuracy: **98.75%**
3. Best Test Accuracy: **99.48%**

**Analysis:**
1. Model Architecture is tuned with less Filter size to reduice not only total Parameter also we can manage 28*28 image with less filters
2. Learning Rate is Tuned to acheive better consistent accuracy
3. Poor man Augmentation is sufficient Random Rotaion for **+/-7%** and Normalization
4. Best part MultiStep LR is used which can be configured which step we want to reduce LR
5. >**99.4%** observed over 4 epochs
   
## Model_3 Summary
```
Requirement already satisfied: torchsummary in c:\users\91702\anaconda3\lib\site-packages (1.5.1)
cuda
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 10, 26, 26]              90
              ReLU-2           [-1, 10, 26, 26]               0
       BatchNorm2d-3           [-1, 10, 26, 26]              20
           Dropout-4           [-1, 10, 26, 26]               0
            Conv2d-5           [-1, 12, 24, 24]           1,080
              ReLU-6           [-1, 12, 24, 24]               0
       BatchNorm2d-7           [-1, 12, 24, 24]              24
           Dropout-8           [-1, 12, 24, 24]               0
            Conv2d-9           [-1, 10, 24, 24]             120
        MaxPool2d-10           [-1, 10, 12, 12]               0
           Conv2d-11           [-1, 10, 10, 10]             900
             ReLU-12           [-1, 10, 10, 10]               0
      BatchNorm2d-13           [-1, 10, 10, 10]              20
          Dropout-14           [-1, 10, 10, 10]               0
           Conv2d-15             [-1, 16, 8, 8]           1,440
             ReLU-16             [-1, 16, 8, 8]               0
      BatchNorm2d-17             [-1, 16, 8, 8]              32
          Dropout-18             [-1, 16, 8, 8]               0
           Conv2d-19             [-1, 16, 6, 6]           2,304
             ReLU-20             [-1, 16, 6, 6]               0
      BatchNorm2d-21             [-1, 16, 6, 6]              32
          Dropout-22             [-1, 16, 6, 6]               0
           Conv2d-23             [-1, 12, 6, 6]           1,728
             ReLU-24             [-1, 12, 6, 6]               0
      BatchNorm2d-25             [-1, 12, 6, 6]              24
          Dropout-26             [-1, 12, 6, 6]               0
        AvgPool2d-27             [-1, 12, 1, 1]               0
           Conv2d-28             [-1, 10, 1, 1]             120
================================================================
Total params: 7,934
Trainable params: 7,934
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.56
Params size (MB): 0.03
Estimated Total Size (MB): 0.60
----------------------------------------------------------------
```
## Model_4 Details

**Target:**

Stable model test accuracy to be > 99.4% over >7  Epochs.
Result Retained at Last Epoch also.

**Results:**
1. Parameters: **7774**
2. Best Train Accuracy: **99.41%**
3. Best Test Accuracy: **99.44%**

**Analysis:**
1. Model Architecture is tuned with less Filter size to reduce  not only total Parameter also we can manage 28*28 image with less filters
2. Learning Rate is Tuned with STepLR to acheive better consistent accuracy
3. Augmentation is used like Color Jitter Random Rotaion for **+/-5%** and Normalization
4. Best part of Model 1 is : Least gap and Costinency is observed between train and test accuracy 
5. Loss Covergence is Quite good
   
## Model_4 Summary
```
Requirement already satisfied: torchsummary in c:\users\91702\anaconda3\lib\site-packages (1.5.1)
cuda
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 10, 26, 26]              90
              ReLU-2           [-1, 10, 26, 26]               0
       BatchNorm2d-3           [-1, 10, 26, 26]              20
           Dropout-4           [-1, 10, 26, 26]               0
            Conv2d-5           [-1, 12, 24, 24]           1,080
              ReLU-6           [-1, 12, 24, 24]               0
       BatchNorm2d-7           [-1, 12, 24, 24]              24
           Dropout-8           [-1, 12, 24, 24]               0
            Conv2d-9           [-1, 10, 24, 24]             120
        MaxPool2d-10           [-1, 10, 12, 12]               0
           Conv2d-11           [-1, 10, 10, 10]             900
             ReLU-12           [-1, 10, 10, 10]               0
      BatchNorm2d-13           [-1, 10, 10, 10]              20
          Dropout-14           [-1, 10, 10, 10]               0
           Conv2d-15             [-1, 14, 8, 8]           1,260
             ReLU-16             [-1, 14, 8, 8]               0
      BatchNorm2d-17             [-1, 14, 8, 8]              28
          Dropout-18             [-1, 14, 8, 8]               0
           Conv2d-19             [-1, 16, 6, 6]           2,016
             ReLU-20             [-1, 16, 6, 6]               0
      BatchNorm2d-21             [-1, 16, 6, 6]              32
          Dropout-22             [-1, 16, 6, 6]               0
           Conv2d-23             [-1, 14, 6, 6]           2,016
             ReLU-24             [-1, 14, 6, 6]               0
      BatchNorm2d-25             [-1, 14, 6, 6]              28
          Dropout-26             [-1, 14, 6, 6]               0
        AvgPool2d-27             [-1, 14, 1, 1]               0
           Conv2d-28             [-1, 10, 1, 1]             140
================================================================
Total params: 7,774
Trainable params: 7,774
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.56
Params size (MB): 0.03
Estimated Total Size (MB): 0.60
```
## Logs from local model run
```
EPOCH: 1
Loss=0.10382454842329025 Batch_id=468 Accuracy=93.60: 100%|██████████| 469/469 [00:06<00:00, 72.35it/s]  

Test set: Average loss: 0.0562, Accuracy: 9836/10000 (98.36%)

EPOCH: 2
Loss=0.013904877007007599 Batch_id=468 Accuracy=98.33: 100%|██████████| 469/469 [00:06<00:00, 72.64it/s] 

Test set: Average loss: 0.0421, Accuracy: 9873/10000 (98.73%)

EPOCH: 3
Loss=0.06856909394264221 Batch_id=468 Accuracy=98.69: 100%|██████████| 469/469 [00:06<00:00, 72.39it/s]  

Test set: Average loss: 0.0344, Accuracy: 9907/10000 (99.07%)

EPOCH: 4
Loss=0.019036216661334038 Batch_id=468 Accuracy=98.87: 100%|██████████| 469/469 [00:06<00:00, 72.33it/s]  

Test set: Average loss: 0.0288, Accuracy: 9912/10000 (99.12%)

EPOCH: 5
Loss=0.04306738078594208 Batch_id=468 Accuracy=99.20: 100%|██████████| 469/469 [00:06<00:00, 70.20it/s]   

Test set: Average loss: 0.0212, Accuracy: 9939/10000 (99.39%)

EPOCH: 6
Loss=0.009497318416833878 Batch_id=468 Accuracy=99.31: 100%|██████████| 469/469 [00:07<00:00, 62.61it/s]  

Test set: Average loss: 0.0208, Accuracy: 9939/10000 (99.39%)

EPOCH: 7
Loss=0.02535936050117016 Batch_id=468 Accuracy=99.34: 100%|██████████| 469/469 [00:07<00:00, 63.02it/s]   

Test set: Average loss: 0.0210, Accuracy: 9941/10000 (99.41%)

EPOCH: 8
Loss=0.02803097479045391 Batch_id=468 Accuracy=99.36: 100%|██████████| 469/469 [00:07<00:00, 63.39it/s]   

Test set: Average loss: 0.0204, Accuracy: 9938/10000 (99.38%)

EPOCH: 9
Loss=0.02037068083882332 Batch_id=468 Accuracy=99.42: 100%|██████████| 469/469 [00:07<00:00, 63.54it/s]   

Test set: Average loss: 0.0201, Accuracy: 9939/10000 (99.39%)

EPOCH: 10
Loss=0.004072252660989761 Batch_id=468 Accuracy=99.39: 100%|██████████| 469/469 [00:07<00:00, 62.67it/s]  

Test set: Average loss: 0.0199, Accuracy: 9943/10000 (99.43%)

EPOCH: 11
Loss=0.008614900521934032 Batch_id=468 Accuracy=99.41: 100%|██████████| 469/469 [00:07<00:00, 62.15it/s]  

Test set: Average loss: 0.0201, Accuracy: 9940/10000 (99.40%)

EPOCH: 12
Loss=0.010816306807100773 Batch_id=468 Accuracy=99.41: 100%|██████████| 469/469 [00:07<00:00, 62.99it/s]  

Test set: Average loss: 0.0197, Accuracy: 9944/10000 (99.44%)

EPOCH: 13
Loss=0.00832297932356596 Batch_id=468 Accuracy=99.39: 100%|██████████| 469/469 [00:07<00:00, 63.70it/s]   

Test set: Average loss: 0.0199, Accuracy: 9943/10000 (99.43%)

EPOCH: 14
Loss=0.007128103170543909 Batch_id=468 Accuracy=99.42: 100%|██████████| 469/469 [00:07<00:00, 63.44it/s]  

Test set: Average loss: 0.0203, Accuracy: 9943/10000 (99.43%)

EPOCH: 15
Loss=0.02005930431187153 Batch_id=468 Accuracy=99.42: 100%|██████████| 469/469 [00:07<00:00, 63.73it/s]   

Test set: Average loss: 0.0201, Accuracy: 9942/10000 (99.42%)

-------------------------------------------------------------
```
