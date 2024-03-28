We evaluated the **MAE**, **MSE**, **parameter count**, and the **inference time(average of 5 runs)** wiht batch_size\= **128** on **ETTh1** dataset. We set the model dimension uniformly to **512**.

We explored **Leddam (Ours)** and four transformer-based multivariate time series forecasting models: iTransformer, Crossformer, PatchTST, and FEDformer. 

Results:

|Models|Parameter(M)|time(ms)|MSE|MAE|
|-|-|-|-|-|
|Leddam|**4.996**|**6.581**|**0.457**|**0.457**|
|iTransformer|5.154|10.437|0.503|0.491 |
|Crossformer|26.432|49.387|0.814|0.692 |
|PatchTST|9.168|13.785|0.529|0.500|
|FEDformer|18.060|37.332|0.506|0.507|

Leddam achieves optimal predictive performance with just one Dual Attention module, excelling in **inference speed** and **parameter efficiency**. The LD implementation utilizes a single convolutional kernel with kernel size of 25 shared across all channels. The total number of parameters is 25(kernel parameters)+1(bias), making it remarkably compact.
