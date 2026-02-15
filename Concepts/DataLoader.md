# 🧠 Big Picture (Before Details)
When training a neural network:
- ❌ We cannot give the entire dataset at once
- ✔️ We give data in small chunks called batches

`DataLoader` is the tool that:
- Breaks data into batches
- Shuffles data
- Feeds data to the model efficiently

# 🧩 Part-by-Part Explanation 
## `DataLoader(...)` :
`DataLoader` converts the dataset into something the model can consume easily.
💡 It answers questions like:
- How many  images at once ? 
- In what Order ? 
- How fast data should me loaded ? 

## `batch_size = 128` 
At one time model can see the 128 images 
🔍 What actually happens?
- If your dataset has 10,000 images: 
 - `10000 / 128 ≈ 79 batches`
 - Each training epoch will have 79 steps (iterations)

## `shuffle = True` 
Randomly mix the data every epoch
Why this matters:
- Prevents the model from memorizing order
- Improves generalization
- Avoids biased learning

> DataLoader takes your dataset, shuffles it, splits it into batches, and feeds it efficiently to the model during training.