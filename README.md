**This repository acts as a supplement to my work for CS 725 - Independent Study**

# Project Overview

## Title: Analysis of Physiological Responses in League of Legends Players

### Project Advisor: Dr Kasthuri Jayarajah

![image](https://github.com/narenkhatwani/sensor-data-process-gaming-data/assets/48763124/c9bc2525-7b91-4f49-876a-6c1c2c926903)

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


### Understanding the Game: League of Legends
In the game League of Legends, defeating opponents, often referred to as securing a "kill," involves a combination of strategy, skill, and timing. There isn't an instant-kill mechanic as every champion (character) in the game has a health bar that needs to be depleted for them to be defeated. Here's a simplified explanation of how a player can kill an opponent in the game:

- Understanding Champion Abilities: Each champion in League of Legends comes with a unique set of abilities, which include basic attacks and four special skills (three basic abilities and one ultimate ability).
- Effective Use of Combos: Skilled players learn to chain their champion’s abilities in quick succession to maximize damage.
- Confidence and Decision-Making: Effective players gauge when they're in a strong position to secure a kill, understanding their own strength relative to the opponent's. 
- Execution: Once everything is lined up—the player knows their champion’s combos, understands both champions' strengths and weaknesses, and senses an opportunity—they execute their plan. 

**Confidence plays a key role here; a player who hesitates often misses the narrow window of opportunity to take down the opponent.**

This is how we tried visualizing Galvanic Skin Response Data (GSR) and Heart Rate Sensor Data (HR) from the data available at https://github.com/smerdov/eSports_Sensors_Dataset

### Significance of Sensors:
**Galvanic Skin Response Data (GSR)**




**Heart Rate Sensor (HR):**


### Explanations
#### Initial Visualizations:
Here, below as we can see 
![Image_1](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/1.png?raw=true)
#### GSR Phasic and Tonic Components' Data Visualization
**Tonic Component Graph:** By examining the trend in the tonic component, you can assess how the participant's baseline arousal level changes over time. An increasing trend might suggest growing tension or stress, while a decreasing trend could indicate relaxation.

**Phasic Component Graph:** Looking at the peaks in the phasic component can help you identify moments of acute response. The presence, frequency, and magnitude of these peaks can be linked back to specific events, offering insights into the participant's reactions.

![Image_2](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/2.png?raw=true)
#### Associating Kills and Assists with the tonic and Phasic Component of GSR
![Image_3](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/3.png?raw=true)
#### Scaling to see the results/ eyeballing the results of kill events
![Image_4](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/4.png?raw=true)
![Image_5](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/5.png?raw=true)
#### FOrmat of Final Results
![Image_6](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/6.png?raw=true)


The following graph visualizes the above dataframes which consist of the kill events with the physiological sensors' data 

##### Player 9
![Image_7](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/7.png?raw=true)
##### Player 6
![Image_8](https://github.com/narenkhatwani/analysis-of-physiological-responses/blob/main/pictures/8.png?raw=true)

### Results

For each player and match, the analysis generates:
- Average counts of GSR dips and HR peaks during kills vs. baseline periods.
- P-values from the t-tests to determine if the differences observed are statistically significant.

Results are aggregated across all matches and stored in a comprehensive data frame, allowing for easy access and further analysis.

### Significance

The findings can provide insights into players' ______ and help develop strategies to enhance gaming performance. Additionally, understanding physiological responses can aid in the design of more engaging and balanced game environments.
