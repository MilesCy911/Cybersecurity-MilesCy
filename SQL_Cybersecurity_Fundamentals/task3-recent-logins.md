# 🛡️ Task 3: Find Recent Logins

## 📌 Objective
Query the users table to find all users who have logged in within the last 7 days. This helps monitor recent activity for security auditing.

## 🗂️ Insert Sample Data (Extended for Portfolio) & Query Recent Logins

INSERT INTO users (username, role, is_active, last_login) 
VALUES 
('philippe_scheme', 'user', true, '2024-05-10 10:00:00'),
('pete_wormsy', 'user', true, '2024-05-09 12:30:00'),
('randy_ransom', 'admin', false, '2024-04-20 15:45:00');

SELECT * 
FROM users
WHERE last_login >= NOW() - INTERVAL 7 DAY;
