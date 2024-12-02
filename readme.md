# Node.js CRUD Application

A simple CRUD (Create, Read, Update, Delete) application built with Node.js, Express, and MySQL.

## Prerequisites

Before you begin, ensure you have met the following requirements:
* You have installed Node.js and npm (Node Package Manager)
* You have installed MySQL
* You have a Windows/Linux/Mac machine

## Installing Node.js CRUD Application

To install the application, follow these steps:

1. Clone the repository
```bash
git clone https://github.com/triyono777/crud-app-espress-js.git
```

2. Navigate to the project directory
```bash
cd crud-app-espress-js
```

3. Install dependencies
```bash
npm install
```

4. Create a MySQL database and table
```sql
CREATE DATABASE crud_db;
USE crud_db;

CREATE TABLE products (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    price DECIMAL(10, 2) NOT NULL,
    stock INT NOT NULL,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

5. Configure environment variables
```bash
# Create .env file
cp .env_sample .env

# Edit .env file with your database credentials
PORT=3000
DB_HOST=localhost
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=crud_db
```

## Using Node.js CRUD Application

To use the application, follow these steps:

1. Start the development server
```bash
npm run dev
```

2. Start the production server
```bash
npm start
```

The server will start running at `http://localhost:3000`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/products | Get all products |
| GET | /api/products/:id | Get a single product |
| POST | /api/products | Create a new product |
| PUT | /api/products/:id | Update a product |
| DELETE | /api/products/:id | Delete a product |

### Example API Requests

#### Get All Products
```http
GET http://localhost:3000/api/products
```

#### Get Single Product
```http
GET http://localhost:3000/api/products/1
```

#### Create Product
```http
POST http://localhost:3000/api/products
Content-Type: application/json

{
    "name": "Product 1",
    "price": 99.99,
    "stock": 100
}
```

#### Update Product
```http
PUT http://localhost:3000/api/products/1
Content-Type: application/json

{
    "name": "Updated Product",
    "price": 149.99,
    "stock": 75
}
```

#### Delete Product
```http
DELETE http://localhost:3000/api/products/1
```

## Project Structure
```
crud-app/
├── src/
│   ├── config/
│   │   └── database.js
│   ├── controllers/
│   │   └── productController.js
│   ├── models/
│   │   └── productModel.js
│   ├── routes/
│   │   └── productRoutes.js
│   └── app.js
├── .env
└── package.json
```

## Dependencies

* express - Web framework for Node.js
* mysql2 - MySQL client for Node.js
* dotenv - Load environment variables
* cors - Enable CORS
* nodemon (dev dependency) - Auto-reload server during development

## Contributing to Node.js CRUD Application

To contribute to the project, follow these steps:

1. Fork this repository
2. Create a new branch: `git checkout -b <branch_name>`
3. Make your changes and commit them: `git commit -m '<commit_message>'`
4. Push to the original branch: `git push origin <project_name>/<location>`
5. Create the pull request

## Contact

If you want to contact me you can reach me at `<your_email@example.com>`.

## License

This project uses the following license: [MIT License](<link_to_license>).