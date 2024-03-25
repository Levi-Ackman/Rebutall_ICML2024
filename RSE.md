According to the suggestions from reviewer xxyy, we conducted additional experiments on the **ETTm1**, **ETTm2**, and **Weather** datasets to explore the model's performance in terms of **R-squared** (the coefficient of determination). Due to time and computational constraints, we selected a subset of the most representative models: 

**Leedam (Ours)**, 

[iTransformer](https://arxiv.org/abs/2310.06625),

[MICN](https://openreview.net/pdf?id=zt53IDUR1U),

[DLinear](https://arxiv.org/pdf/2205.13504.pdf),

[PatchTST](https://arxiv.org/abs/2211.14730),

[Crossformer](https://openreview.net/pdf?id=vSVLM2j9eie),

and two experimental tasks: input-96-forecast-96/720. The experimental results are as follows:

| Models       | pred_len | Leddam(Ours) | iTransformer | MICN  | DLinear | PatchTST | Crossformer |
|--------------|----------|--------------|--------------|-------|---------|----------|-------------|
| Metric       | RSE      | RSE          | RSE          | RSE   | RSE     | RSE      | RSE         |
| ETTh2        | 96       | 0.433        | 0.441        | 0.482 | 0.470   | 0.435    | 0.666       |
|              | 720      | 0.511        | 0.534        | 0.723 | 0.697   | 0.523    | 0.870       |
| ETTm2        | 96       | 0.340        | 0.347        | 0.352 | 0.356   | 0.343    | 0.421       |
|              | 720      | 0.507        | 0.517        | 0.606 | 0.589   | 0.510    | 1.076       |
| Weather      | 96       | 0.522        | 0.554        | 0.577 | 0.585   | 0.549    | 0.511       |
|              | 720      | 0.769        | 0.787        | 0.758 | 0.776   | 0.780    | 0.802       |

