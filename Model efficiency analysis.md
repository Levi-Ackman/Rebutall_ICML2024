## Model efficiency analysis

Taking the prediction task of input-96-forecast-720 on the ETTh1 dataset as an example, we explored the efficiency of **Leddam (Ours)** and four state-of-the-art transformer-based multi-variate time series forecasting models: [iTransformer](https://arxiv.org/abs/2310.06625), [Crossformer](https://openreview.net/pdf?id=vSVLM2j9eie), [PatchTST](https://openreview.net/pdf?id=Jbdc0vTOcol), and [FEDformer](https://arxiv.org/abs/2201.12740). 
We sequentially evaluated the MAE, MSE for predictions, parameter count, and the inference time for a batch size of 128. We set the model dimension uniformly to 512.

| Models       | Parameter(M) | time(ms) | MSE   | MAE   |
|--------------|--------------|----------|-------|-------|
| Leddam       | **1.450**        | **6.581**    | **0.457** | **0.457** |
| iTransformer | 5.154        | 10.437   | 0.503 | 0.491 |
| Crossformer  | 6.875        | 49.387   | 0.814 | 0.692 |
| PatchTST     | 9.168        | 13.785   | 0.529 | 0.500 |
| FEDformer    | 18.060       | 37.332   | 0.506 | 0.507 |

Due to the fact that our Leddam model only requires a single layer of Dual Attention to achieve optimal predictive performance, it excels in inference speed, parameter efficiency, and other metrics!
Due to implementation of the learnable decomposition kernel, which consists of a convolutional kernel with a kernel size of 25 shared across all channels, the total number of parameters is only 25 (kernel parameters) + 1 (bias). Indeed, it is a quite small number of parameters.