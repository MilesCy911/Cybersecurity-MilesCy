# 🛡️ Task 4: Audit Login Attempts

CREATE TABLE login_attempts (
    attempt_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(100),
    attempt_time DATETIME,
    success BOOLEAN,
    ip_address VARCHAR(45)
);

-- Insert sample data to simulate login attempts (including failures for audit)

INSERT INTO login_attempts (username, attempt_time, success, ip_address) VALUES
('tim_cheatham', '2025-05-19 08:15:00', TRUE, '192.168.1.10'),
('sly_stone', '2025-05-19 08:20:00', FALSE, '192.168.1.11'),
('con_man', '2025-05-19 08:25:00', TRUE, '192.168.1.12'),
('philippe_scheme', '2025-05-18 09:00:00', FALSE, '192.168.1.13'),
('pete_wormsy', '2025-05-17 10:30:00', TRUE, '192.168.1.14'),
('randy_ransom', '2025-05-16 11:45:00', FALSE, '192.168.1.15'),
('tim_cheatham', '2025-05-15 12:00:00', TRUE, '192.168.1.10');

-- Query: Find all failed login attempts for audit review

SELECT username, attempt_time, ip_address
FROM login_attempts
WHERE success = FALSE
ORDER BY attempt_time DESC;
