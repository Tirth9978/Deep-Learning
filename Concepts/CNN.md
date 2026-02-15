# Look at the Code 
```python 
class SimpleCNN(nn.Module):
    def __init__(self):
        super().__init__()
        
        self.features = nn.Sequential(
            nn.Conv2d(3, 32, kernel_size=3, padding=1),
            nn.ReLU(),
            nn.MaxPool2d(2),

            nn.Conv2d(32, 64, kernel_size=3, padding=1),
            nn.ReLU(),
            nn.MaxPool2d(2)
        )
        
        self.classifier = nn.Sequential(
            nn.Linear(64 * 8 * 8, 256),
            nn.ReLU(),
            nn.Linear(256, 10)
        )

    def forward(self, x):
        x = self.features(x)
        x = x.view(x.size(0), -1)
        x = self.classifier(x)
        return x
```

---
# First Convolution Block 
```python
nn.Conv2d(3, 32, kernel_size=3, padding=1),
nn.ReLU(),
nn.MaxPool2d(2),
```

## `nn.Conv2d(3, 32, kernel_size=3, padding=1)`
This is a 2D convolution layer.
| Parameter       | Meaning                                           |
| --------------- | ------------------------------------------------- |
| `3`             | Number of input channels (RGB image → 3 channels) |
| `32`            | Number of filters (output channels)               |
| `kernel_size=3` | 3×3 convolution filter                            |
| `padding=1`     | Keeps spatial size the same                       |


📌 What it does:-
- Take the RGB Image 
- Applies the  32 different 3 x 3 filters 
- Produce the 32 features .

📐 Shape change example (if input is 3 × 64 × 64):
```
Input:   (3, 64, 64)
Output: (32, 64, 64)
```

## `nn.MaxPool2d(2)`
This is Max Pooling with a 2×2 window.<br>
- Takes the maximum value in each 2×2 region
- Reduces height and width by half
- Keeps the most important features


📐 Shape change: 
```
(32, 64, 64)  →  (32, 32, 32)
```
