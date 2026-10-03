# Sports League Database Design
**MySQL Workbench | Academic Project | George Mason University**

## Overview
Designed a five-table relational database model to organize sports league seasons, divisions, clubs, teams, and registrations. Completed for IT 214, this project demonstrates relational modeling, composite keys, and data integrity constraints.

## Database Structure

| Table | Purpose |
|---|---|
| SEASON_DA | Stores seasons and associated dates |
| DIVISION_DA | Defines divisions within each season |
| CLUB_DA | Stores club identification and contact information |
| TEAM_DA | Stores teams and their club affiliations |
| REGISTRATION_DA | Associates teams with seasonal divisions |

## Key Design Decisions
- **Season-specific divisions:** A composite primary key `(DIVISION_ID_DA, SEASON_ID_DA)` identifies each division within its season.
- **Registration limits:** The registration primary key `(TEAM_ID_DA, SEASON_ID_DA)` limits each team to one registration per season.
- **Consistent references:** Registrations use a composite foreign key to reference the correct division and season combination.
- **Duplicate restrictions:** Unique constraints define rules for season name/year combinations, club abbreviations, and team names within clubs.
- **Required data:** NOT NULL settings identify mandatory attributes, while data types define the values each field can store.

## View the Model
Download `D3_Acquaye_Deron.mwb` and open it in MySQL Workbench. Use the EER diagram to inspect relationships and the table editors to review columns, indexes, and foreign keys.

## Project Status
The database model is complete. SQL execution, sample data, query results, and constraint testing are not yet documented in this repository.

## Author
Deron Acquaye  
IT 214 — Module 6 D3 Design Assignment  
George Mason University
