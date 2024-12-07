Database 
mysql -u root -p
CREATE DATABASE feedback_system_db;
SHOW DATABASES;
USE feedback_system_db;
-- Create the 'student' table
CREATE TABLE student (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

-- Create the 'admin' table
CREATE TABLE admin (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

-- Create the 'feedback' table
CREATE TABLE feedback (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    faculty_name VARCHAR(255) NOT NULL,
    question1 VARCHAR(255),
    question2 VARCHAR(255),
    question3 VARCHAR(255)
);
-- Create the 'student' table
CREATE TABLE student (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

-- Create the 'admin' table
CREATE TABLE admin (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

-- Create the 'feedback' table
CREATE TABLE feedback (
    id BIGINT AUTO_INCREMENT PRIMARY KEY,
    faculty_name VARCHAR(255) NOT NULL,
    question1 VARCHAR(255),
    question2 VARCHAR(255),
    question3 VARCHAR(255)
);
# Database configuration
spring.datasource.url=jdbc:mysql://localhost:3306/feedback_system_db
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# Hibernate configuration
spring.jpa.database-platform=org.hibernate.dialect.MySQL8Dialect
spring.jpa.hibernate.ddl-auto=update  # Can be 'create' for a fresh schema or 'update' to keep changes

# JPA properties
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
