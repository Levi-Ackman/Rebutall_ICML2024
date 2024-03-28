To further investigate why our **LD** is a better time series decomposition solution than moving average kernel (**MOV**), we conducted the following analysis on the seasonal part and trend part obtained. 

Since the seasonal part represents repetitive patterns in the raw sequence, **a good seasonal part should capture all major frequencies in the raw sequence.**
We separately calculated the **amplitude similarity of the dominant frequencies of the top **66.6%** (i.e., the top **2/3**)** between the seasonal part obtained from LD and MOV and the raw sequence.

**A better decomposition strategy should yield a seasonal part with higher similarity to the dominant frequencies of the raw sequence.**

**A good trend part should effectively capture the trend changes in the original sequence.** Thus, we employed Dynamic Time Warping ([DTW](https://doi.org/10.1007/978-3-540-74048-3_4)) to compute the similarity between the raw sequence and the trend parts obtained from the two decompositions. 

**A superior decomposition strategy should result in a trend part with higher DTW similarity to the raw sequence.**

Results:

|Kernel|LD (Ours)|LD (Ours)|MOV|MOV|
|-|-|-|-|-|
|Dataset\Metric|DTW|FFT|DTW|FFT|
|Electricity|**0.633**|**0.978**|0.614|0.913|
|Solar_Energy|**0.602**|**0.960**|0.590|0.920|
|Traffic|**0.650**|**0.813**|0.621|0.732|
|weather|**0.694**|**0.987**|0.686|0.956|
|ETTh1|**0.676**|**0.995**|0.670|0.983|
|ETTh2|**0.689**|**0.996**|0.683|0.834|
|ETTm1|**0.711**|**0.909**|0.704|0.846|
|ETTm2|**0.592**|**0.921**|0.573|0.907|

**LD** significantly outperforms **MOV** on eight datasets in: **FFT** (similarity of the most dominant frequency between the seasonal part and raw series) and **DTW** (DTW similarity between the trend part and the raw series). 

Therefore, it's rational to conclude that **our LD is a superior time series decomposition approach compared to naive MOV**.
