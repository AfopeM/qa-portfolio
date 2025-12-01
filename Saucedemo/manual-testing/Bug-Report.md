# Bug Reports – [Sauce Demo](https://www.saucedemo.com/)

**Testing Date**: 20-11-25
**Tester**: Afope Matilukuro
**Bugs Documented**: 1

### BUG-001: Login Fails When Valid Credentials Include Extra Whitespace

**Severity**: Medium

**Priority**: P3

**Status**: Open

**Environment**:

- Browser: Brave 1.84.141
- Operating System: Windows 11
- Device type: Desktop
- Test Account: standard_user

**Preconditions**:

- User is on **[Home Page](https://www.saucedemo.com/)**
- User is **not logged in**

**Steps to Reproduce**:

1. Enter **valid username** in the Username field
2. Add an extra space after the username
3. Enter **valid password** in the Password field
4. Click the **Login** button

**Expected Result**:

- Whitespace in the username field is **trimmed**
- User is redirected to
  **[Inventory Page](https://www.saucedemo.com/inventory.html)**
- Product list is displayed

**Actual Result**:

- User remains on **[Home Page](https://www.saucedemo.com/)**
- Username and password field remain the same
- System displays error message:**"Epic sadface: Username and password do not match any user in this service"**

**Evidence**:![Login Page](screenshots/BUG-001-whitespace-login.png)
