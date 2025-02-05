CREATE DATABASE memory_game;

USE memory_game;

CREATE TABLE cards (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    image VARCHAR(255) NOT NULL
);

INSERT INTO cards (name, image) VALUES
('chili', '../assets/chili.png'),
('grapes', '../assets/grapes.png'),
('lemon', '../assets/lemon.png'),
('orange', '../assets/orange.png'),
('pineapple', '../assets/pineapple.png'),
('strawberry', '../assets/strawberry.png'),
('tomato', '../assets/tomato.png'),
('watermelon', '../assets/watermelon.png'),
('cherries', '../assets/cherries.png');

CREATE USER 'Memory'@'%' IDENTIFIED BY 'Memory1';
GRANT ALL PRIVILEGES ON `memory_game`.* TO 'Memory'@'%';
FLUSH PRIVILEGES;

