# PyTorch API Quick Reference

This document provides a quick reference for commonly used PyTorch APIs used throughout the *Mastering Deep Learning* book.

## Tensor Operations

### Tensor Creation

```python
torch.tensor(data)
torch.zeros(shape)
torch.ones(shape)
torch.randn(shape)
torch.arange(start, end)
```

### Tensor Manipulation

```python
tensor.shape
tensor.size()

tensor.reshape()
tensor.view()

tensor.unsqueeze()
tensor.squeeze()

torch.cat()
torch.stack()
```

### Mathematical Operations

```python
a + b
a - b
a * b
a / b

torch.matmul(a, b)
torch.sum(tensor)
torch.mean(tensor)
torch.max(tensor)
```

### Device Management

```python
tensor.to(device)

torch.cuda.is_available()
```

---

## Neural Network Modules

### Base Class

```python
import torch.nn as nn

class Model(nn.Module):
    def __init__(self):
        super().__init__()

    def forward(self, x):
        return x
```

### Common Layers

```python
nn.Linear()
nn.Conv2d()
nn.MaxPool2d()
nn.Flatten()
nn.Dropout()
nn.BatchNorm1d()
nn.BatchNorm2d()
nn.Embedding()
nn.RNN()
nn.LSTM()
nn.GRU()
nn.Transformer()
```

### Activation Functions

```python
nn.ReLU()
nn.Sigmoid()
nn.Tanh()
nn.Softmax()
nn.LogSoftmax()
```

### Loss Functions

```python
nn.MSELoss()
nn.L1Loss()
nn.BCELoss()
nn.BCEWithLogitsLoss()
nn.CrossEntropyLoss()
nn.NLLLoss()
```

---

## Optimizers

### Creating an Optimizer

```python
import torch.optim as optim

optimizer = optim.Adam(
    model.parameters(),
    lr=0.001
)
```

### Common Optimizers

```python
optim.SGD()
optim.Adam()
optim.AdamW()
optim.RMSprop()
optim.Adagrad()
```

### Training Steps

```python
optimizer.zero_grad()

loss.backward()

optimizer.step()
```

### Learning Rate Schedulers

```python
optim.lr_scheduler.StepLR()
optim.lr_scheduler.MultiStepLR()
optim.lr_scheduler.ExponentialLR()
optim.lr_scheduler.ReduceLROnPlateau()
optim.lr_scheduler.CosineAnnealingLR()
```

---

## Dataset and DataLoader APIs

### Dataset Base Class

```python
from torch.utils.data import Dataset

class CustomDataset(Dataset):

    def __len__(self):
        pass

    def __getitem__(self, index):
        pass
```

### DataLoader

```python
from torch.utils.data import DataLoader

loader = DataLoader(
    dataset,
    batch_size=32,
    shuffle=True
)
```

### Useful Dataset Utilities

```python
TensorDataset()

random_split()

DataLoader()
```

### Iterating Through Data

```python
for inputs, labels in loader:
    outputs = model(inputs)
```

### Common DataLoader Parameters

```python
batch_size
shuffle
num_workers
drop_last
pin_memory
```

---

## Model Saving and Loading

### Save Model

```python
torch.save(
    model.state_dict(),
    "model.pth"
)
```

### Load Model

```python
model.load_state_dict(
    torch.load("model.pth")
)

model.eval()
```

---

## Training Workflow

```python
model.train()

for inputs, labels in loader:

    outputs = model(inputs)

    loss = criterion(
        outputs,
        labels
    )

    optimizer.zero_grad()

    loss.backward()

    optimizer.step()
```

---

## Evaluation Workflow

```python
model.eval()

with torch.no_grad():

    outputs = model(inputs)

    predictions = outputs.argmax(dim=1)
```

---

For complete examples and hands-on labs, refer to the corresponding chapter folders in this repository.
