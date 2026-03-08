# Working with the Image 

Deep Learning model only works with the Numbers . <br>
So you have convert your image to the number represenation . <br> 

So you have to  convert it into this kind of formate : 
```
[Batch_size , Colour_channels , Width , Height]
```

- Batch_size : In deep learning, the batch size is a crucial hyperparameter that defines the number of training examples processed together in one iteration (forward and backward pass) before the model's internal parameters are updated . 
   - So Our meaching learning algo will look that 32 or 64 images at a time . 