# Log Analysis Script

## Project Description
This project is a Python script designed to analyze web server log files for critical insights. The script focuses on extracting meaningful information to aid in cybersecurity and operational assessments. It demonstrates key Python skills like **file handling**, **string manipulation**, and **data analysis** while addressing challenges such as identifying suspicious activity, analyzing user behavior, and summarizing endpoint access patterns.

---

## Table of Contents
1. [Objective](#objective)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Output Details](#output-details)
6. [Evaluation Criteria](#evaluation-criteria)
7. [Author](#author)

---

## Objective
The primary goal of this script is to:
- Process log files to extract valuable insights.
- Automate tasks like identifying suspicious activities and determining user behavior trends.
- Produce a clean, structured output in the terminal and a CSV file for reporting purposes.

---

## Features
The script implements the following functionalities:
1. **Count Requests per IP Address**:
    - Parses the log file to identify unique IP addresses and their request counts.
    - Sorts the results in descending order of request counts for quick interpretation.

2. **Identify the Most Frequently Accessed Endpoint**:
    - Extracts all accessed endpoints from the log file.
    - Highlights the most frequently accessed endpoint along with its access count.

3. **Detect Suspicious Activity**:
    - Identifies potential brute force login attempts:
        - Flags IP addresses with failed login attempts exceeding a configurable threshold (default: 10).
    - Detects log entries indicating failed login attempts using HTTP status codes (`401`) or failure messages.

4. **Output Results**:
    - Displays findings in an organized format in the terminal.
    - Saves results to a CSV file named `log_analysis_results.csv` with the following structure:
        - **Requests per IP**: `IP Address`, `Request Count`
        - **Most Accessed Endpoint**: `Endpoint`, `Access Count`
        - **Suspicious Activity**: `IP Address`, `Failed Login Count`

---

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repository-name.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Log-Analysis-Script
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

---

## Usage
1. Place the log file in the project directory.
2. Run the script by providing the log file as an argument:
   ```bash
   python log_analysis.py <logfile>
   ```
3. View the results in the terminal and check the `log_analysis_results.csv` for a detailed report.

---

## Output Details
The script generates the following:
1. **Terminal Output**:
    - Count of requests per IP, sorted in descending order.
    - The most frequently accessed endpoint and its count.
    - Suspicious activities with flagged IPs and failed login counts.

2. **CSV File**:
    - **log_analysis_results.csv** with:
        - Requests per IP: `IP Address`, `Request Count`
        - Most Accessed Endpoint: `Endpoint`, `Access Count`
        - Suspicious Activity: `IP Address`, `Failed Login Count`

---

## Evaluation Criteria
1. **Functionality**:
    - Properly implements all required analysis features.
    - Handles the provided log file accurately and efficiently.
2. **Code Quality**:
    - Follows Python best practices with clean, modular, and well-commented code.
    - Uses meaningful variable names and clear function definitions.
3. **Performance**:
    - Processes large log files without significant delays.
4. **Output**:
    - Displays a structured and accurate terminal output.
    - Creates a correctly formatted CSV file matching specifications.

---

## Author
This project was developed by **Avanindra Vijay**.
