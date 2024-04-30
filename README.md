# Forest-Fire-aka-Quebec-Wildfire
Capstone project for the Erdos Fall 2023 Data Science Bootcamp 

**Team members**
1. Christopher Mahadeo
2. Murat Uyar
3. Nihal Uyar
4. Rohan Sarkar

**Mentor**: 
Kenny Salau

### Data data everywhere, not a sense to it
Well, here it is now

- The weather data is available here: https://climatedata.ca/download/#station-download
- The wildfire data is available here: https://www.kaggle.com/datasets/ulasozdemir/wildfires-in-canada-19502021/data
- For the notebook 'wildfire_modeling' use dataset 'fire_0_df.csv', 'fire_1_df.csv'
- For the notebook 'haversinedistance' use datasets 'climatetotalcoord1.csv'
- Relevant csv files required to run notebooks are provided in the relevant folders

### My contribution
I merged all the weather datasets and the wildfire dataset together. This was based on the common coordinates. Then I selected for the wildfires in the Quebec region and lightning-caused fires. Since there were multiple weather stations reporting individual fires, I created a unique "fire- nearest weather station" pair calculated through the haversine distance. I wrote a function to convert the latitudes and longitudes into radians and then calculating the distance. Subsequently data for the past 15 days prior to the wildfire for each of these unique weather stations were added to create a new dataframe. I created another dataframe containing weather details from these same weather stations on days of no wildfire, chosen randomly. Other cleaning procedures like dropping duplicate columns, imputing or removing missing values and generalising syntax and font throughout the entire dataframes were also performed. The imputation strategy involved employing aggregation methods tailored to each variable, with mean aggregation for temperature-related features and pchip interpolation for max and min relative humidity. 

### Overall Project Details
In the data modeling process, the preliminary tests indicated the viability of decision tree, random forest, gradient boosting, logistic regression, k-nearest neighbors, support vector machine, and naive bayes models. Subsequent cross-validation and hyperparameter tuning revealed excellent performance for all tuned models, as depicted in a table of accuracy.

![image](https://github.com/SarkarRohan1/Forest-Fire-aka-Quebec-Wildfire/assets/82277560/e28a99a1-0b28-4609-8ce6-55894a03e597)


The analysis identifies data limitations, primarily stemming from the non-linear nature of meta-features, such as recent atmospheric conditions and lightning storm occurrences. The study uses aggregated weather data, emphasizing recent atmospheric conditions, and highlights the importance of a more robust dataset for improved predictions. Additionally, the investigation into feature importance shows that total precipitation ranks as the most influential factor in all models, contradicting expectations based on the dataset's structure.

![image](https://github.com/SarkarRohan1/Forest-Fire-aka-Quebec-Wildfire/assets/82277560/0fbd8ee7-f65c-49eb-a6af-5fa523b5628b)


The study underscores the promising capabilities of the selected models and encourages further research to refine predictions and address the complexities of wildfire forecasting.
