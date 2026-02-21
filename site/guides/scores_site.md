# Scores Site Instructions


## Database

### Set up database

### Permissions

### Create Tables

These are the queries used to create the tables in the database:

```sql
	CREATE TABLE leagues (
		  league_id INT UNSIGNED NOT NULL AUTO_INCREMENT,
		  sport ENUM('soccer','american_football','baseball','basketball','cricket') NOT NULL,
		  league_name VARCHAR(120) NOT NULL,
		  country VARCHAR(80) NULL,
		  level VARCHAR(50) NULL,
		  is_active TINYINT(1) NOT NULL DEFAULT 1,
		  PRIMARY KEY (league_id),
		  UNIQUE KEY uq_league (sport, league_name)
		) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

```sql
 CREATE TABLE teams (
  team_id INT UNSIGNED NOT NULL AUTO_INCREMENT,
  sport ENUM('soccer','american_football','baseball','basketball','cricket') NOT NULL,
  team_name VARCHAR(120) NOT NULL,
  short_name VARCHAR(40) NULL,
  country VARCHAR(80) NULL,
  is_active TINYINT(1) NOT NULL DEFAULT 1,
  PRIMARY KEY (team_id),
  KEY idx_team_sport (sport, team_name)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```

```sql
CREATE TABLE user_follows (
  follow_id INT UNSIGNED NOT NULL AUTO_INCREMENT,
  follow_type ENUM('team','league') NOT NULL,
  team_id INT UNSIGNED NULL,
  league_id INT UNSIGNED NULL,
  PRIMARY KEY (follow_id),
  UNIQUE KEY uq_follow_team (follow_type, team_id),
  UNIQUE KEY uq_follow_league (follow_type, league_id),
  CONSTRAINT fk_follow_team FOREIGN KEY (team_id) REFERENCES teams(team_id),
  CONSTRAINT fk_follow_league FOREIGN KEY (league_id) REFERENCES leagues(league_id)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4;
```
