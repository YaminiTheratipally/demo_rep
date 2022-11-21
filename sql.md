# Data Project - SQL 
## 1. Create DB, permissions etc.
      sudo -i -u  postgres
      psql
      create user yamini with password '1234';
      CREATE ROLE
      create database mydb;
      CREATE DATABASE
      grant all privileges on database mydb to yamini;
      GRANT
      \c mydb
      

## 2. Clean up script

      drop database if exists mydb;
      DROP DATABASE
      drop user yamini;
      DROP ROLE
      
## 3. Load CSV
       create table matches (id int, season int, city varchar(50), date date, team1 varchar(50),
					  team2 varchar(50),toss_winner varchar(50),toss_decision varchar(50),
					  result varchar(50), dl_applied int,winner varchar(50), win_by_runs int,
					  win_wickets int, player_of_match varchar(50), venue varchar(100),
                     umpire1 varchar(50),umpire2 varchar(50), umpire3 varchar(50));
                     
        \copy matches from '/home/admin-pc/Downloads/matches.csv' DELIMITER ',' CSV HEADER;              

       create table deliveries (match_id int, inning int, batting_team varchar(200), bowling_team varchar(200),
                        over int, ball int, batsman varchar(200), non_striker varchar(200),
                        bowler varchar(200),is_super_over int,wide_runs int,bye_runs int,legbye_runs int,
                        noball_runs int,penalty_runs int,batsman_runs int,extra_runs int,total_runs int,
                        player_dismissed varchar(200),dismissal_kind varchar(200),fielder varchar(200));
                                               
      \copy deliveries from '/home/admin-pc/Downloads/deliveries.csv' DELIMITER ',' CSV HEADER;
                  
                        
                        
## 4. Solve the IPL problems

### 1. Number of matches played per year of all the years in IPL.

      select season as Year, count(*) as Matches_Played from matches group by year order by season;

### 2. Number of matches won of all teams over all the years of IPL.

      select winner as team,count(*) as matches_won  from matches group by winner order by team;

### 3. For the year 2016 get the extra runs conceded per team.

      select bowling_team, sum(extra_runs) as total_extra_runs from deliveries  inner join matches on  deliveries.match_id = matches.id  where matches.season = 2016 Group by deliveries.bowling_team ; 
     
### 4. For the year 2015 get the top economical bowlers.

      select bowler,(sum(total_runs)/(count(bowler)/6)) as economical from deliveries  inner join matches on  deliveries.match_id = matches.id  where matches.season = 2015 group by deliveries.bowler order by economical;






