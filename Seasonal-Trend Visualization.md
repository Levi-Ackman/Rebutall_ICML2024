Given advice from **reviewer 5uUN**, in addition to the visualization results of the **trend part** obtained from the time series decomposition by **LD** and **[MOV](https://arxiv.org/abs/2106.13008)** as mentioned in the original paper, 
we further provide the visualization results of the **seasonal part** here.

We selected **the final dimension of each dataset**. The variables used are as follows: 
- ETTh1&2, ETTm1&2: Oil Temperature (OT) every **hour or 15minutes**.
- Electricity: the **hourly** electricity consumption of the 321th (last) user.
- Solar-Energy: the solar power production every **10 minutes** of the 137th(last) PV plant.
- Traffic: the **hourly** road occupancy rates measured by the 862th(last) sensor.
- Weather: CO2 (ppm) collected every **10 minutes**.
  
**LD** are pretrained on task: **input-96-forecast-720.**

Given a sampling frequency of 10, 15 minutes, or 1 hour for these datasets, we opt to decompose time series into two lengths: **120 and 720**, to better contrast the decomposition results and reflect the extracted seasonal and trend patterns.

#### ETTh1 Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/ETTh1/trend.png" alt="ETTh1 trend" width=49%> <img src="Visualiziation_of_STD_120/ETTh1/season.png" alt="ETTh1 seasonal" width=49%>
#### ETTh1 Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/ETTh1/trend.png" alt="ETTh1 trend" width=49%> <img src="Visualiziation_of_STD_720/ETTh1/season.png" alt="ETTh1 seasonal" width=49%>
#### ETTh2 Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/ETTh2/trend.png" alt="ETTh2 trend" width=49%> <img src="Visualiziation_of_STD_120/ETTh2/season.png" alt="ETTh2 seasonal" width=49%>
#### ETTh2 Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/ETTh2/trend.png" alt="ETTh2 trend" width=49%> <img src="Visualiziation_of_STD_720/ETTh2/season.png" alt="ETTh2 seasonal" width=49%>
#### ETTm1 Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/ETTm1/trend.png" alt="ETTm1 trend" width=49%> <img src="Visualiziation_of_STD_120/ETTm1/season.png" alt="ETTm1 seasonal" width=49%>
#### ETTm1 Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/ETTm1/trend.png" alt="ETTm1 trend" width=49%> <img src="Visualiziation_of_STD_720/ETTm1/season.png" alt="ETTm1 seasonal" width=49%>
#### ETTm2 Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/ETTm2/trend.png" alt="ETTm2 trend" width=49%> <img src="Visualiziation_of_STD_120/ETTm2/season.png" alt="ETTm2 seasonal" width=49%>
#### ETTm2 Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/ETTm2/trend.png" alt="ETTm2 trend" width=49%> <img src="Visualiziation_of_STD_720/ETTm2/season.png" alt="ETTm2 seasonal" width=49%>
#### Electricity Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/Electricity/trend.png" alt="Electricity trend" width=49%> <img src="Visualiziation_of_STD_120/Electricity/season.png" alt="Electricity seasonal" width=49%>
#### Electricity Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/Electricity/trend.png" alt="Electricity trend" width=49%> <img src="Visualiziation_of_STD_720/Electricity/season.png" alt="Electricity seasonal" width=49%>
#### Traffic Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/Traffic/trend.png" alt="Traffic trend" width=49%> <img src="Visualiziation_of_STD_120/Traffic/season.png" alt="Traffic seasonal" width=49%>
#### Traffic Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/Traffic/trend.png" alt="Traffic trend" width=49%> <img src="Visualiziation_of_STD_720/Traffic/season.png" alt="Traffic seasonal" width=49%>
#### Solar Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/Solar/trend.png" alt="Solar trend" width=49%> <img src="Visualiziation_of_STD_120/Solar/season.png" alt="Solar seasonal" width=49%>
#### Solar Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/Solar/trend.png" alt="Solar trend" width=49%> <img src="Visualiziation_of_STD_720/Solar/season.png" alt="Solar seasonal" width=49%>
#### Weather Trend-Seasonal Decomposition Results of input-120 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_120/Weather/trend.png" alt="Weather trend" width=49%> <img src="Visualiziation_of_STD_120/Weather/season.png" alt="Weather seasonal" width=49%>
#### Weather Trend-Seasonal Decomposition Results of input-720 obttained by LD(Red) and MOV(Blue).  Left Trend part, Right seasonal Part.
<img src="Visualiziation_of_STD_720/Weather/trend.png" alt="Weather trend" width=49%> <img src="Visualiziation_of_STD_720/Weather/season.png" alt="Weather seasonal" width=49%>
