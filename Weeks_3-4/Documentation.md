# Documentation
## Changes made in PyTorch Implementation  
There are two critical changes that have been made,  
1. The shape of the tensors in PyTorch is (Batch_Size, Num_Channels, Height, Width) whereas in Keras it is (Batch_Size, Height, Width, Num_Channels). This has been corrected.
2. There does not exist a model.fit() equivalent in PyTorch, hence the training loop had to be implemented manually.
3. In PyTorch, all numpy arrays have to be converted to PyTorch Tensors before they can be passed to the model. This is unlike Keras where we can durectly use numpy arrays.

## Challenges
The biggest challenge faced was the incompatibility of the provided Keras code with Keras3.0. This required the code to be first updated so that compatibility is restored before conversion to PyTorch.

## Results
The results of the converted PyTorch model are in close agreement with the respective Keras model.
