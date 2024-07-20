# Inventory-Management-System
A basic inventory management system using MySQL

This repository contains the SQL code for a basic Inventory Management System. The project is designed to demonstrate the use of SQL for database creation, management, and operations. This system includes tables for products, suppliers, orders, and order details, and includes sample data to illustrate typical operations.

## Table of Contents

- [Introduction](#introduction)
- [Database Schema](#database-schema)
- [Sample Data](#sample-data)
- [Usage](#usage)
- [Future Enhancements](#future-enhancements)
- [License](#license)
- [Contact](#contact)

## Introduction

The Inventory Management System is a basic database system designed to manage and track inventory items, suppliers, and orders. The primary purpose of this project is to demonstrate the use of SQL for database operations and to serve as a foundation for future enhancements and interface development.

## Database Schema

The database schema includes the following tables:

1. **Products**: Stores information about inventory items.
   - `ProductID`: Primary key, auto-incremented
   - `ProductName`: Name of the product
   - `Category`: Category of the product
   - `Quantity`: Quantity available
   - `Price`: Price of the product

2. **Suppliers**: Stores information about suppliers.
   - `SupplierID`: Primary key, auto-incremented
   - `SupplierName`: Name of the supplier
   - `ContactName`: Contact person at the supplier
   - `Address`: Address of the supplier
   - `City`: City of the supplier
   - `PostalCode`: Postal code of the supplier
   - `Country`: Country of the supplier
   - `Phone`: Contact phone number

3. **Orders**: Stores information about orders placed with suppliers.
   - `OrderID`: Primary key, auto-incremented
   - `OrderDate`: Date the order was placed
   - `SupplierID`: Foreign key referencing `SupplierID` in the Suppliers table

4. **OrderDetails**: Stores details about the products ordered.
   - `OrderDetailID`: Primary key, auto-incremented
   - `OrderID`: Foreign key referencing `OrderID` in the Orders table
   - `ProductID`: Foreign key referencing `ProductID` in the Products table
   - `Quantity`: Quantity of the product ordered

## Sample Data

The following sample data is included in the database:

### Products

| ProductID | ProductName | Category  | Quantity | Price |
|-----------|-------------|-----------|----------|-------|
| 1         | Product1    | Category1 | 100      | 10.00 |
| 2         | Product2    | Category2 | 200      | 20.00 |

### Suppliers

| SupplierID | SupplierName | ContactName | Address   | City  | PostalCode | Country | Phone  |
|------------|--------------|-------------|-----------|-------|------------|---------|--------|
| 1          | Supplier1    | Contact1    | Address1  | City1 | PostalCode1| Country1| Phone1 |
| 2          | Supplier2    | Contact2    | Address2  | City2 | PostalCode2| Country2| Phone2 |

### Orders

| OrderID | OrderDate  | SupplierID |
|---------|------------|------------|
| 1       | 2023-01-01 | 1          |
| 2       | 2023-01-02 | 2          |

### OrderDetails

| OrderDetailID | OrderID | ProductID | Quantity |
|---------------|---------|-----------|----------|
| 1             | 1       | 1         | 50       |
| 2             | 1       | 2         | 150      |
| 3             | 2       | 1         | 20       |
| 4             | 2       | 2         | 180      |

## Usage

To use this SQL script, follow these steps:

1. Open your MySQL client or command line interface.
2. Copy and paste the SQL code from the `Project DB.sql` file into your MySQL client.
3. Execute the SQL code to create the database and tables, and insert the sample data.
4. Verify that the database and tables are created correctly by running appropriate SQL queries.

## Future Enhancements

This basic Inventory Management System can be expanded with the following features:
- Develop a web-based interface for user interaction.
- Implement CRUD operations for managing products, suppliers, and orders.
- Add user authentication and authorization.
- Generate detailed reports and analytics.
- Implement inventory tracking and alerts.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

## Contact

For any questions or suggestions, please contact:

- **Name**: Usama Shahid
- **Email**: [usama03306587434@gmail.com]
