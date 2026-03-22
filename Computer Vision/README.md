# Working with the Image 

Deep Learning model only works with the Numbers . <br>
So you have convert your image to the number represenation . <br> 

So you have to  convert it into this kind of formate : 
```Python
[Batch_size , Colour_channels , Width , Height] <--(Users in the PyTorch)
```
Or 
```python
[Batch_size , Width, Height, Color_channels]
```
- Note : In the dataset if there are the different size of the images then Then we have to fix the optimal width and Height kind of things . 

- Batch_size : In deep learning, the batch size is a crucial hyperparameter that defines the number of training examples processed together in one iteration (forward and backward pass) before the model's internal parameters are updated . 
   - So Our meaching learning algo will look that 32 or 64 images at a time . 


# Computer Vision Libarary : 
1. `torchvision` 
2. `torchvision.datasets` : Gets datasets and data function here 
3. `torchvision.models` : To get pre-Trained models . You can use it for own problem 
4. `torchvision.transforms` : Functions for manuplating your vision data which is the best for our models comverting into numbers 
5. `torch.utils.data.Dataset` : Base dataset class for pytorch
6. `torch.utils.data.DataLoader` : Create PyThon itrrable over a dataset 
