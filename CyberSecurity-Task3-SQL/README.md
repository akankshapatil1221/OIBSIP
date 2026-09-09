# TASK 3: SQL Injection on DVWA (Low Security)

## Overview
This project demonstrates a classic SQL Injection (SQLi) vulnerability on **DVWA (Damn Vulnerable Web Application)** running locally under **Low Security** setting. The report details the setup, attack mechanics, payloads used, data exposed, and developer remediation strategies.

---

## 1. Environment & Setup
* **Application**: DVWA (Damn Vulnerable Web Application)
* **Local Web Server**: XAMPP (Apache + MariaDB/MySQL)
* **PHP Version**: 8.x / 7.x
* **Security Level**: Low (`DVWA Security` set to `Low`)

---

## 2. What is SQL Injection (SQLi)?
SQL Injection is a code injection technique where an attacker manipulates application input fields to execute arbitrary SQL queries on the backend database. This occurs when user input is concatenated directly into a database query string without proper sanitization or parameterization.

---

## 3. Attack Execution & Payloads Tested

### Payload 1: Classic True Condition (Data Dumping)
* **Input**: `1' OR '1'='1`
* **Vulnerable Query Pattern**:
  ```sql
  SELECT first_name, last_name FROM users WHERE user_id = '1' OR '1'='1';
  
  Why it works: The condition '1'='1' is always TRUE. This overrides the original WHERE clause logic, forcing the database to return all records stored in the users table.

Exposed Data: All user accounts in the database (User IDs, First Names, Surnames).
### Payload 2: UNION-Based Injection (Credential Extraction)
* **Input: 1' UNION SELECT user, password FROM users #

* **Vulnerable Query Pattern**:
  ```sql
  SELECT first_name, last_name FROM users WHERE user_id = '1' UNION SELECT user, password FROM users #'

  Why it works:

The UNION operator combines the output of the original query with a secondary query targeting sensitive columns (user, password).

The trailing # (comment character in MySQL) truncates the rest of the original application query to avoid syntax errors.

Exposed Data: Usernames and MD5 password hashes (e.g., admin : 5f4dcc3b5aa765d61d8327deb882cf99).

4. Screenshots Evidence
   
01_DVWA_Setup.png - Successful setup of DVWA database on local XAMPP server.

02_Security_Level_Low.png - Verification of DVWA Security set to Low.

03_SQLi_Payload1_Basic.png - Data dumped using basic true condition payload.

04_SQLi_Payload2_Hashes.png - Password hashes extracted using UNION SELECT payload.

5. How to Prevent SQL Injection (Remediation)
   
1. Prepared Statements / Parameterized Queries (Primary Defense)
Developers must treat user input as parameter data rather than executable SQL code.

Insecure PHP Code:
PHP
$id = $_GET['id'];$query = "SELECT first_name, last_name FROM users WHERE user_id = '$id';";
$result = mysqli_query($db,$query);
Secure PHP Code (Using PDO Prepared Statements):
PHP

$id =$_GET['id'];
$stmt =$pdo->prepare('SELECT first_name, last_name FROM users WHERE user_id = :id');
$stmt->execute(['id' =>$id]);
$user =$stmt->fetch();

2. Input Validation & Type Casting
Ensure the expected input strictly matches the data type (e.g., casting id to an integer using intval($_GET['id'])).

3. Principle of Least Privilege
Limit the database user permissions so that the web application cannot execute system-level commands or access unneeded databases.

6. Conclusion
SQL Injection poses a severe security risk by allowing unauthorized access to sensitive database records. Implementing Parameterized Queries (Prepared Statements) completely eliminates this vulnerability.
