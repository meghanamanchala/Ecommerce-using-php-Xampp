-- This are the first steps to follow --

1. download windows latest version of xampp 
2. After installation click on start button to run apache , mySql
3. open your http://localhost/dashboard to check server is running correctly
4. open your http://localhost/phpmyadmin
5. now create a new database named ecommerce
6. After that create cart,users and product table
   
   - carts: sql command
   CREATE TABLE cart (
    id INT AUTO_INCREMENT PRIMARY KEY,
    user_id INT NOT NULL,
    product_id INT NOT NULL,
    quantity INT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP
   );

   - products: sql command
   CREATE TABLE products (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    price DECIMAL(10, 2) NOT NULL,
    description TEXT,
    image VARCHAR(255),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

   - user: sql command
   CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    role ENUM('user', 'admin') DEFAULT 'user'
   );

7. create a folder ecommerce in following location

   Location: filesfolder->this Pc -> os(c:) -> xampp -> htdocs -> (ecommerce) 

   open this file in vscode 

8. now create db.php and db_test.php to check    connection

9. finally create all pages and run http://localhost/ecommerce/index.php 

