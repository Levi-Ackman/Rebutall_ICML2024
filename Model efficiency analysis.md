We evaluated the **parameter count**, and the **inference time(average of 5 runs)** wiht batch_size\= **1** on **ETTh1 and Electricity** dataset. We set the model dimension in {256,512}, and number of backbone layers to **2**.

We explored **Leddam (Ours)** and four transformer-based multivariate time series forecasting models: **iTransformer**, **Crossformer**, **PatchTST**, and **FEDformer**. 

Results:

**'*' stand for former**
  
|Models||Leddam|Leddam|PatchTST|PatchTST|Cross*|Cross*|iTrans*|iTrans*|FED*|FED*|
|-|-|-|-|-|-|-|-|-|-|-|-|
||dim|Parameter(M)|time(ms)|Para|time|Para|time|Para|time|Para|time|
|ETTh1|256|2.50|233.92|3.27|251.00|8.19|399.00|**1.27**|**177.67**|3.43|303.556|
||512|9.20|249.34|8.64|266.66|32.11|445.74|**4.63**|**190.92**|13.68|345.736|
|Electricity|256|2.59|283.04|3.27|322.53|13.66|432.40|**1.27**|**192.12**|4.24|347.634|
||512|9.36|296.70|8.64|411.96|43.04|507.54|**4.63**|**249.60**|15.29|398.599|

It's noteworthy that he LD implementation utilizes a single convolutional kernel with kernel size of 25 shared across all channels. The total number of parameters is 25(kernel parameters)+1(bias), making it remarkably compact.
