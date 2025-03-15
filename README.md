# Big-Data-Analysis-with-Hadoop-MapReduce

## Overview
This project implements **Hadoop MapReduce** to analyze the IMDb Top 1000 dataset, exploring the impact of directors and top-billed actors on a film's success. By utilizing the MapReduce framework, the project processes large-scale movie data in a distributed manner, extracting key insights into average IMDb ratings and gross earnings for directors and actors.

## Research Objective
- **Question**: How do top-billed actors and directors affect a film's success, measured by IMDb ratings and gross earnings?
- The study aims to support the film industry with data-driven insights for better decision-making in casting, direction, and production strategies.

## Key Components
### Dataset
- **Source**: [IMDb Top 1000 Movies Dataset on Kaggle](https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows)
- **Key Attributes**: 
  - `Director`, `Star1`, `IMDb_Rating`, `Gross` (primary focus)
  - `Star2`, `Star3`, `Star4` (additional actors)
  - Includes other metadata like runtime, genre, etc.

### MapReduce Design
The project employs four key components:
1. **Mapper_Director**:
   - Extracts director names, IMDb ratings, and gross earnings.
   - Outputs key-value pairs of directors and their respective data.

2. **Reducer_Director**:
   - Aggregates data by director, calculating the average IMDb rating and gross earnings.
   - Outputs directors ranked by critical and commercial performance.

3. **Mapper_Actor**:
   - Extracts actor names, IMDb ratings, and gross earnings.
   - Outputs key-value pairs of actors and their respective data.

4. **Reducer_Actor**:
   - Aggregates data by actor, calculating the average IMDb rating and gross earnings.
   - Outputs actors ranked by critical and commercial success.

### Hadoop Framework Setup
- Configured the Hadoop environment on Google Colab using virtual Linux machines.
- Installed dependencies, set up Java SDK, and added Hadoop libraries to the PATH for execution.

## Results
### Directors
- **Top by IMDb Ratings**: Tim Robbins, Elijah Wood, John Travolta.
- **Top by Gross Earnings**: Daisy Ridley, Sam Worthington, Joe Russo.

### Actors
- **Top by IMDb Ratings**: Bob Gunton, Aaron Eckhart, William Sadler.
- **Top by Gross Earnings**: Daisy Ridley, John Boyega, Michelle Rodriguez.

### Insights
- Directors with high critical acclaim are not always the most commercially successful.
- Actors like Daisy Ridley dominate both critical and commercial metrics.

## Conclusions
- Focus on high-rated directors for critically acclaimed films (e.g., Tim Robbins).
- Leverage the commercial success of directors and actors with high gross earnings (e.g., Daisy Ridley).
- Strategic casting and directing choices can significantly impact box office success.

## Future Enhancements
- Explore the impact of actor-director combinations on movie performance.
- Extend the analysis to include other variables like genre and runtime.
- Implement real-time data processing pipelines for streaming movie datasets.

## References
- Dean, J. and Ghemawat, S. "MapReduce: Simplified Data Processing on Large Clusters."
- Padhy, R.P. "Big Data Processing with Hadoop-MapReduce in Cloud Systems."
- Hashem, I.A.T., et al. "MapReduce: Review and open challenges." Scientometrics, 2016.

