# 🗳️ Online Voting System

A secure, console-based **Online Voting System** built in Java with MySQL integration. This project enables users to register, log in, vote once for a candidate, and view real-time election results. It implements basic authentication and ensures vote integrity using a simple JDBC setup.

---

## 🚀 Features

- 🔐 **User Authentication** – Register and login functionality
- 🗳️ **Secure Voting** – Each user can cast only one vote
- 📊 **Live Results** – View current vote count for each candidate
- 💾 **Database Integration** – MySQL backend for user and vote storage
- 🛡️ **Vote Integrity** – Prevents duplicate voting using a flag system

---

## 🛠️ Tech Stack

- **Java** – Core logic and console interaction
- **JDBC** – Database connectivity
- **MySQL** – Data persistence (Users & Votes)

---

## 📷 Demo

```bash
Welcome to the Online Voting System!
1. Register
2. Login
Enter username: alice
Enter password: ****
Login successful!
Enter candidate name to vote for: John Doe
Vote cast successfully!
Do you want to view the results? (yes/no): yes
John Doe: 1 votes
