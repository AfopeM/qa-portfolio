# Test Cases - SauceDemo

## Overview
This document outlines the test cases for verifying login, inventory, cart, and checkout behaviour on **SauceDemo**. Each case includes priority, preconditions, steps, and expected outcomes for clarity.

---

## Login Functionality  🔐

## 🔸 TC-LOGIN-001 — Successful Login With Valid Credentials  
**Priority:** High

### Preconditions
- User is on **[Home Page](https://www.saucedemo.com/)**
- User is not logged in

### Steps
1. Enter **valid username** in the Username field  
2. Enter **valid password** in the Password field  
3. Click the **"Login"** button

### Expected Results
- The user is redirected to **[Inventory Page](https://www.saucedemo.com/inventory.html)**  
- The product list is displayed

---

## 🔸 TC-LOGIN-002 — Unsuccessful Login With Invalid Credentials  
**Priority:** High

### Preconditions
- User is on **[Home Page](https://www.saucedemo.com/)**
- User is not logged in

### Steps
1. Enter **invalid username** in the Username field  
2. Enter **valid password** in the Password field  
3. Click the **"Login"** button

### Expected Results
- The user remains on **[Home Page](https://www.saucedemo.com/)**
- The system displays an Error message:**"Epic sadface: Username and password do not match any user in this service"**

---

## 🔸 TC-LOGIN-003 — Login Fails With Blank Username and Password  
**Priority:** Medium

### Preconditions
- User is on **[Home Page](https://www.saucedemo.com/)**
- User is not logged in

### Steps
1. Leave both Username and Password fields blank  
2. Click the **"Login"** button

### Expected Results
- User remains on **[Home Page](https://www.saucedemo.com/)**
- System displays an Error message:**"Epic sadface: Username and password do not match any user in this service"**

---

## 🔸 TC-LOGIN-004 — Login Fails When Valid Credentials Include Extra Whitespace  
**Priority:** High

### Preconditions
- User is on **[Home Page](https://www.saucedemo.com/)**
- User is not logged in

### Steps
1. Enter **"standard_user"** in the Username field  
2. Add an extra space after the username  
3. Enter **"secret_sauce"** in the Password field  
4. Click the **"Login"** button

### Expected Results
- Whitespace is trimmed  
- User is redirected to **[Inventory Page](https://www.saucedemo.com/inventory.html)**   
- Product list is displayed

---