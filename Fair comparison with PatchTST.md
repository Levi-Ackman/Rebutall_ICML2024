We standardized the input length of all baselines to 96 following [iTransformer](iTransformer). But PatchTST and DLinear used input lengths of 512 and 336 in their original papers, respectively. Hence, we rerun the experiments for PatchTST and DLinear using input length of 96 to ensure fair comparison. We also conducted experiments with **a longer look-back window (512)** as shown below, **our Leddam** still **outperforms** other SOTA methods like **PatchTST**.

|Models|pred_len|Leddam|Leddam|PatchTST|PatchTST|DLinear|DLinear|
|-|-|-|-|-|-|-|-|
|Dataset\Metric||MSE|MAE|MSE|MAE|MSE|MAE|
|ETTm1|96|0.295|0.346|**0.293**|0.346|0.299|**0.343**|
|| 720|**0.412**|**0.417**|0.416|0.420|0.425|0.421|
|ETTm2|96|**0.163**|**0.254**|0.166|0.256|0.167|0.260|
||720|**0.361**|**0.382**|0.362|0.385|0.397| 0.421|
|Electricity|96|**0.122**|**0.217**|0.129|0.222|0.140|0.237|
||720|**0.188**|**0.285**|0.197|0.290| 0.203|0.301|
|Weather|96|0.152|**0.197**|**0.149**| 0.198|0.176|0.237|
||720|**0.312**|**0.332**|0.314|0.334| 0.323|0.362|
