To further investigate why our **LD** is a better time series decomposition solution than moving average kernel (**MOV**), we conducted the following analysis on the seasonal part and trend part obtained. 

Since the seasonal part represents repetitive patterns in the raw sequence, **a good seasonal part should capture all major frequencies in the raw sequence.**
We separately calculated the **amplitude similarity of the dominant frequencies(top 25%)** between the seasonal part obtained from LD and MOV and the raw sequence.

**A better decomposition strategy should yield a seasonal part with higher similarity to the dominant frequencies of the raw sequence.**

**A good trend part should effectively capture the trend changes in the original sequence.** Thus, we employed Dynamic Time Warping ([DTW](https://doi.org/10.1007/978-3-540-74048-3_4)) to compute the similarity between the raw sequence and the trend parts obtained from the two decompositions. 

**A superior decomposition strategy should result in a trend part with higher DTW similarity to the raw sequence.**

We selected **the final dimension of each dataset**. The variables used are as follows: 
- ETTh1&2, ETTm1&2: Oil Temperature (OT) every **hour or 15minutes**.
- Electricity: the **hourly** electricity consumption of the 321th (last) user.
- Solar-Energy: the solar power production every **10 minutes** of the 137th(last) PV plant.
- Traffic: the **hourly** road occupancy rates measured by the 862th(last) sensor.
- Weather: CO2 (ppm) collected every **10 minutes**.
  
**LD** are pretrained on task: **input-96-forecast-720**

*To avoid cherry-picking, both metrics are computed by averaging the results calculated over the entire dataset.*

Results:
|Kernel|LD (Ours)|LD (Ours)|MOV|MOV|
|-|-|-|-|-|
|Dataset\Metric|DTW|FFT|DTW|FFT|
|Electricity|**0.643**|**0.942**|0.618|0.931|
|Solar_Energy|**0.910**|**0.781**|0.873|0.734|
|Traffic|**0.603**|**0.993**|0.563|0.991|
|weather|**0.858**|**0.760**|0.846|0.691|
|ETTh1|**0.741**|**0.892**|0.724|0.852|
|ETTh2|**0.675**|**0.900**|0.652|0.887|
|ETTm1|**0.821**|**0.754**|0.808|0.717|
|ETTm2|**0.925**|**0.894**|0.908|0.759|

**LD** significantly outperforms **MOV** on eight datasets in: **FFT** (similarity of the most dominant frequency between the seasonal part and raw series) and **DTW** (DTW similarity between the trend part and the raw series). 

Therefore, it's rational to conclude that **our LD is a superior time series decomposition approach compared to naive MOV**.
