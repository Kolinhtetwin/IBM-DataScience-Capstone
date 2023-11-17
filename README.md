# SpaceX Rocket Analysis Project

This is final Capstone project for IBM Data Science Professional Certificate.

## Description
The commercial space age is here, companies are making space travel affordable for everyone. Virgin Galactic is providing suborbital spaceflights. Rocket Lab is a small satellite provider. Blue Origin manufactures sub-orbital and orbital reusable rockets. Perhaps the most successful is SpaceX. SpaceX’s accomplishments include: Sending spacecraft to the International Space Station. Starlink, a satellite internet constellation providing satellite Internet access. Sending manned missions to Space. One reason SpaceX can do this is the rocket launches are relatively inexpensive. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upwards of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. 
In this capstone project, I will take the role of a data scientist working for a new rocket company. Space Y that would like to compete with SpaceX founded by Billionaire industrialist Allon Musk. My job is to determine the price of each launch. I will do this by gathering information about Space X and creating dashboards for my team. I also determine if SpaceX will reuse the first stage. Instead of using rocket science to determine if the first stage will land successfully, I train a machine learning model and use public information to predict if SpaceX will reuse the first stage.

## Table of Contents
- [Methodology](#methodology)
- [Project Workflow](#project)
- [Result](#result)
- [Author](#author)
- [Acknowledgement](#acknow)

## Methodology <a name="methodology"></a>
- Data collection with api and webscraping 
- Data Wrangling
- Exploratory Data Analysis using SQL
- EDA Data Visualization Using Python Pandas and Matplotlib
- Launch Sites Analysis with Folium-Interactive Visual Analytics and PlotyDash
- Machine Learning Landing Prediction

Required important libraries
- pandas
- numpy
- request
- datetime
- foilum
- plotly
  
Programming Language 
- Python

## Project workflow <a name="project"></a>
### Data collection with api 
  In this stage, I collected the data from the API provided by SpaceX REST API. The data from API only give you the id version and I apply the function to get the information I want. You can check the code inside this link. [Data collection with api](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/Data%20collection%20with%20api.ipynb)

### Data wrangling
In this part, I try to understand the features and label of the dataset and determine what would be the feature for training the supervised models. In the dataset, there are serveral cases where the booster did not land successfully. Sometimes, a landing was attempted but failed due to an accident. In this part, I convert these outcomes into Training labels with 0(which means fail) and 1(which means successful landing).
[Data wrangling](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/Data%20collection%20with%20api.ipynb)

### Exploratory Data Analysis using SQL
In this part, I try to see the lot of different thing that offered by the dataset using SQL query. 
[Exploratory Data Analysis using SQL](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/EDA%20with%20sqlite.ipynb)

### EDA Data Visualization
In this part, I try to see the relationship between the different features and outcome and how they affect. 
[EDA Data Visualization](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/Exploratory%20Data%20Analysis%20with%20Data%20Visualization.ipynb)

### Launch Sites Analysis with folium-map
In this part, I find some geographical patterns about launch sites.[Folium Map](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/folium%20lab.ipynb)

###  Launch Sites Analysis with ploty dash
In this part, I build the interactive dashboard for my team to see which sites and payload mass has affected the success rate. [Plotly dash](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/spacex_dash_app.py)

### Machine Learning Prediction
In this step, I create a machine learning to predict if the first stage will land given the data from the preceding labs. [Machine Learning](https://github.com/Kolinhtetwin/IBM-DataScience-Capstone/blob/3d6bc14f6688ee07d0407c1282e3f7099e21d928/Machine%20Learning.ipynb)

## Result <a name= "result"></a>
SpaceX uses four different launch sites which are all near the coast line. The launch sites are near the railway and highway that makes it easier for transporation but far away from the city which make a safe environment.
The successful rate for landing has been increased steadily from 2013 and get the highest success rate at 2019, reaching 90%. The first successful landing in ground pad was achieved at 2015. As the time increases, the success rate for landing has been increased which means SpaceX has been improving their landing from time to time. 
Mission Outcome for F9 version is incredible with almost 100%. In terms of four different launch sites, KSC LC-39A has the highest success rate with 41.7%.
Also KSC LC-39C has 100 percentage success rate for low payload mass between 0kg and 5000 kg.
Interestingly, for high payload mass between 5000kg and 10000kg, it didn’t have achieved no success at all.
For machine learning, the four models produce relatively similar result due to relatively small dataset. In four of them, the decision tree model has lowest test accuracy. For using the model, I choose Logistic Regression to predict the successful landings because it never miss the successful landing and can increase profit by reusing the first stage again.

## Author <a name="author"></a>
Lin Htet Win

## Acknowledgements <a name="acknow"></a>
##### © Copyright IBM Corporation 1994, 2021.


