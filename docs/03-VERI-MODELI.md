# Database Schema and Data Model Documentation

This document outlines the database schema and data model for the ERP Distribution System, including all tables, relationships, and indexes.

## Tables

### 1. Users
- **user_id** (PK, int) - Unique identifier for each user
- **username** (varchar) - Username of the user
- **password** (varchar) - Password for the user account
- **email** (varchar) - Email address of the user

### 2. Products
- **product_id** (PK, int) - Unique identifier for each product
- **product_name** (varchar) - Name of the product
- **price** (decimal) - Price of the product
- **stock_quantity** (int) - Quantity in stock

### 3. Orders
- **order_id** (PK, int) - Unique identifier for each order
- **user_id** (FK, int) - Identifier for the user who placed the order
- **order_date** (datetime) - Date and time when the order was placed

### 4. Order_Items
- **order_item_id** (PK, int) - Unique identifier for each order item
- **order_id** (FK, int) - Identifier for the order
- **product_id** (FK, int) - Identifier for the product
- **quantity** (int) - Quantity of the product ordered

### 5. Inventory
- **inventory_id** (PK, int) - Unique identifier for each inventory record
- **product_id** (FK, int) - Identifier for the product
- **quantity_in_stock** (int) - Current stock quantity

## Relationships
- **Users** to **Orders**: One-to-Many (One user can place multiple orders)
- **Orders** to **Order_Items**: One-to-Many (One order can contain multiple items)
- **Products** to **Order_Items**: One-to-Many (One product can appear in multiple order items)
- **Products** to **Inventory**: One-to-One (Each product has one inventory record)

## Indexes
- **Users:** Index on `username` for faster lookup.
- **Products:** Index on `product_name` for quick search.
- **Orders:** Composite index on `user_id` and `order_date` for efficient order history retrieval.
- **Order_Items:** Index on `order_id` for faster access to order items related to a specific order.

## ERD Diagram
![ERD Diagram](path/to/erd-diagram.png)

This ERD diagram visually represents the relationships between the tables in the ERP Distribution System.