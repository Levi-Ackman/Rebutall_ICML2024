# Research Analysis

To further investigate why our learnable decomposition kernel (LD) is a better time series decomposition solution than 
the simple moving average kernel (MOV), we conducted the following analysis on the seasonal part and trend part obtained from decomposition on eight datasets. 
Specifically, since the seasonal part represents repetitive patterns in the original sequence, 
a good seasonal part should capture all major frequencies in the original sequence.        
Hence, we separately calculated the similarity between the seasonal part obtained from
two decomposition strategies and the dominant frequencies of the first 66.6% (i.e., the first 2/3) of the original sequence. 
A better decomposition strategy should yield a seasonal part with higher similarity to the dominant frequencies of the original sequence.

Additionally, for a good trend part, it should effectively capture the trend changes in the original sequence. 
Thus, we utilized Dynamic Time Warping (DTW) to compute the similarity between the original sequence and the trend parts obtained from the two decompositions. 
A superior decomposition strategy should result in a trend part with higher DTW similarity to the original sequence.

Below are the results:

| Kernel         | LD (Ours) |       | MOV     |       |
|----------------|-----------|-------|---------|-------|
| Dataset\Metric | DTW       | FFT   | DTW     | FFT   |
| Electricity    | **0.633**     | **0.978** | 0.614   | 0.913 |
| Solar_Energy   | **0.602**     | **0.960** | 0.590   | 0.920 |
| Traffic        | **0.650**     | **0.813** | 0.621   | 0.732 |
| weather        | **0.694**     | **0.987** | 0.686   | 0.956 |
| ETTh1          | **0.676**     | **0.995** | 0.670   | 0.983 |
| ETTh2          | **0.689**     | **0.996** | 0.683   | 0.834 |
| ETTm1          | **0.711**     | **0.909** | 0.704   | 0.846 |
| ETTm2          | **0.592**     | **0.921** | 0.573   | 0.907 |

