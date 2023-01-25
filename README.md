# <p align="center"> <ins>ETL Project 2</ins>
# <p align="center"> :soccer: FIFA 2022 :soccer:

 ![Screen Shot 2023-01-25 at 22 37 55](https://user-images.githubusercontent.com/116304118/214707931-5c826886-1e19-40ce-9a84-8e78eea2c0f2.png)




## <ins>Project Proposal</ins>

The project focuses on the FIFA World Cup 2022 data. With 32 teams from around the world competing for the coveted trophy, the excitement and energy of this global event is palpable. This series of dataset captures some of the action, from player statistics and team standings, to game scores and match performances.

With this FIFA World Cup 2022 dataset, the possibilities are endless. Don't miss out on the opportunity to be a part of the action and join the ranks of the world's top data analysts. Grab your dataset today and let the games begin!

The data transformation process will be performed using Jupyter Notebook, and then be loaded into a PostgreSQL database preparing the data for further analysis to be performed.
The chosen dataset’s have been extracted from three different sources of data: groups statitics data, team data and team tips data.

## Goal of our project
The goal of this project was to find out: 
* Top 5 teams that played the most minutes
* The top 5 teams that took penalties
* Top 5 teams that had the most yellow and red cards
* Top 5 teams with the most goals

## Sources of Data
Our dataset contains two CSV files and a JSON file, available from Kaggle.com.
* team data
* group stats
* team tips (JSON) 

## Data Extraction
Three files are selected from Kaggle.com and converted to panda DataFrames.

The Dataframes are named as team_data_new and new_team_tips. Both csv files were merged in order to create the team_data_new panda DtaFrame. (insert picture of the code to merge and picture of dataframe after merged)

## Transformation
After looking through the data, the data was cleaned. This is where coloumns needed were selected and another DataFrame was generated. (insert picture of code and dataframe)

## Loading of the Data
‘pgAdmin 4’ was used to create PostgreSQL tables that included the headers from the dataframe. See images below.

![Screen Shot 2023-01-25 at 19 58 30](https://user-images.githubusercontent.com/116304118/214709587-e96a53c9-768f-4630-a491-a38e3e4f08ba.png)

![Screen Shot 2023-01-25 at 19 58 40](https://user-images.githubusercontent.com/116304118/214709679-4b0aecae-e358-44bf-aca3-7c531e0d0580.png)


