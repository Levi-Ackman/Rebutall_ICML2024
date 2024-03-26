## Further performance comparisons of predictions were made using an input length of 512 (aligned with PatchTST).

To ensure fair comparison, we followed [TimesNet](https://arxiv.org/abs/2210.02186) and standardized the input length of all baselines to 96. However, considering that [PatchTST](https://openreview.net/pdf?id=Jbdc0vTOcol) and [DLinear](https://arxiv.org/pdf/2205.13504.pdf) used input lengths of 512 and 336, respectively, in their original papers, to avoid unfair comparison, we additionally set the input length of **Leddam (Ours)** to 512. We compared the results with those reported in [PatchTST](https://openreview.net/pdf?id=Jbdc0vTOcol) on the two prediction tasks of the four datasets: ETTm1, ETTm2, Weather, and Electricity, namely input-512-forecast-96/720. The results are as follows:

| Models    | Length | Leddam     | Leddam     | PatchTST     | PatchTST     | DLinear     | DLinear     |
|-----------|--------|------------|------------|--------------|--------------|-------------|-------------|
| Metric    |        | MSE        | MAE        | MSE          | MAE          | MSE         |MAE          |
| ETTm1     | 96     | 0.295      | 0.346      | **0.293**        | 0.346        | 0.299       | **0.343**       |
|           | 720    | **0.416**      | **0.418**      | 0.416        | 0.420        | 0.425       | 0.421       |
| ETTm2     | 96     | **0.166**      | **0.256**      | 0.166        | 0.256        | 0.167       | 0.260       |
|           | 720    | **0.361**      | **0.382**      | 0.362        | 0.385        | 0.397       | 0.421       |
|Electricity| 96     | **0.122**      | **0.219**      | 0.129        | 0.222        | 0.140       | 0.237       |
|           | 720    | **0.188**      | **0.285**      | 0.197        | 0.290        | 0.203       | 0.301       |
| Weather   | 96     | 0.152      | **0.197**      | **0.149**        | 0.198        | 0.176       | 0.237       |
|           | 720    | **0.312**      | **0.332**      | 0.314        | 0.334        | 0.323       | 0.362       |

We can easily observe that in scenarios with **a longer look-back window** (longer historical inputs), **our Leddam** still **outperforms** then state-of-the-art models like **PatchTST**.
