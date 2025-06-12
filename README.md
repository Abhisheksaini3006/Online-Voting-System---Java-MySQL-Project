# 🗳️ Online Voting System

This is a simple console-based Online Voting System built in Java using MySQL as the backend database. It allows users to register, log in, vote for a candidate, and view the voting results. The system ensures that each user can only vote once.

## ✨ Features

- User registration and login
- Vote casting for any candidate
- One vote per user restriction
- View total votes for each candidate
- MySQL database integration using JDBC

## 🔧 Technologies Used

- Java (JDK 8 or above)
- MySQL
- JDBC

## 📥 How to Set It Up

```bash
1. Clone this repository:
   git clone https://github.com/your-username/online-voting-system.git
   cd online-voting-system

2. Make sure MySQL is installed on your system.
   You can download it from https://dev.mysql.com/downloads/
   (Default username: root, use your own password during setup)

3. Open MySQL Workbench or terminal and run these SQL commands:
   CREATE DATABASE OnlineVotingSystem;

   USE OnlineVotingSystem;

   CREATE TABLE users (
       id INT AUTO_INCREMENT PRIMARY KEY,
       username VARCHAR(50) UNIQUE NOT NULL,
       password VARCHAR(100) NOT NULL,
       hasVoted BOOLEAN DEFAULT FALSE
   );

   CREATE TABLE votes (
       id INT AUTO_INCREMENT PRIMARY KEY,
       candidate VARCHAR(100) NOT NULL,
       user_id INT,
       FOREIGN KEY (user_id) REFERENCES users(id)
   );

4. Open the `DatabaseConnection.java` file and update your MySQL credentials:
   private static final String URL = "jdbc:mysql://localhost:3306/OnlineVotingSystem";
   private static final String USERNAME = "root";
   private static final String PASSWORD = "your_password";

5. Compile the Java files using:
   javac Main.java User.java VotingSystem.java DatabaseConnection.java

6. Run the program:
   java Main
```

## 📌 Sample Output

```
Welcome to the Online Voting System!
1. Register
2. Login
Enter username: john123
Enter password: ****
Login successful!
Enter candidate name to vote for: Alice
Vote cast successfully!
Do you want to view the results? (yes/no): yes
Alice: 1 votes
```

## 🚀 Future Scope

- Add password encryption
- Create an admin panel
- Develop a GUI using Swing or JavaFX
- Add support for voting deadlines

## 🙌 Contributing

If you find any bugs or have suggestions, feel free to fork the repo and raise a pull request.

