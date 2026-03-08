# Classification : 
For this we will use the torch.nn.Sequential 
- Here is the table what matter most .
  
| Hyperparameter | Binary Classification | Multiclass Classification |
|---|---|---|
| **Input layer shape (`in_features`)** | Same as number of features (e.g. 5 for age, sex, height, weight, smoking status in heart disease prediction) | Same as binary classification |
| **Hidden layer(s)** | Problem specific, minimum = 1, maximum = unlimited | Same as binary classification |
| **Neurons per hidden layer** | Problem specific, generally 10 to 512 | Same as binary classification |
| **Output layer shape (`out_features`)** | 1 (one class or the other) | 1 per class (e.g. 3 for food, person or dog photo) |
| **Hidden layer activation** | Usually ReLU (rectified linear unit) but can be many others | Same as binary classification |
| **Output activation** | Sigmoid (`torch.sigmoid` in PyTorch) | Softmax (`torch.softmax` in PyTorch) |
| **Loss function** | Binary crossentropy (`torch.nn.BCELoss` in PyTorch) | Cross entropy (`torch.nn.CrossEntropyLoss` in PyTorch) |
| **Optimizer** | SGD (stochastic gradient descent), Adam (see `torch.optim` for more options) | Same as binary classification |
