## What is SQLMap?

SQLMap is an open-source penetration testing tool that automates the process of detecting and exploiting SQL injection vulnerabilities in database systems. It is widely used by security professionals to perform ethical hacking and vulnerability assessments. 

### Uses of SQLMap:
- Detect and exploit SQL injection vulnerabilities in web applications.
- Retrieve information from the database such as tables, columns, and data.
- Bypass web application firewalls (WAF) and filters using tamper scripts.
- Automate SQL injection testing for large-scale assessments.
- Extract sensitive data like user credentials or confidential records.
- Test and validate the security of database-driven applications.
- Gain insights into the database structure for further analysis.

## Common Options

- `--dbs` : **List all databases** present. Use this to see the databases available on the target server.
- `--banner` : **Retrieve the database version**. Helps identify the DBMS type and version.
- `--batch` : **Automate the process** (SQLMap won't prompt for user inputs). Useful for running SQLMap in non-interactive mode.
- `--tables` : **Get table names** in the current or specified database. Helpful for discovering the schema.
- `-D <database>` : **Specify a database** to target. Used in conjunction with other options to focus on a specific database.
- `-t <table>` : **Specify a table** to target.
- `--dump-all` : **Dump all data** from the specified table or database. Extracts information from the database.
- `--cookie <cookie>` : **Specify cookie information** (e.g., for authentication). Obtain the cookie by inspecting the web element in your browser.
- `--wizard` : **Enable a user-friendly interface**. Great for beginners who want step-by-step guidance.
- `--list-tamper` : **List available tamper scripts**. Shows tampering modules to evade detection or bypass filters.
- `--random-agent` : **Use a random user agent**. Helps disguise SQLMap requests as originating from various devices or browsers.
- `--tamper <module>` : **Enable a tamper module** to bypass WAF/filters. For example, to obfuscate SQL queries.
- `--mobile` : **Simulate a mobile device**. Useful for websites that serve different content based on the user agent.
- `--crawl <level>` : **Crawl for links** related to the provided URL. Levels can be 1, 2, or 3 for increasing depth.
- `--columns` : **List column names** of a table. Useful to understand the structure of a table.
- `--count` : **Count the total number of records** in a table. Helps gauge the amount of data.

## SQL Shell Options

- `--sql-shell` : **Open an interactive SQL shell**. Allows running SQL queries directly on the database.

### Common SQL Commands in Shell

1. `database();`  
   **Retrieve database information** like the current database name.

2. `SELECT table_name FROM information_schema.tables WHERE table_schema = 'database_name';`  
   **List table names** in the specified database. Useful for exploring database schemas.

3. `SELECT * FROM database_name.table_name;`  
   **Retrieve all records** from the specified table. Be cautious, as large tables may return significant amounts of data.

4. `x`  
   **Exit the SQL shell**. Ends the interactive SQL session.

---

### Key Notes:
- Always check for authorization before testing a website to ensure ethical use.
- Combine multiple options (e.g., `-D`, `--tables`, `--columns`) for targeted attacks to minimize noise.
- Use tamper scripts wisely to bypass advanced protections or obfuscate queries.
