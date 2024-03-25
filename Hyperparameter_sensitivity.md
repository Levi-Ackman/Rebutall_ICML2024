We investigated the impact of the most significant parameters of our Leddam to forecasting performance: 

**model dimension (dim)**, 

**number of dual attention layers (n_layer)**, 

**dropout ratio (dropout)**, 

and **size of decomposition kernel (kernel_size)**. 

We conducted experiments on the **ETTm1** and **ETTm2** datasets, where the experimental setup is **input-96-forecast-720**. 
The default experimental settings for these four parameters were as follows:

- **dropout = 0.0**
- **dim = 512**
- **n_layer = 2**
- **Kernel_sizes = 25**
The experimental results for each hyperparameter are as follows:
**Dropout**:

| Dataset        | ETTm1 |       | ETTm2 |       |
|----------------|-------|-------|-------|-------|
| Dropout\Metric | MSE   | MAE   | MSE   | MAE   |
| 0.0            | 0.469 | 0.447 | 0.406 | 0.400 |
| 0.1            | 0.468 | 0.446 | 0.404 | 0.401 |
| 0.2            | 0.476 | 0.452 | 0.406 | 0.401 |
| 0.5            | 0.474 | 0.452 | 0.409 | 0.404 |

**Dim**:

| Dataset        | ETTm1 |       | ETTm2 |       |
|----------------|-------|-------|-------|-------|
| Dim\Metric     | MSE   | MAE   | MSE   | MAE   |
| 128            | 0.486 | 0.454 | 0.399 | 0.397 |
| 256            | 0.473 | 0.449 | 0.403 | 0.399 |
| 512            | 0.469 | 0.447 | 0.406 | 0.400 |
| 1024           | 0.492 | 0.459 | 0.402 | 0.397 |

**n_layer**:

| Dataset        | ETTm1 |       | ETTm2 |       |
|----------------|-------|-------|-------|-------|
| n_layer\Metric | MSE   | MAE   | MSE   | MAE   |
| 1              | 0.474 | 0.447 | 0.398 | 0.398 |
| 2              | 0.469 | 0.447 | 0.406 | 0.400 |
| 3              | 0.482 | 0.456 | 0.427 | 0.413 |
| 4              | 0.485 | 0.456 | 0.407 | 0.401 |

**Kernel_size**:

| Dataset        | ETTm1 |       | ETTm2 |       |
|----------------|-------|-------|-------|-------|
| Kernel\Metric  | MSE   | MAE   | MSE   | MAE   |
| 15             | 0.469 | 0.447 | 0.406 | 0.400 |
| 25             | 0.469 | 0.447 | 0.406 | 0.400 |
| 55             | 0.469 | 0.448 | 0.407 | 0.401 |
| 75             | 0.470 | 0.446 | 0.406 | 0.401 |
| 105            | 0.469 | 0.447 | 0.406 | 0.400 |



