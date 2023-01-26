# <p align="center"> <ins>ETL Project 2</ins>
# <p align="center"> :soccer: FIFA 2022 :soccer:

 ![Screen Shot 2023-01-25 at 22 37 55](https://user-images.githubusercontent.com/116304118/214707931-5c826886-1e19-40ce-9a84-8e78eea2c0f2.png)




## <ins>Project Proposal</ins>

The project focuses on the FIFA World Cup 2022 data. With 32 teams from around the world competing for the coveted trophy, the excitement and energy of this global event is palpable. This series of dataset captures some of the action, from player statistics and team standings, to game scores and match performances.

With this FIFA World Cup 2022 dataset, the possibilities are endless. Don't miss out on the opportunity to be a part of the action and join the ranks of the world's top data analysts. Grab your dataset today and let the games begin!

The data transformation process will be performed using Jupyter Notebook, and then be loaded into a PostgreSQL database preparing the data for further analysis to be performed.
The chosen dataset’s have been extracted from three different sources of data: groups statitics data, team data and team tips data.
The full code can be viewed here. <a href="https://github.com/HJandu/ETL_Project_2/blob/main/Fifa_project2.ipynb">Click here</a>  </br>

## <ins>Goal of our project</ins>
The goal of this project was to find out: 
* Top 5 teams that played the most minutes
* The top 5 teams that took penalties
* Top 5 teams that had the most yellow and red cards
* Top 5 teams with the most goals

## <ins>Sources of Data</ins>
Our dataset contains two CSV files and a JSON file, available from Kaggle.com.
* <a href="https://github.com/HJandu/ETL_Project_2/blob/main/Resources/team_data.csv">Team Data</a>  </br>
* <a href="https://github.com/HJandu/ETL_Project_2/blob/main/Resources/group_stats.csv">Group Stats</a>  </br>
* <a href="https://github.com/HJandu/ETL_Project_2/blob/main/Resources/team_tips.json">Team tips (JSON)</a>  </br> 


## <ins>Data Extraction</ins>
Three files are selected from Kaggle.com and converted to panda DataFrames.

The Dataframes are named as team_data_new and new_team_tips. Both csv files were merged in order to create the team_data_new Panda DataFrame. 

![Screen Shot 2023-01-26 at 17 43 47](https://user-images.githubusercontent.com/116304118/214910190-cba99eed-18f8-4c60-89c8-824cc751f56c.png)
![Screen Shot 2023-01-26 at 17 44 07](https://user-images.githubusercontent.com/116304118/214910244-2d7cee38-e5df-4837-b953-57bf596bd34a.png)

## <ins>Transformation</ins>
After looking through the data, the data was cleaned. This is where columns needed were selected and another DataFrame was generated. 

![Screen Shot 2023-01-26 at 17 44 07](https://user-images.githubusercontent.com/116304118/214911741-057b7712-7829-4963-ae03-076838dcccce.png)

Columns were also renamed, before loading the data to PostgreSQL. See image below. 
![Screen Shot 2023-01-26 at 17 55 32](https://user-images.githubusercontent.com/116304118/214912287-327d1d23-b7de-4d2c-bc73-0dae94c7a613.png)


## <ins>Loading of the Data</ins>
Data was then loaded into a relational database for storage. ‘pgAdmin 4’ was used to create PostgreSQL tables that included the headers from the dataframe. See images below.

![Screen Shot 2023-01-25 at 19 58 30](https://user-images.githubusercontent.com/116304118/214709587-e96a53c9-768f-4630-a491-a38e3e4f08ba.png)

![Screen Shot 2023-01-25 at 19 58 40](https://user-images.githubusercontent.com/116304118/214709679-4b0aecae-e358-44bf-aca3-7c531e0d0580.png)

Data was loaded successfully onto PostgreSQL. See image of output below.

![Screen Shot 2023-01-26 at 19 41 06](https://user-images.githubusercontent.com/116304118/214934466-0a170e90-52bb-4935-b084-fc171a333698.png)

Once the data was loaded, we downloaded the CSV files. You can find the csv files by clicking the links below.
* <a href="https://github.com/HJandu/ETL_Project_2/blob/main/Description_PGAdmin.csv">Description</a>  </br>
* <a href="https://github.com/HJandu/ETL_Project_2/blob/main/teams_PGAdmin.csv">Teams</a>  </br>

## <ins>Summary of our findings</ins>
Using the aggregate method, we were able to create Pandas DataFrames for our query questions. 
We then created tables in PGAdmin.

![Screen Shot 2023-01-26 at 22 56 45](https://user-images.githubusercontent.com/116304118/214971416-e8e37ab4-5a44-4d99-ad84-8efa7cdcaa1f.png)



The DataFrames were first created on Jupyter notebook and then uploaded onto PostgreSQL (PGAdmin). 
See images of the code and the tables for each query below.

#### Top 5 teams that played the most minutes

![Screen Shot 2023-01-26 at 23 14 29](https://user-images.githubusercontent.com/116304118/214971766-1aef358e-229f-47be-9e70-576fd6d58ca6.png)

![Screen Shot 2023-01-26 at 22 45 47](https://user-images.githubusercontent.com/116304118/214971623-09ec7d59-8986-45e2-a5a9-bf03d91cdb69.png)

![Screen Shot 2023-01-26 at 17 57 26](https://user-images.githubusercontent.com/116304118/214913122-4dbaf3a3-b103-4d82-b335-4d21b42e9fe8.png)

Based on the findings, we can see that Argentina took the lead in playing the most minutes (690 minutes) and Brazil coming in fifth in playing the most minutes (480 minutes).

#### The top 5 teams that took penalties

![Screen Shot 2023-01-26 at 23 16 33](https://user-images.githubusercontent.com/116304118/214971972-aa541f25-2350-427c-b645-491b01a03429.png)


![Screen Shot 2023-01-26 at 22 58 45](https://user-images.githubusercontent.com/116304118/214971899-e9628069-05c1-411c-9802-0efec3d9e7a4.png)


![Screen Shot 2023-01-26 at 17 57 39](https://user-images.githubusercontent.com/116304118/214913268-b1486ae9-7a20-4c9f-a4d9-0b0ef6a8eef2.png)

Based on the findings Argentina took the most penalities and scored (4) and joint 4th were Ecuador and Spain (1)


#### Top 5 teams that had the most yellow and red cards
![Screen Shot 2023-01-26 at 23 17 37](https://user-images.githubusercontent.com/116304118/214972081-83e3e28d-01f7-43ca-afd3-8a5406b97d2b.png)

![Screen Shot 2023-01-26 at 22 59 15](https://user-images.githubusercontent.com/116304118/214972152-ef0a079a-debd-48fe-a470-0ceefab2a2aa.png)


![Screen Shot 2023-01-26 at 17 57 53](https://user-images.githubusercontent.com/116304118/214913309-daec10ed-5d2e-41d4-9ac7-6f950ef2b369.png)

Based on the findings, Netherlands were the only team who were given both yellow and red cards.

#### Top 5 teams with the most goals

![Screen Shot 2023-01-26 at 23 19 01](https://user-images.githubusercontent.com/116304118/214972255-af1bb640-c2f6-4a2f-a1bc-8d66d9147cb3.png)


![Screen Shot 2023-01-26 at 22 58 02](https://user-images.githubusercontent.com/116304118/214972208-ddace3cd-31c9-4012-b233-629335cc1d28.png)


![Screen Shot 2023-01-26 at 17 58 28](https://user-images.githubusercontent.com/116304118/214913361-dc3e03be-2f8e-4636-8452-4c3bfa4faf0f.png)

Based on the findings, all 5 teams had a higher turnout in scoring 'Goals' than they did in taking 'Non-Penality Goals'.
