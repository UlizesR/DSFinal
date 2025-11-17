# Uli Raudales — Data Science Page

---

## Data Sources and Project Ideas

Below are five real-world datasets I am considering for my final project, along with short descriptions and ideas for exploring each one. Many of these ideas involve simple applications of Topological Data Analysis (TDA).

### **1. NOAA Daily Temperature Dataset (Kaggle)**  
Dataset: [Daily Temperature of Major Cities](https://www.kaggle.com/datasets/sudalairajkumar/daily-temperature-of-major-cities)  
**Description:**  
Daily temperature measurements collected from real weather stations in major global cities.  
**Project Idea:**  
Convert the temperature time series into a geometric point cloud using sliding-window (Takens) embeddings. Apply persistent homology to detect seasonal periodicity—revealing loops (H₁ features) corresponding to yearly climate cycles.

### **2. GeoLife GPS Trajectories (UCI Machine Learning Repository)**  
Dataset: [GeoLife GPS Trajectories 1.3](https://archive.ics.uci.edu/dataset/168/geolife+gps+trajectories)  
**Description:**  
Over 17,000 real GPS trajectories collected from 182 users over several years, including walking, biking, and driving paths.  
**Project Idea:**  
Select a single real-world trajectory and compute persistent homology to detect loops in the path. This reveals geometric structure in human movement patterns using H₁ persistence.

### **3. Human Activity Recognition (UCI Smartphone Sensor Data)**  
Dataset: [Human Activity Recognition Using Smartphones](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones)  
**Description:**  
Accelerometer and gyroscope sensor data collected from smartphones carried by volunteers performing activities such as walking, standing, and climbing stairs.  
**Project Idea:**  
Use TDA to compare the shape of motion patterns. Apply H₀ persistence to analyze how different activities form distinct topological clusters in feature space.

### **4. USGS Earthquake Catalog (Real Seismology Observations)**  
Dataset: [USGS Earthquake Catalog](https://earthquake.usgs.gov/earthquakes/search/)  
**Description:**  
A scientific observational dataset containing global earthquake events with magnitude, depth, location, and time. CSV downloads are customizable by region and date.  
**Project Idea:**  
Download earthquakes from a specific region (e.g., California). Use persistent homology (H₀/H₁) to study spatial clustering and whether seismic activity forms topological voids or ring-like structures.

### **5. NOAA CO₂ Monthly Records (Mauna Loa Observatory)**  
Dataset: [Mauna Loa CO₂ Monthly Data](https://gml.noaa.gov/ccgg/trends/data.html)  
**Description:**  
A historic climate dataset containing monthly atmospheric CO₂ measurements collected continuously since 1958.  
**Project Idea:**  
Apply time-delay embeddings to the CO₂ time series and compute persistent homology to reveal seasonal oscillations and long-term trends. Expect a strong persistent H₁ loop corresponding to annual CO₂ cycles.

---

## Where’s Schueller?

Below are my embedded, “live” Plotly visualizations from the *Where’s Schueller?* assignment.  
These figures display real-world geolocation trajectories and derived summaries, and are fully interactive on this webpage.

### Interactive Travel Map

<iframe
    src="schueller_plot.html"
    width="100%"
    height="600"
    frameborder="0">
</iframe>

### Annual Total Distance Traveled

<iframe
    src="annual_distance_traveled.html"
    width="100%"
    height="500"
    frameborder="0">
</iframe>

### Transport Mode Distribution by Time Period

<iframe
    src="transport_mode_distribution.html"
    width="100%"
    height="500"
    frameborder="0">
</iframe>

---

## Above & Beyond: Simple Topological Data Analysis (TDA)

For my above-and-beyond component, I am incorporating **Topological Data Analysis (TDA)**, a modern technique from applied topology that studies the “shape” of data. TDA is not part of the standard data science curriculum, but it offers powerful insights into geometric and structural patterns across many types of datasets.

For the final project, I plan to use one of the datasets above to demonstrate:

- **Slide-window embeddings on time series** to reveal periodic structure  
- **Persistent homology** (H₀ and H₁) to detect clusters or loops  
- **Persistence diagrams and barcodes** to visualize topological features  
- **Interpretation of these features** in terms of climate cycles, human motion, GPS loops, or seismic patterns  

This connects my mathematical background to data science and demonstrates a method that goes beyond classical statistical analysis.
