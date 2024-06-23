# World Cup Database
This repository contains a PostgreSQL database that stores FIFA World Cup match results, along with Bash scripts for manipulating and querying this database.

## Repository Contents

1. worldcup.sql: This file contains the PostgreSQL database dump including the database structure, table definitions, and pre-inserted data of World Cup matches and teams.

2. populate_db.sh: A Bash script designed to populate the database with FIFA World Cup match data. The script reads data from a CSV file (games.csv) and inserts it into corresponding tables (games and teams) in the PostgreSQL database.

3. queries.sh: A Bash script that executes various SQL queries on the database to extract specific statistics and data from FIFA World Cup matches. Queries include calculations such as total goals, averages, winning teams, and more.

## Usage
### Prerequisites
To run these scripts, make sure you have PostgreSQL installed and have access to a database named worldcup. Adjust connection variables in the scripts if necessary.

### Execution
1. Importing the Database:
```sh
psql --username=your_username --dbname=worldcup < worldcup.sql
```
*You should have execution permits*
```sh
ch mod +x <file>
```

2. Populating the Database:
```sh
./populate_db.sh
```

3. Queries and Analysis:
```sh
./queries.sh
```

## Database Details
The database includes the following key tables and fields:

Table games:
- game_id: Unique identifier of the match.
- year: Year of the match.
- round: Stage of the tournament.
- winner_id: ID of the winning team.
- opponent_id: ID of the opposing team.
- winner_goals: Goals scored by the winning team.
- opponent_goals: Goals scored by the opposing team.

Table teams:
- team_id: Unique identifier of the team.
- name: Name of the team.

## Contributions
Feel free to contribute to this repository by improving scripts, adding additional queries, or expanding the database with more historical FIFA World Cup data.