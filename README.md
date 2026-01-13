# OrangeHRM-login
OrangeHRM login functionality (Manual Test)

Test Environment Details
Browser: Google Chrome (Version 143.0.7499.170 (Official Build) (64-bit)
Application Version: OrangeHRM OS 5.7
Platform: Windows 11
URL:(https://opensource-demo.orangehrmlive.com/web/index.php/auth/login)

TC01 – Valid Login Credentials
Objective: Verify Administrator can log in with correct credentials.

Steps:

1. Navigate to the login page.

2. Enter valid username: Admin

3. Enter valid password: admin123

4. Click the "Login" button.

Expected Result: User is redirected to the dashboard.
Actual Result: Login successful redirected to the dashboard
https://github.com/Sudoapt-getjared/OrangeHRM-login/blob/main/README.md

TC02 – Valid Login Credentials
Objective: Verify Standard user can log in with correct credentials.

Steps:

1. Navigate to the login page.

2. Enter valid username: Jaredp01

3. Enter valid password: Orange123!

4. Click the "Login" button.

Expected Result: User is redirected to the dashboard.
Actual Result: Login successful redirected to the dashboard

Negative Test Cases
TC03 – Invalid Username
Objective: Verify login fails with incorrect username.

Steps:

1. Enter username: WrongUser

2. Enter password: admin123

3. Click "Login".

Expected Result: Error message appears: “Invalid credentials.”
Actual Result: Error message: “Invalid credentials”

TC04 – Invalid Password
Objective: Verify login fails with incorrect password.

Steps:

1. Enter username: Admin

2. Enter password: Wrongpass

3. Click "Login".

Expected Result: Error message appears: “Invalid credentials.”
Actual Result: Error message: “Invalid credentials”

TC05 – Case sensitive password
Objective: Verify that the application correctly enforces case sensitivity in the password field during login authentication.

Steps:

1. Enter username: Admin

2. Enter password: Admin123

3. Click "Login".

Expected Result: Error message appears: “Invalid credentials.”
Actual Result: Error message: “Invalid credentials”

TC06 – Verify login credentials are not retained after logout
Objective: To ensure that after logging out of the application, the username and password fields are cleared and not auto-filled on return to the login page

Steps:

Enter username: Admin

Enter password: Admin123

1. Once logged in, click Logout

2. Return to the login page (Using browser back button)

3. Observe the login form fields

Expected Result: Blank login fields after logging in and manually pushing browser back button
Actual Result: Login credentials retained in both fields

TC07 – Empty Fields
Objective: Verify login fails when both fields are empty.

Steps:

1. Leave username and password blank.

2. Click "Login".

Expected Result: Error message or validation prompt appears.
Actual Result: Error message – “Required” for both missing fields

TC08 – Only Username Entered
Objective: Verify login fails when password is missing.

Steps:

1. Enter username: Admin

2. Leave password blank.

Click "Login".

Expected Result: Error message or validation prompt appears.
Actual Result: Error message - “Required” for missing password field.

TC09 – Only Password Entered
Objective: Verify login fails when username is missing.

Steps:

1. Leave username blank.

2. Enter password: admin123

Click "Login".

Expected Result: Error message or validation prompt appears.
Actual Result: Error message – “Required” for missing username field.

Security & Session Test Cases
TC10 – Session Timeout
Objective: Verify session expires after inactivity.

Steps:

1. Log in with valid credentials.

2. Remain inactive for 30 minutes.

Expected Result: User is logged out and redirected to login page.
Actual Result: Redirected to logout page

