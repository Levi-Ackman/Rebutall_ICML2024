We investigated the impact of the most significant parameters of **Leddam**: 

- **model dimension (dim)**, 
- **number of dual attention layers (n_layer)**, 
- **dropout ratio (dropout)**, 
- **size of decomposition kernel (kernel_size)**. 

The default settings were below:
- **dropout = 0.0**
- **dim = 512**
- **n_layer = 2**
- **Kernel_sizes = 25**
  
Results:

**Dropout**:
|Dataset|ETTm1||ETTm2||
|-|-|-|-|-|
|Dropout\Metric|MSE|MAE|MSE|MAE|
|0.0|0.469|0.447|0.406|0.400|
|0.1|0.468|0.446|0.404|0.401|
|0.2|0.476|0.452|0.406|0.401|
|0.5|0.474|0.452|0.409|0.404|

**Dim**:
|Dataset|ETTm1||ETTm2||
|-|-|-|-|-|
|Dim\Metric|MSE|MAE|MSE|MAE|
|128|0.486|0.454|0.399|0.397|
|256|0.473|0.449|0.403|0.399|
|512|0.469|0.447|0.406|0.400|
|1024|0.492|0.459|0.402|0.397|


**n_layer**:
|Dataset|ETTm1||ETTm2||
|-|-|-|-|-|
|n_layer\Metric|MSE|MAE|MSE|MAE|
|1|0.474|0.447|0.398|0.398|
|2|0.469|0.447|0.406|0.400|
|3|0.482|0.456|0.427|0.413|
|4|0.485|0.456|0.407|0.401|

**Kernel_size**:
|Dataset|ETTm1||ETTm2||
|-|-|-|-|-|
|Kernel\Metric|MSE|MAE|MSE|MAE|
|15|0.469|0.447|0.406|0.400|
|25|0.469|0.447|0.406|0.400|
|55|0.469|0.448|0.407|0.401|
|75|0.470|0.446|0.406|0.401|
|105|0.469|0.447|0.406|0.400|

We can easily conclude that **Leddam** is insensitive to dropout ratio and kernel size, while more sensitive to the number of Dual Attention layers and model dimension. For the kernel size, we argue after our initialization with a Gaussian distribution of 0 mean and 1 variance, the weight of the central element are the largest. As moving away from the center, the weights gradually decrease. Therefore, when the kernel size increases, the weights of the farther points become smaller, thus not significantly affecting the final decomposition result. 
