# 🔒 Task 4: Identify Inactive Admin Accounts

CREATE DATABASE psy_lab;

## 📌 Objective  
Detect admin accounts that are no longer active. This is important for identifying stale privileged users that could pose a security risk if left unattended.

## 🗂️ Create Table  
CREATE TABLE users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100),
    role VARCHAR(50),
    is_active BOOLEAN,
    last_login DATETIME
);

## 🧪 Insert Sample Data (extended for portfolio testing)  
INSERT INTO users (username, role, is_active, last_login) VALUES
('tim_cheatham', 'admin', true, '2024-05-01 08:30:00'),
('sly_stone', 'user', true, '2024-05-02 14:15:00'),
('con_man', 'admin', false, '2024-04-25 16:20:00'),
('philippe_scheme', 'user', true, '2025-05-19 10:00:00'), 
('pete_wormsy', 'user', true, '2025-05-14 12:30:00'), 
('randy_ransom', 'admin', false, '2025-04-20 15:45:00');

## 🔍 Query: Find Inactive Admins  
SELECT * FROM users
WHERE role = 'admin' AND is_active = FALSE;
