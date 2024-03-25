Taking the prediction task of input-96-forecast-720 on the ETTh1 dataset as an example, we explored the efficiency of Leddam (Ours) and four state-of-the-art transformer-based multi-variate time series forecasting models: iTransformer, Crossformer, PatchTST, and FEDformer. 
We sequentially evaluated the MAE, MSE for predictions, parameter count, and the inference time for a batch size of 128.

| Models       | Parameter(M) | time(ms) | MSE   | MAE   |
|--------------|--------------|----------|-------|-------|
| Leddam       | **1.450**        | **6.581**    | **0.457** | **0.457** |
| iTransformer | 5.154        | 10.437   | 0.503 | 0.491 |
| Crossformer  | 6.875        | 49.387   | 0.814 | 0.692 |
| PatchTST     | 9.168        | 13.785   | 0.529 | 0.500 |
| FEDformer    | 18.060       | 37.332   | 0.506 | 0.507 |
