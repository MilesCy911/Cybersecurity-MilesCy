# 🛡️ Task 2: Identify Inactive Users

USE psy_lab;

## 📌 Objective
Use SQL to find users who are marked as inactive. Inactive accounts can be vulnerable entry points and should be reviewed, disabled, or removed when not needed.

## 🗂️ Query Inactive Users
SELECT * FROM users
WHERE is_active = false;
