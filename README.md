# Leddam

This is the supplementary experiment and visualization repository for the paper "**Revitalizing Multivariate Time Series Forecasting: Learnable Decomposition with Inter-Series Dependencies and Intra-Series Variations Modeling**," currently under reviewed at ICML 2024.

## Readers can check each markdown file to view corresponding supplementary experiments and analyses.

**Seasonal-Trend Visualization.md：** 

Visualization of both Seasonal and Trend part decomposed by **LD** and **MOV** from eight datasets.

**Fair comparison with PatchTST.md：** 

Further performance comparisons of predictions were made using an input length of 512 (aligned with PatchTST).

**Further LD and MOV comparison and analysis.md：** 

Further Analysis of different decomposition strategy.

**Further analysis of Auto-regressive self-attention.md：** 

Further analysis of different attention mechanism in intra-sereis variation modeling. Point-wise, patch-wise, and auto-regressive self-attention.

**Hyperparameter sensitivity analysis.md：**  

Hyperparameter sensitivity study(model dimension (dim),number of dual attention layers (n_layer),dropout ratio (dropout),and size of decomposition kernel (kernel_size).)

**Model efficiency analysis.md:**

We sequentially evaluated the MAE, MSE for predictions, parameter count, and the inference time for a batch size of 128. We set the model dimension uniformly to 512.

**R-squared metric result.md:**

Further comparison of forecasting performance using R-squared as the evaluation metric

