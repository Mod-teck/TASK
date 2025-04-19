# Inventory Management System with Demand Forecasting

## Description

This is a simple Inventory Management System built using **Laravel** and **SQL**.  
The system allows users to:

- Add new products
- Track available stock for each product
- Record product orders
- Generate a demand forecast report based on past order trends
  
---

## Features

- **Add Products:** Add new products with name, description, and quantity
- **List Products:** View all available products and their quantities
- **Create Orders:** Place orders for products and reduce available stock accordingly
- **Demand Forecasting:** Report products that need to be reordered based on recent demand

---

## Technologies Used

- Laravel (PHP Framework)
- MySQL or any other SQL-based database

---

## Models

### 1. Product

Represents a product in the inventory.

| Field        | Type         | Description                      |
|--------------|--------------|----------------------------------|
| id           | Integer      | Primary key                      |
| name         | String       | Product name                     |
| description  | Text         | Product description              |
| quantity     | Integer      | Available stock                  |
| created_at   | Timestamp    | Record creation date             |
| updated_at   | Timestamp    | Record last update date          |

---

### 2. Order

Represents a customer order for a product.

| Field        | Type         | Description                                 |
|--------------|--------------|---------------------------------------------|
| id           | Integer      | Primary key                                 |
| product_id   | Integer      | Foreign key referencing `products` table    |
| quantity     | Integer      | Quantity ordered                            |
| order_date   | Date         | Date of the order                           |
| created_at   | Timestamp    | Record creation date                        |
| updated_at   | Timestamp    | Record last update date                     |

---

## API Endpoints

### 1. Add a New Product

- **Endpoint:** `POST /api/products`
- **Input:** JSON object with:
  ```json
  {
    "name": "Product Name",
    "description": "Product Description",
    "quantity": 100
  }
