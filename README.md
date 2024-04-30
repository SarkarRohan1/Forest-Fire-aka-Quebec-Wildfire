# Forest-Fire-aka-Quebec-Wildfire
Capstone project for the Erdos Fall 2023 Data Science Bootcamp 

**Team members**
1. Christopher Mahadeo
2. Murat Uyar
3. Nihal Uyar
4. Rohan Sarkar

### Data data everywhere, not a sense to it
Well, here it is now

- The weather data is available here: https://climatedata.ca/download/#station-download
- The wildfire data is available here: https://www.kaggle.com/datasets/ulasozdemir/wildfires-in-canada-19502021/data
- For the notebook 'wildfire_modeling' use dataset 'fire_0_df.csv', 'fire_1_df.csv'
- For the notebook 'haversinedistance' use datasets 'climatetotalcoord1.csv'
- Relevant csv files required to run notebooks are provided in the relevant folders

### My contribution
I merged all the weather datasets and the wildfire dataset together. This was based on the common coordinates. Then I selected for the wildfires in the Quebec region and lightning-caused fires. Since there were multiple weather stations reporting individual fires, I created a unique "fire- nearest weather station" pair calculated through the haversine distance. I wrote a function to convert the latitudes and longitudes into radians and then calculating the distance. Subsequently data for the past 15 days prior to the wildfire for each of these unique weather stations were added to create a new dataframe. I created another dataframe containing weather details from these same weather stations on days of no wildfire, chosen randomly. Other cleaning procedures like dropping duplicate columns, imputing or removing missing values and generalising syntax and font throughout the entire dataframes were also performed.
