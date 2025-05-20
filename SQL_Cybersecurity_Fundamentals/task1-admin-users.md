# 🛡️ Task 1: Identify Admin Users

CREATE DATABASE psy_lab;

USE psy_lab;

## 📌 Objective
Create a users table and use SQL to find all users with the role of 'admin'. This helps identify who has elevated privileges — critical for auditing and access control.

## 🗂️ Create Table
CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100),
    role VARCHAR(50),
    is_active BOOLEAN,
    last_login DATETIME
);

## 📥 Insert Sample Data
INSERT INTO users (username, role, is_active, last_login) 
VALUES 
('tim_cheatham', 'admin', true, '2024-05-01 08:30:00'),
('sly_stone', 'user', true, '2024-05-02 09:45:00'),
('con_man', 'admin', false, '2024-04-25 16:20:00');

## 🔍 Query Admin Users
SELECT * FROM users
WHERE role = 'admin';


