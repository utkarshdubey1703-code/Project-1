# Simple Store – Pure Python Website using PyWebIO

## Project Overview

**Simple Store** is a lightweight web-based store application developed entirely in Python using the **PyWebIO** framework. The project demonstrates how Python can be used to create an interactive browser-based application without directly writing HTML, CSS, or JavaScript.

The application provides a basic store workflow:

- Display available products
- View price and stock information
- Buy products by selecting quantity
- Validate requested quantity against available stock
- Add purchased products to a shopping cart
- Calculate the total cart amount
- Add new products to the store
- Exit the application through the user interface

The project is implemented in a Jupyter Notebook and uses PyWebIO to provide browser-based interaction.

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Web UI Framework | PyWebIO |
| Development Environment | Jupyter Notebook / IPython |
| Server | PyWebIO server using Tornado |
| Data Storage | In-memory Python lists |
| Python Version in notebook | 3.14.6 |
| PyWebIO version shown in notebook | 1.8.4 |

## Project Structure

The notebook is organized into three main parts:

1. **Project introduction**
2. **Store data and application functions**
3. **PyWebIO server startup**

### Main Data Structures

The application stores product information in parallel Python lists:

- `product_names` – stores product names
- `product_prices` – stores product prices
- `product_stock` – stores available stock quantities
- `cart_items` – stores items selected by the customer
- `cart_prices` – stores the corresponding prices/totals

Initial products included in the project:

| Product | Price | Initial Stock |
|---|---:|---:|
| Notebook | 50 | 20 |
| Pen | 10 | 100 |
| Bag | 500 | 15 |
| Water Bottle | 150 | 30 |
| Calculator | 300 | 10 |

## Main Functions

### `show_products()`
Displays the available products in a table containing product number, product name, price, and stock.

### `buy_product()`
Allows the user to:

1. Select a product.
2. Enter the required quantity.
3. Validate that the quantity is positive.
4. Check whether sufficient stock is available.
5. Reduce inventory after a successful purchase.
6. Add the selected item and its calculated price to the cart.

### `sell_product()`
Despite the function name, this feature is used to **add a new product to the store inventory**. It accepts:

- Product name
- Price
- Stock quantity

The new product is appended to the existing inventory lists.

### `show_cart()`
Displays the items currently in the cart and calculates the total amount.

### `main()`
Controls the application workflow through a continuous menu:

- Buy a Product
- Sell / Add a Product
- View Cart
- Exit

## Installation

Install PyWebIO using:

```bash
pip install pywebio
```

Or, inside Jupyter Notebook:

```python
%pip install pywebio
```

## Running the Project

Open the notebook in Jupyter Notebook or JupyterLab and execute the cells in order.

The project starts a PyWebIO server on:

```text
http://127.0.0.1:8080
```

Open this address in a browser after the server starts.

## Important Note About Port 8080

The notebook output shows that the server initially reports:

```text
Server started! Open http://127.0.0.1:8080 in your browser.
```

A subsequent server-start attempt produced:

```text
OSError: [WinError 10048] Only one usage of each socket address
```

This indicates that port **8080 was already occupied**, commonly because another instance of the application/server was already running. This is an environment/runtime issue rather than an error in the store's product and cart logic.

If required, restart the Jupyter kernel before starting a fresh server instance.

## Application Workflow

```text
Start Application
       |
       v
Display Product Inventory
       |
       v
Choose an Action
   /      |       |        Buy    Add     Cart     Exit
  |      |        |        |
  v      v        v        v
Check   Add    Calculate  End
Stock   Item     Total
  |
  v
Update Inventory
  |
  v
Add Item to Cart
  |
  v
Return to Menu
```

## Limitations

The current version is intentionally simple and educational. It does not include:

- Database persistence
- User authentication
- Payment gateway integration
- Order history
- Product deletion/editing
- Image-based product catalogue
- Persistent shopping carts
- Multi-user session management
- Advanced validation for all input fields

Because product and cart data are stored in Python lists, the data is lost when the application process/kernel is restarted.

## Future Enhancements

Possible improvements include:

1. Replace parallel lists with dictionaries or structured classes.
2. Add SQLite/MySQL database storage.
3. Add login and user authentication.
4. Add product search and filtering.
5. Add product categories.
6. Add quantity update and item removal in the cart.
7. Add checkout and order confirmation.
8. Add persistent order history.
9. Add better input validation.
10. Add product images and improved UI styling.
11. Add an administrator dashboard.
12. Deploy the application to a cloud platform.

## Learning Outcomes

This project demonstrates practical use of:

- Python lists and variables
- Functions
- Loops
- Conditional statements
- Input validation
- String formatting
- Basic inventory management
- Shopping cart logic
- Modular program design
- Browser-based Python interfaces
- Running a Python web application through PyWebIO

## Academic Project Summary

**Project Title:** Simple Store – Pure Python Website using PyWebIO

**Project Type:** Python/Web Application

**Primary Objective:** To develop a basic interactive store application using Python and PyWebIO.

**Core Concepts:** Python programming, functions, lists, loops, conditions, input handling, inventory management, and web-based user interaction.

**Development Environment:** Jupyter Notebook

**Framework:** PyWebIO

**Status:** Functional educational prototype with in-memory data storage.

---

## Author Details

Fill in the following information before submission:

- **Student Name:** ______________________________
- **Registration Number:** ________________________
- **Course / Program:** ____________________________
- **Branch / Section:** ____________________________
- **Semester:** ___________________________________
- **Faculty / Mentor:** ____________________________
- **Institute:** VIT Bhopal University
- **Academic Year:** ______________________________

