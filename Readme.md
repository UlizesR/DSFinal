# Comparing Weather, CO₂, and Climate Topology of Rome and Chicago

## Authors
- Yinqi Wang  
- Uli Rodriguez  

## Colab Notebook
[Download the Colab notebook](./notebook/project_colab.ipynb)

---

## Introduction
This project compares weather patterns, atmospheric CO₂ trends, and climate structure for two cities located at similar latitudes: **Rome, Italy** and **Chicago, USA** (approximately 41°N). Despite their similar latitude, the two cities experience markedly different climates due to geographical and atmospheric factors.

We analyze temperature, precipitation, and atmospheric CO₂ data to address the following hypothesis:

> **Hypothesis:** Because Rome is close to the Mediterranean Sea, it is warmer than Chicago, and the colder city experiences more precipitation.

---

## Weather Analysis: Methods & Results
Daily temperature and precipitation data for **Chicago** were obtained from NOAA for the period **January 1, 2025 to July 1, 2025**. Corresponding data for **Rome** were obtained from Visual Crossing.

The results show that Rome consistently has higher temperatures than Chicago, supporting our hypothesis. During winter (January–March), Chicago frequently experiences temperatures below 0 °C, reaching nearly –20 °C at times, while Rome remains relatively mild, typically between 5–10 °C. In spring, both cities warm significantly, but Chicago experiences more dramatic temperature swings, while Rome warms steadily from approximately 13 °C to 30 °C.

Although both cities lie at similar latitudes, their climates differ substantially. Rome’s proximity to the Mediterranean Sea moderates temperature fluctuations due to the sea’s high heat capacity, while Chicago’s continental climate leads to sharper seasonal contrasts.

### Precipitation Patterns
Rome experiences significantly more rainy days than Chicago from January through May, averaging 15–21 rainy days per month compared to Chicago’s 6–13. However, in June, Rome becomes drier (7 rainy days) while Chicago experiences increased rainfall (10 rainy days).

This finding partially contradicts our original hypothesis. Rome’s Mediterranean climate brings wetter winters and springs, whereas Chicago’s continental climate results in colder, drier winters and increased summer precipitation driven by convective storms.

---

## Weather Conclusion
Rome is warmer than Chicago during winter and spring, consistent with Mediterranean climate influences. However, Rome becomes drier in summer, while Chicago experiences increased rainfall. These differences highlight the role of geography and atmospheric circulation in shaping local climate.

---

## CO₂ Trends: Methods & Results
Atmospheric CO₂ concentrations were analyzed using the **Mauna Loa Observatory dataset (1958–2025)**. After converting year and month data into timestamps, both long-term and short-term trends were examined.

The data reveal a clear long-term increase in CO₂ levels, rising from approximately **315 ppm in 1958** to over **425 ppm in 2025**, reflecting anthropogenic greenhouse gas emissions. Seasonal oscillations are also evident, with CO₂ peaking in late winter and declining in summer due to increased photosynthesis.

---

## CO₂ Comparison With Temperature
CO₂ data from **January–July 2025** were compared with temperature data for Rome and Chicago over the same period. While daily temperatures vary widely (–15 °C to 30 °C), CO₂ levels fluctuate only slightly within a narrow ~5 ppm range.

This demonstrates that short-term CO₂ variations do not directly influence daily or weekly weather. Instead, local temperature is governed by regional climate, geography, and atmospheric dynamics. CO₂ impacts climate on long time scales (decades), not short-term weather variability.

---

## CO₂ Conclusion
Although global CO₂ levels continue to rise and contribute to long-term climate warming, they do not explain short-term temperature differences between individual cities. Long-term datasets are required to detect climate-scale relationships between CO₂ and temperature.

---

## Topological Data Analysis (TDA)

### Motivation
While traditional statistical methods capture averages and trends, they may fail to reveal the underlying *shape* of climate dynamics. To address this, we applied **Topological Data Analysis (TDA)** to monthly temperature data for Rome and Chicago using Meteostat.

### Methods
Monthly average temperature data (2000–2025) were standardized and analyzed using:
- **Time-delay embeddings (m = 3, τ = 1)** to capture month-to-month dynamics
- **12-month sliding window embeddings** to capture annual climate structure

Persistent homology was computed, with focus on **H₁ features**, which correspond to loop-like structures associated with seasonal cycles.

### TDA Results
In the time-delay embedding, both cities exhibit persistent H₁ features corresponding to annual seasonality. However, **Rome shows a stronger dominant loop** (maximum persistence **0.9529**) compared to **Chicago (0.7796)**, indicating more stable month-to-month temperature dynamics.

The sliding window embedding further highlights climatic differences. Rome exhibits a highly persistent annual loop (maximum persistence **3.4849**) with fewer competing features, while Chicago shows a larger number of H₁ features and greater total persistence, reflecting stronger interannual variability.

### TDA Conclusion
Topological analysis reveals that Rome’s climate exhibits greater seasonal stability, while Chicago’s climate is more variable across both monthly and yearly scales. These findings align with the known Mediterranean climate of Rome and the continental climate of Chicago.

---

## References
- *Chicago, IL, US Climate Data (GHCN-Daily).* NOAA National Centers for Environmental Information, 2025. Climate Data Online (CDO).
- *Rome Climate and Weather Data.* Meteostat, 2025. Rome | Weather History & Climate.
