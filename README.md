<table>
   <tr>
      <p align="center">
        <a href="#about">About</a> •
        <a href="#how_to_run">How to run</a> •
        <a href="#populating_the_database">Populating the database</a> •
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
    * git clone https://github.com/victor-s-santos/Python-SQL.git

3. Install the dependencies:
   * pip install ipython[notebook] `to install jupyter notebook`
   * pip install python-dotenv `to install dotenv`
   * pip install pymysql `to install this pure-Python MySQL client library`

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
    
    1.1 ![adminer](/images/adminer.png)
    Enter with your credentials(in this case, I am using a remote database from remotemysql.com)
    
    1.2 ![informations_database](/images/informations_database.png)
    Look to the database structure.
    
    1.3 ![inserting_players](/images/inserting_players.png)
    The easiest way to populate the data base. The another is just run by python.
