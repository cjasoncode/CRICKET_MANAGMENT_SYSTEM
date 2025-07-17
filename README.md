 
# 🏏 Cricket Management System (MySQL)

**"Cricket Meets SQL – A Perfect Partnership!"**  
A complete **Cricket Tournament Management System** built using **MySQL**, featuring IPL-style data, strong relationships, and advanced SQL queries.

---

## 📌 Project Overview
Cricket Management System is designed to **manage and analyze cricket tournament data**. It covers details like teams, players, matches, auctions, and statistics, inspired by **IPL 2025** format.

This project demonstrates:
✔ Database **Normalization**
✔ Proper **Primary & Foreign Key Relationships**
✔ Real-life **SQL Query Implementations**

---

 
## ✅ Features
✔ **9 Interconnected Tables** for Teams, Players, Matches, Auctions, and more  
✔ **Primary & Foreign Keys**, Constraints  
✔ **20+ Analytical Queries** for:  
   - Match Schedules & Results  
   - Player Performance Analysis  
   - Points Table Standings  
   - Auction Details  

---

## 🏗 Database Schema
**Core Tables:**  
`TOURNAMENT | TEAMS | PLAYERS | VENUE | MATCHES | FINAL_MATCH | POINTS_TABLE | PLAYER_STATS | AUCTION`

---

## 💡 Tech Stack
- **Database:** MySQL  
- **Tools:** MySQL Workbench  

---

## 📂 Project Structure
📦 Cricket_Management_System/
│
├── 📄 CRICKET_MANAGEMENT_SYSTEM.sql # Complete Database Creation Script (Tables + Constraints + Sample Data)
├── 📄 Queries.sql # Collection of 20+ Analytical SQL Queries
└── 🖼 ER_Diagram.png # Entity-Relationship Diagram (Visual Representation of Tables & Relationships)

 
---

## 📸 Visual Diagram  
![ER Diagram](MAIN.SQL\ER_DIAGRAM.png)  

---

## 🔍 Sample Queries
  

### ✅ 1. List all teams

```sql
SELECT TEAM_NAME FROM TEAMS;
```

### ✅ 2. Players with more than 200 runs
```sql
SELECT PLAYERS.PLAYER_NAME, PLAYER_STATS.RUNS
FROM PLAYERS
JOIN PLAYER_STATS ON PLAYERS.PLAYER_ID = PLAYER_STATS.PLAYER_ID
WHERE PLAYER_STATS.RUNS > 200;
```

### ✅ 3. Final match details
```sql
SELECT
 FINAL_A.TEAM_NAME AS TEAM_A,
 FINAL_B.TEAM_NAME AS TEAM_B,
 VENUE.VENUE_NAME AS VENUE,
 CHAMPION.TEAM_NAME AS WINNER
FROM FINAL_MATCH
JOIN TEAMS AS FINAL_A ON FINAL_MATCH.FINALTEAM_A = FINAL_A.TEAM_ID
JOIN TEAMS AS FINAL_B ON FINAL_MATCH.FINALTEAM_B = FINAL_B.TEAM_ID
JOIN VENUE ON FINAL_MATCH.VENUE_ID = VENUE.VENUE_ID
JOIN TEAMS AS CHAMPION ON FINAL_MATCH.CHAMPION_TEAM = CHAMPION.TEAM_ID;
```


## 🤝 Contributors
* 👤 [cjasoncode](https://github.com/cjasoncode)
* 👤 [Ogvishesh](https://github.com/Ogvishesh)

---

 

## 🚀 How to Run

1. **Install MySQL and MySQL Workbench**.

2. **Create the database**:

```sql
CREATE DATABASE CRICKET_MANAGMENT_SYSTEM;
```

3. **Import** `CRICKET_MANAGEMENT_SYSTEM.sql`.

4. **Run queries** from `Queries.sql`.



