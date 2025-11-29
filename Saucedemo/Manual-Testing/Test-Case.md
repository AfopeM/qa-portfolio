# Test Cases - SauceDemo

## Overview

This document outlines the test cases for verifying **login**, **inventory**,
**cart**, and **checkout** behaviour on **SauceDemo**.  
Each test case includes **priority**, **preconditions**, **steps**, and
**expected outcomes** for clarity.

## Login Functionality 🔐

### 🔹 TC-LOGIN-001: Successful Login With Valid Credentials

**Priority:** High

**Preconditions:**

- User is on **[Home Page](https://www.saucedemo.com/)**
- User is **not logged in**

**Steps:**

1. Enter **valid username** in the Username field
2. Enter **valid password** in the Password field
3. Click the **Login** button

**Expected Results:**

- User is redirected to
  **[Inventory Page](https://www.saucedemo.com/inventory.html)**
- Product list is displayed

### 🔹 TC-LOGIN-002: Unsuccessful Login With Invalid Credentials

**Priority:** High

**Preconditions:**

- User is on **[Home Page](https://www.saucedemo.com/)**
- User is **not logged in**

**Steps:**

1. Enter **invalid username** in the Username field
2. Enter **valid password** in the Password field
3. Click the **Login** button

**Expected Results:**

- User remains on **[Home Page](https://www.saucedemo.com/)**
- System displays error message: **"Epic sadface: Username and password do not
  match any user in this service"**

---

### 🔹 TC-LOGIN-003: Login Fails With Blank Username and Password

**Priority:** Medium

**Preconditions:**

- User is on **[Home Page](https://www.saucedemo.com/)**
- User is **not logged in**

**Steps:**

1. Leave both Username and Password fields blank
2. Click the **Login** button

**Expected Results:**

- User remains on **[Home Page](https://www.saucedemo.com/)**
- System displays error message: **"Epic sadface: Username and password do not
  match any user in this service"**

### 🔹 TC-LOGIN-004: Login Fails When Valid Credentials Include Extra Whitespace

**Priority:** High

**Preconditions:**

- User is on **[Home Page](https://www.saucedemo.com/)**
- User is **not logged in**

**Steps:**

1. Enter **valid username** in the Username field
2. Add an extra space after the username
3. Enter **valid password** in the Password field
4. Click the **Login** button

**Expected Results:**

- Whitespace in the username field is **trimmed**
- User is redirected to
  **[Inventory Page](https://www.saucedemo.com/inventory.html)**
- Product list is displayed


## Inventory Functionality 📦

### 🔹 TC-INVENTORY-005: Inventory Items Display Correct Details

**Priority:** High

**Preconditions:**

- User is **logged in**
- User is on **[Inventory Page](https://www.saucedemo.com/inventory.html)**

**Steps:**

1. Scroll through the full inventory list
2. Verify that each item’s **name**, **description**, and **image** match
   expected values

**Expected Results:**

- All item names, descriptions, and images display correct and matching details


### 🔹 TC-INVENTORY-006: Sort Items by Name (Z → A)

**Priority:** Low

**Preconditions:**

- User is **logged in**
- User is on **[Inventory Page](https://www.saucedemo.com/inventory.html)**

**Steps:**

1. Click the **“Sort”** icon/button
2. Select **“Name (Z - A)”** from the options

**Expected Results:**

- Products reorder in **descending alphabetical order** by name

### 🔹 TC-INVENTORY-007: Item Sort Order Does Not Persist After Page Refresh

**Priority:** Low

**Preconditions:**
- User is **logged in**  
- User is on **[Inventory Page](https://www.saucedemo.com/inventory.html)**  
- Items are sorted in **Name descending order**

**Steps:**
1. Refresh the page

**Expected Results:**
- Page refreshes successfully  
- Products remain arranged in **descending order by name**

### 🔹 TC-INVENTORY-008: Add Item to Cart From Inventory Page
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Inventory Page](https://www.saucedemo.com/inventory.html)**

**Steps:**
1. Select any item from the inventory list  
2. Click the **Add to cart** button for that item

**Expected Results:**
- Selected item is added to the cart  
- Cart icon count increases by **1**  
- Item’s button updates to reflect its new state (**“Remove”**)


### 🔹 TC-INVENTORY-009: Remove Item From Cart on Inventory Page
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Inventory Page](https://www.saucedemo.com/inventory.html)**  
- At least one item is in the cart

**Steps:**
1. Select an item that has been added to the cart  
2. Click the **“Remove”** button for that item

**Expected Results:**
- Selected item is removed from the cart  
- Cart icon count decreases by **1**  
- Item’s button updates to reflect its new state (**“Add to cart”**)

### 🔹 TC-INVENTORY-010: Successfully Add the Correct Item to Cart
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Inventory Page](https://www.saucedemo.com/inventory.html)**  
- Cart is empty

**Steps:**
1. Scroll through the inventory list  
2. Select any item from the inventory list  
3. Click the **“Add to cart”** button on the selected item  
4. Capture (screenshot/document) the details of the selected item  
5. Navigate to the **[Cart Page](https://www.saucedemo.com/cart.html)**  
6. Compare the details of the item in the cart with the captured data

**Expected Results:**
- Details of the cart item match the captured data (**name, image, description**)  
- Cart icon count increases by **1**

## Cart Functionality 🛒

### 🔹 TC-CART-011: Cart Items Persist Through Refresh on Cart Page
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Cart Page](https://www.saucedemo.com/cart.html)**  
- At least **one item** is in the cart

**Steps:**
1. Capture **(screenshot/document)** the item(s) in the cart  
2. Capture **(screenshot/document)** the cart icon count  
3. Refresh the page  
4. Compare the captured item(s) data with the current cart items  
5. Compare the captured cart icon count with the current cart icon count

**Expected Results:**
- Items in the cart match the captured data  
- Cart icon count remains **unchanged**

### 🔹 TC-CART-012: Remove Cart Item from Cart Page
**Priority:** Medium

**Preconditions:**
- User is **logged in**  
- User is on **[Cart Page](https://www.saucedemo.com/cart.html)**  
- At least **one item** is in the cart

**Steps:**
1. Select an item from the cart  
2. Click the **“Remove”** button for the selected item

**Expected Results:**
- The selected item is removed from the cart  
- Cart icon count decreases by **1**


### 🔹 TC-CART-013: Checkout Process Fails When Cart is Empty
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Cart Page](https://www.saucedemo.com/cart.html)**  
- Cart is **empty**

**Steps:**
1. Click the **“Checkout”** button

**Expected Results:**
- User remains on the **Cart Page**  
- System displays error message:  
  **“Your Cart is Empty, Add Items from Inventory page”**

### 🔹 TC-CART-014: Successfully Start Checkout Process When Cart Has an Item
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Cart Page](https://www.saucedemo.com/cart.html)**  
- At least **one item** is in the cart

**Steps:**
1. Click the **“Checkout”** button

**Expected Results:**
- User is navigated to **[Checkout Step One Page](https://www.saucedemo.com/checkout-step-one.html)**

### 🔹 TC-CART-015: Item is Removed From Cart if Not Present in Inventory
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Cart Page](https://www.saucedemo.com/cart.html)**  
- At least **one item** is in the cart  
- Tester has access to **inventory data** (backend/admin panel)

**Steps:**
1. Capture **(screenshot/document)** the item(s) in the cart  
2. Navigate to **Inventory database** (backend/admin panel)  
3. Remove item matching captured data from the inventory  
4. Navigate back to **Cart Page**  
5. Check cart items for any item matching captured data

**Expected Results:**
- Item removed from cart matches the captured data  
- Cart icon count decreases by **1**

## Checkout Functionality 🧾

### 🔹 TC-CHECKOUT-016: User Cannot Proceed to Checkout Step Two with Blank Form
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Checkout Step One Page](https://www.saucedemo.com/checkout-step-one.html)**

**Steps:**
1. Leave all fields in the information form **blank**  
2. Click the **Continue** button at the bottom right of the form

**Expected Results:**
- User remains on **Checkout Step One Page**  
- System displays error message:  
  **“Error: First Name is required”**

### 🔹 TC-CHECKOUT-017: Checkout Step One Form Rejects Invalid Data Types
**Priority:** Medium

**Preconditions:**
- User is **logged in**  
- User is on **[Checkout Step One Page](https://www.saucedemo.com/checkout-step-one.html)**

**Steps:**
1. Enter **numbers** in the “First Name” field  
2. Enter **valid text** in the “Last Name” field  
3. Enter **valid postal code** in the “Zip/Postal Code” field  
4. Click the **Continue** button

**Expected Results:**
- User remains on **Checkout Step One Page**  
- System displays error message:  
  **“Error: Data type for First Name is incorrect”**

### 🔹 TC-CHECKOUT-018: Cart Items Match Items Displayed in Checkout Step Two
**Priority:** High

**Preconditions:**
- User is **logged in**  
- Tester has captured data **(screenshot/document)** of items in the cart  
- User is on **[Checkout Step Two Page](https://www.saucedemo.com/checkout-step-two.html)**

**Steps:**
1. Compare the Checkout Step Two overview of cart items with captured data

**Expected Results:**
- Captured cart item data matches Checkout Step Two overview (**name, image, description**)

### 🔹 TC-CHECKOUT-019: Checkout Total Price Calculation Is Correct
**Priority:** High

**Preconditions:**
- User is **logged in**  
- User is on **[Checkout Step Two Page](https://www.saucedemo.com/checkout-step-two.html)**

**Steps:**
1. Manually calculate the total price of all items **(sum of items + tax)**  
2. Compare manual total with the total displayed on Checkout Step Two

**Expected Results:**
- Manually calculated total matches the total displayed on Checkout Step Two

### 🔹 TC-CHECKOUT-020: Successfully Complete Checkout Process
**Priority:** High

**Preconditions:**
- User is **logged in**  
- At least **one item** is in the cart  
- User is on **[Checkout Step Two Page](https://www.saucedemo.com/checkout-step-two.html)**

**Steps:**
1. Click the **Finish** button at the bottom right of the overview section

**Expected Results:**
- User is navigated to **[Checkout Complete Page](https://www.saucedemo.com/checkout-complete.html)**  
- System displays success message: **“Thank you for your order!”**  
- Cart icon count is reset to **0**
