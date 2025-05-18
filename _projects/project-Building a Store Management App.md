---
title: Building a Store Management App
excerpt: All-in-one solution for store operations
layout: single
author_profile: true
toc: true
toc_sticky: true
header:
  teaser: /assets/obsidian/44dfddcd19c868e998541eedbb8781fc.png
---
## **Business Scenario**

This project is a Store Management App designed for small to medium-sized retail businesses. It streamlines the management of employees, products, suppliers, customers, inventory, sales (invoices), and purchase transactions. The app supports different user roles (Admin, Staff, Viewer) with appropriate access controls. The app provides an all-in-one solution for store operations, ensuring efficient management and insightful reporting.

## **Techniques**

- **Frontend:** Built with `Streamlit` for rapid web app development and interactive dashboards.
- **Backend:** Uses MySQL for data storage and retrieval, with `mysql-connector-python` for database connectivity.
- **Data Handling:** Utilizes `pandas` for data manipulation and display.
- **Authentication:** Simple role-based login system.
- **UI Components:** Employs `streamlit-option-menu` for sidebar navigation.

## **Workflow**

### Step 1: **Role-based Navigation**

- Users log in with a username and password.
- Role-based access determines available sections (Admin, Trading, Report).
    - Admin: Access all tabs: Admin, Trading, Report, Dashboard
    - Staff: Access Trading, Report, Dashboard tabs
    - Viewer: Access Report, Dashboard tab only

### Step 2: **Admin Management**

- Manage employees, salaries, suppliers, customers, products, and product prices.
- Auto-generates unique IDs for new records.
- Inline editing and deletion of records.
- Data entry and editing via forms.

### Step 3: **Trade Management**

- Create and save sales invoices (with stock checks).
- Create and save purchase transactions.
- Dynamic product selection, quantity, and price entry.
- Real-time calculation of totals.

### Step 4: **Report Management**

- View product stock availability.
- List and filter invoices and transactions with detailed breakdowns.
- Calculate and display total sales and purchase amounts.

## **Functionalities**

- User Login

1. Login Interface

<img src="/assets/obsidian/930c7465dcbbb047d4c64d66bc4cf2c5.png" />

2. Login wrong password

<img src="/assets/obsidian/f8a2cdf49cccfa45e32babaffa02f5dd.png" />

3. Admin Login

<img src="/assets/obsidian/2c1a564fc981e3c074e8d6d7e13b8349.png" />

4. Staff Login

<img src="/assets/obsidian/e9d07b6d761e02cf1a7254129769e0b6.png" />

5. Viewer Login

<img src="/assets/obsidian/73b3f1f14f3266b7e4ce9bbc3ffc3697.png" />

- Add/edit/delete employees, products, suppliers, customers, and prices

1. Add Employee

<img src="/assets/obsidian/1e33b643e0b7f94d3b72a4eef909637e.png" />

<img src="/assets/obsidian/235f764d60fe5b1aad4d18dd2ea4b102.png" />

2. Edit Employee

<img src="/assets/obsidian/47d4237e5c0f33e4e09b1a429f2e5cdb.png" />

3. Add Salary

<img src="/assets/obsidian/fe7f069a5055557a9772ecb1afb55c66.png" />

4. Edit Salary

<img src="/assets/obsidian/0524d85fb0707455ffaad277fd4b5cf6.png" />


5. Add Supplier

<img src="/assets/obsidian/e65fff952540f24b3b89fe999c3297ca.png" />

6. Edit Supplier

<img src="/assets/obsidian/fe980133a5002c5811714aead595219a.png" />

7. Add Customer

<img src="/assets/obsidian/a5f3f804d8a986b6c25d5c5104cc551c.png" />

8. Edit Customer

<img src="/assets/obsidian/6042dec4dbca1e53255e715bc0fa7b9c.png" />

9. Add Product

<img src="/assets/obsidian/c3f1d137d09a221f62db403984c2db18.png" />

10. Edit Product

<img src="/assets/obsidian/716b24de2f9ae0d6e3e5c4ad7dbccd94.png" />

11. Add Product Price

<img src="/assets/obsidian/9fe3fe7f35649e66f0a7b16d11de3d86.png" />

12. Edit Product Price

<img src="/assets/obsidian/5632e9f5986d5010f7192517292955ca.png" />


- Create invoices and transactions, ensuring stock is available

1. Add Invoice with stock check: select employee name, customer name, invoice date using drop box (can not edit or delete invoice after it is created)

<img src="/assets/obsidian/962f19fe35561f8fdfcba5b090c69a5d.png" />

<img src="/assets/obsidian/d05ce02d7ae82fcffd642c2390f49b29.png" />

2. Add Transaction: select employee name, supplier name, transaction date using drop box (can not edit or delete transaction after it is created)

<img src="/assets/obsidian/d1b105d0511cdb7ab7c4806793cfcb92.png" />


- View and filter reports on stock, invoices, and transactions

1. Product Stock

<img src="/assets/obsidian/1ee00d59ad0b45a18835c896bf3d99ee.png" />

2. List of Invoices

<img src="/assets/obsidian/e3d4cc32355d43e0cab0b87bd84b8e19.png" />

3. List of Transactions

<img src="/assets/obsidian/88ccc3d3d76740eddb8dd165b2a85c2b.png" />

- Integrate Power BI Dashboard

<img src="/assets/obsidian/44dfddcd19c868e998541eedbb8781fc.png" />


## **Demo**

<iframe width="560" height="315" src="https://www.youtube.com/embed/IRJHvqYcW_k?si=zsanZl0JWNPj0m9S" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


