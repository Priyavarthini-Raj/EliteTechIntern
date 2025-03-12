# EliteTechIntern
 
EliteTechIntern is a repository dedicated to projects, assignments, and resources from my internship at EliteTech Intern in the field of Cybersecurity. This repository serves as a structured collection of hands-on tasks, research materials, and technical documentation that I have worked on during my virtual internship, contributing to my professional development and industry expertise.

**TOOL 1 : FILE INTEGRITY CHECKER**

File Integrity Checker designed to monitor changes in files by calculating and comparing hash values. It helps detect unauthorized modifications, additions, or deletions of files in a specified directory, making it useful for security monitoring and forensic analysis.

📌 **How It Works**

1️⃣**Calculates File Hashes**
Uses SHA-256 hashing via the hashlib library.
Reads the file in chunks and generates a unique hash.

2️⃣ **Loads Previously Stored Hashes**
Checks for a JSON file (file_hashes.json) that stores hashes from previous runs.
If the file exists, it loads the stored hash values.

3️⃣ **Compares Current vs. Stored Hashes**
If a file’s hash value has changed, it flags it as modified.
If a new file appears, it identifies it as new.
If a file is missing, it reports it as deleted.

4️⃣ **Updates the Hash Database**
After checking, the script updates the file_hashes.json file with the latest hash values for future monitoring.

📌 **How to Use**

**🚀 Running the Script**

1. Save the script as file_integrity_checker.py.
2. Run the script 
3. Enter the directory to monitor when prompted.
4. Check for warnings about modified, new, or deleted files.

🛠 **Example Usage**

**Enter the directory to monitor:** /home/user/documents

**[NEW]** New file detected: /home/user/documents/report.pdf

**[WARNING]** File changed: /home/user/documents/config.txt

**[DELETED]** File missing: /home/user/documents/logs.log

**[INFO]** Integrity check completed.



**TOOL 2 : WEB APPLICATION VULNERABILITY SCANNER**

This Python-based Web Application Vulnerability Scanner is designed to identify common security weaknesses in web applications, such as SQL Injection (SQLi) and Cross-Site Scripting (XSS). The tool automates scanning by analyzing web forms and injecting test payloads to detect vulnerabilities.

**📌 How It Works**

1️⃣ **Extracts Forms from Web Pages**

Uses BeautifulSoup to parse HTML and extract <form> elements.
Identifies input fields where vulnerabilities may exist.

2️⃣ **Tests for SQL Injection (SQLi)**

Injects common SQL payloads like:

       ' OR '1'='1
       '; DROP TABLE users; --
       
If the response suggests database errors or authentication bypass, the form is flagged as vulnerable.

**3️⃣ Tests for Cross-Site Scripting (XSS)**

Injects malicious JavaScript payloads, such as:

             <script>alert('XSS')</script>
             
If the script executes in the browser, it indicates an XSS vulnerability.

**4️⃣ Analyzes Responses**

Compares responses before and after payload injection.
If the payload is reflected in the response without proper sanitization, the tool reports the vulnerability.

**📌 How to Use**

**🔧 Prerequisites**

Ensure you have Python installed, along with the required libraries:

        pip install requests beautifulsoup4
        
**🚀 Running the Script**

1. Save the script as web_vuln_scanner.py.
2. Run the script 
3. Enter the target URL when prompted.
4. Review the output for any detected vulnerabilities.

**🛠 Example Usage**

**Enter the target URL:** http://example.com

[+] Testing 2 forms on http://example.com for SQL Injection...
[!] SQL Injection detected on http://example.com/login using payload: ' OR '1'='1

[+] Testing 2 forms on http://example.com for XSS...
[!] XSS detected on http://example.com/search using payload: <script>alert('XSS')</script>

[INFO] Scanning completed.


