# Project Overview

## Title: Analysis of Physiological Responses in League of Legends Players

This project works on players' physiological responses during League of Legends matches, specifically focusing on how intense gaming moments, such as kills, influence players' stress levels. By measuring Galvanic Skin Response (GSR) and heart rate variations, we find patterns that might indicate heightened emotional or cognitive stress during gameplay.

### Objective

The main goal is to determine if and how significant gaming events correlate with measurable changes in physiological metrics, potentially affecting player performance and overall gaming experience.

### Methods

1. **Data Collection**: Data is sourced from augmented match files, including each player's time-stamped kill events and corresponding physiological data (GSR and heart rate).

2. **Data Processing**:
   - **Segmentation**: 
   - **Signal Processing**: 

3. **Statistical Analysis**:
   - **Peak Detection**: Using the `scipy.signal.find_peaks` method, heart rate peaks, and GSR dips are identified for both kill and baseline segments.
   - **t-Test**: To assess statistical significance, a two-sample t-test is applied to compare the mean counts of GSR dips and HR peaks between kill and baseline segments.

### Results

For each player and match, the analysis generates:
- Average counts of GSR dips and HR peaks during kills vs. baseline periods.
- P-values from the t-tests to determine if the differences observed are statistically significant.

Results are aggregated across all matches and stored in a comprehensive data frame, allowing for easy access and further analysis.

### Significance

The findings can provide insights into players' stress management capabilities and help develop strategies to enhance gaming performance. Additionally, understanding physiological responses can aid in the design of more engaging and balanced game environments.
