# Saving the Model . 

1. `torch.save()` - Allows us to save the PyTorch object in the Python's pickle formate 
2. `torch.load()` - Allows the load the saved model.
3. `torch.nn.Module.load_state_dict()` - Allows us to load the model's saved state dictionary 

## Code : 
- Saving : 
```python
torch.save(model.state_dict() , <PATH>)
```

- Loading : 
```py
model = Linear()

model.load_state_dict(torch.load(f = <PATH>))
```

## Reading meterials : 
1. https://docs.pytorch.org/tutorials/beginner/saving_loading_models.html