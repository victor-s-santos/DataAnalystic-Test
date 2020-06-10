<table>
   <tr>
      <p align="center">
        <a href="#about">About</a> •
        <a href="#how_to_run">How to run</a> •
        <a href="#populating_the_database">Populating the database</a> •
         <a href="#jupyter_notebooks">Jupyter Notebooks</a> •
         <a href="#observed_correlations">Observed Correlations</a> •
      </p>
   </tr>
</table>

# About
> This is a repository where I am apllying to Gamers Club Data Analystic Test. Here I am going to show how I UP the database, how I analysed the charts using python, show the results (more charts) and discuss about it. In this repo I am trying to understand why much people leave the Game course after watch a few classes and look for a way to solve this.  
The database credentials has been omitted. 

# How_to_run
> To run this repository, follow the steps:
1. Create a virtualenv (this isn't necessary, but I belive this is a good practic):
    * python3 -m venv .venv `to create a virtualenv`
    * source .venv/bin/activate `to use this virtualenv`
    
2. Clone this repository:
    * git clone https://github.com/victor-s-santos/DataAnalystic-Test.git

3. Install the dependencies:
   * pip install ipython[notebook] `to install jupyter notebook`
   * pip install python-dotenv `to install dotenv`
   * pip install pymysql `to install this pure-Python MySQL client library`

   3.1 Graph dependencies:
      * pip install matplotlib
      * pip install seaborn
   
4. Open python notebook:
    * ipython notebook
    
5. To see a Database manager:
    * Adminer
    sudo docker run \
        --name adminer \
        -p 8080:8080 \
        -d \
        adminer

now you can see your database by accessing:
http://localhost:8080/

# Populating_the_database
>To populate this database to analyse the values, relations etc you need to use Adminer: 
1. With Adimer running, go to:
    http://localhost:8080/, and follow the steps above:
    
    1.1 ![adminer](/images/adminer/adminer.png)
    Enter with your credentials(in this case, I am using a remote database from remotemysql.com)
    
    1.2 ![informations_database](/images/adminer/informations_database.png)
    Look to the database structure.
    
    1.3 ![inserting_players](/images/adminer/inserting_players.png)
    The easiest way to populate the data base. The another is just run by python.
  
2.With jupyter notebook:

   2.1 ![inserting_by_python](/images/adminer/inserting_by_python.png)
   This way is going to waste much more than the previous way, because we have much data amount.
   
   or
   
   2.2 ![inserting_full_data](/images/adminer/insert_full_data.png)
   This way is going to waste much time, as the 2.1, but in this case you are going to execute a single line*.
   But, if you are using a free account, it might be necessary to use the 2.1 way, because in this case, your connection with remotemysql.com are going to break in less time than the necessary time to finish python execution.
   

# Jupyter_Notebooks
>To describe what are the reason of each jupyter notebook in this repo:
1. DDL.ipynb:
>This notebook is used to create the database structure executing SQL statment in python.

2. pre-processing.ipynb:
>This notebook is used to do the pre-processing in the sql file, to manually export a csv where I can use the correlation pandas feature.

3. Analysis.ipynb:
>This notebook is used to do the data analysis, even in the remote mysql table as the csv files, to mainly answer the questions in the test. In this notebook I argue about the correlation method to choose, and why.

4.Analysis2.ipynb:
>This notebook is where I analyse the players skills, and the growth in the number of accounts created.

# Observed_Correlations
>Here are some the images of the correlations:

## The correlation in the matchmaking_summary table:
![heatmap_chart_matchmakingsummary](/images/correlations/heatmap_spearman_matchmakingsummary.png)

## The correlation in the player_mounthly_stats table:
![heatmap_spearman_monthly](/images/correlations/heatmap_spearman_monthly.png)

# Trends noticed
>Here are the images of where trends are concluded

## Relation account_created x day:
![accountbydate](/images/charts/accountbydate.png)


## Relation account_created x month:
![accountbymonth](/images/charts/accountbymonth.png)
