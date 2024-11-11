# E-Commerce Backend API

## Description
A robust backend API for e-commerce platforms built with Express.js, Sequelize ORM, and PostgreSQL. This application provides a complete suite of API endpoints to manage products, categories, and tags in an e-commerce database.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Technologies Used](#technologies-used)
- [Database Models](#database-models)
- [Contributing](#contributing)
- [License](#license)

## Installation
1. Clone the repository
2. Install dependencies:
    ```bash
    npm install
    ```
3. Create a `.env` file with your PostgreSQL credentials:
    ```plaintext
    DB_NAME='ecommerce_db'
    DB_USER='your_username'
    DB_PASSWORD='your_password'
    ```
4. Initialize the database:
    ```bash
    psql -U postgres -f db/schema.sql
    ```
5. Seed the database:
    ```bash
    npm run seed
    ```
6. Start the server:
    ```bash
    npm start
    ```

## Usage
Use an API client like Insomnia or Postman to test the endpoints:

### Categories
- GET `/api/categories` - Get all categories
- GET `/api/categories/:id` - Get category by ID
- POST `/api/categories` - Create new category
- PUT `/api/categories/:id` - Update category
- DELETE `/api/categories/:id` - Delete category

### Products
- GET `/api/products` - Get all products
- GET `/api/products/:id` - Get product by ID
- POST `/api/products` - Create new product
- PUT `/api/products/:id` - Update product
- DELETE `/api/products/:id` - Delete product

### Tags
- GET `/api/tags` - Get all tags
- GET `/api/tags/:id` - Get tag by ID
- POST `/api/tags` - Create new tag
- PUT `/api/tags/:id` - Update tag
- DELETE `/api/tags/:id` - Delete tag

## Technologies Used
- Node.js
- Express.js
- PostgreSQL
- Sequelize ORM
- dotenv

## Database Models

### Category
- id (Integer, Primary Key)
- category_name (String)

### Product
- id (Integer, Primary Key)
- product_name (String)
- price (Decimal)
- stock (Integer)
- category_id (Integer, Foreign Key)

### Tag
- id (Integer, Primary Key)
- tag_name (String)

### ProductTag
- id (Integer, Primary Key)
- product_id (Integer, Foreign Key)
- tag_id (Integer, Foreign Key)

## Contributing
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a pull request

## License
MIT License

## Questions
For questions and support, please contact:
- GitHub: [YourGitHubUsername](https://github.com/YourGitHubUsername)
- Email: your.email@example.com

