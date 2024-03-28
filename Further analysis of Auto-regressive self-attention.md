Our experiments below demonstrate that our auto-regressive embedding, compared to point-wise (embedding values at the same timestamp as tokens), and patch-wise (embedding where the same time series is divided into different patches), maintains crucial temporal positional information within permutation-invariant self-attention mechanisms.

**'w/o'** means without position embedding, **pos** means position embedding is used. 

Results:

|Models|pred_len|Type|Auto|Auto|Patch|Patch|Point|Point|
|-|-|-|-|-|-|-|-|-|
|Dataset\Metric|||MSE|MAE|MSE|MAE|MSE|MAE|
|ETTh2|96|w/o|0.294|0.343|0.382|0.429|1.453|1.000|
|||pos|0.293|0.343|0.354|0.404|0.958|0.803|
||720|w/o|0.413|0.432|0.926|0.703|3.533|1.625|
|||pos|0.416|0.433|0.835|0.666|1.569|0.991|
|ETTm2|96|w/o|0.176|0.257|0.226|0.321|0.419|0.511|
|||pos|0.175|0.256|0.208|0.314|0.335|0.447|
||720|w/o|0.398|0.395|0.963|0.726|2.826|1.386|
|||pos|0.393|0.394|0.732|0.671|1.411|0.996|
|Weather|96|w/o|0.166|0.211|0.176|0.240|0.219|0.309|
|||pos|0.167|0.213|0.165|0.234|0.174|0.260|
||720|w/o|0.342|0.343|0.355|0.405|0.351|0.395|
|||pos|0.342|0.344|0.337|0.370|0.346|0.388|


Based on [DLinear](https://arxiv.org/pdf/2205.13504.pdf), **self-attention** is essentially **permutation-invariant**. Therefore, simply using attention mechanisms may not effectively capture the temporal variations within time series. To address this issue, many approaches adopt **positional encoding**. For instance, both **patch-wise** and **point-wise** self-attention mechanisms exhibit significantly degenerated forecasting performance **without positional encoding**.

**Tokens generated through our autoregressive process inherently capture the temporal variations within the time series**. When the attention mechanism is applied, it can effectively learn the temporal information required for prediction **without the need for positional encoding**.
