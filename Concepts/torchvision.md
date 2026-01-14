# `transforms.Compose`
`transforms.Compose` (in libraries like PyTorch) chains multiple data transformation functions (e.g., resizing, normalizing, converting to tensor)into a single, sequential pipeline, allowing complex preprocessing steps to be applied easily to datasets like images, making data ready for machine learning models by applying them in the order listed within the Compose function.  

## How it works
- Chaining Transforms : you provide a list of individual transform objects (like `ToTensor()` , `Normalize()`, `RandomCrop()` ) to `transforms.Compose`. 

## Syntax : 
```python
transform = transforms.Compose([
    transforms.ToTensor(),
    transforms.Normalize(
        mean=(0.5, 0.5, 0.5),
        std=(0.5, 0.5, 0.5)
    )
])
```
---

# `transforms.Normalize` : 

This transform normalizes image pixel values so that they will be easy for neural network . <br>
Think of it as:
> “Rescaling image values into a clean, balanced range that neural networks prefer.”

## `transforms.Normalize(`
Normalization chnages pixel values using tis formula 
```
ouput = (input - mean) / std
```
Neural networks train faster and more stably when inputs are normalized.

## `mean=(0.5, 0.5, 0.5)`
This line defines the mean values for each channel for `RGB` formate .
- First (0.5) -> Red
- Seond (0.5) -> Green 
- Third (0.5) -> blue 

## `std=(0.5, 0.5, 0.5)` 
This is the standard deviation for each channel 
Again : 
- Red -> 0.5
- Green -> o.5 
- Third -> 0.5
This controls how much we scale the data after shifting.

## In One Sentence 
> This normalization subtracts 0.5 from each RGB channel and divides by 0.5, transforming image pixel values from [0, 1] into [-1, 1], which helps neural networks learn more efficiently.