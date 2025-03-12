# EliteTechIntern
 
EliteTechIntern is a repository dedicated to projects, assignments, and resources from my internship at EliteTech Intern in the field of Cyber Forensics, Information Security, and Cybersecurity. This repository serves as a structured collection of hands-on tasks, research materials, and technical documentation that I have worked on during my virtual internship, contributing to my professional development and industry expertise.

**File Integrity Checker**

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
