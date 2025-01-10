# **NetRiskScanner**

The **NetRiskScanner** is an advanced yet user-friendly graphical user interface built with Python using `tkinter` and `ttkbootstrap`. Designed for network professionals, ethical hackers, and IT enthusiasts, this tool provides seamless interaction with the powerful Nmap scanning utility. It simplifies complex network scanning and risk assessment processes, offering real-time results and actionable insights.

---

## **Features**

### **1. Comprehensive Nmap Scanning**
- **Supports Various Scan Types:**
  - SYN Scan (`-sS`)
  - TCP Connect Scan (`-sT`)
  - Ping Scan (`-sn`)
  - UDP Scan (`-sU`)
  - Null Scan (`-sN`)
  - FIN Scan (`-sF`)
  - Xmas Scan (`-sX`)
  - ACK Scan (`-sA`)
  - Window Scan (`-sW`)
  - IP Protocol Scan (`-sO`)
- **Advanced Options:**
  - OS detection (`-O`)
  - Service detection (`-sV`)
  - Aggressive scan mode (`-A`)
  - Disable ping (`-Pn`)
  - Verbose output (`-v`)

---

### **2. Real-Time Results Display**
- **Side-by-Side Panels:**
  - **Left Panel:** Displays live scan results in real-time.
  - **Right Panel:** Provides a detailed risk assessment based on vulnerabilities found during the scan.
- Progress bar for tracking scan completion.

---

### **3. AI-Powered Risk Assessment**
- **Automated Analysis:** Uses AI models to analyze scan results and detect potential vulnerabilities.
- **Threat Prioritization:** Assigns risk scores to vulnerabilities to help users focus on critical issues.
- **Insights and Recommendations:**
  - Provides actionable steps to mitigate identified risks based on industry best practices.
  - Suggests patches, configuration changes, or system hardening techniques.
- **Continuous Improvement:** Learns from previous scans to enhance future risk assessments.

#### **How Risk Assessment Works**
1. **Scan Results Analysis:**
   - Parses the raw Nmap scan output to identify open ports, running services, and their versions.
   - Matches findings with known vulnerabilities from a vulnerability database (e.g., CVE database).
2. **Risk Scoring:**
   - Assigns a risk score to each finding based on its severity, exploitability, and potential impact.
   - Scores are categorized as Low, Medium, High, or Critical.
3. **Mitigation Recommendations:**
   - For each identified vulnerability, the tool provides mitigation strategies such as:
     - Updating or patching software.
     - Closing unnecessary open ports.
     - Restricting access using firewall rules.
     - Disabling or reconfiguring vulnerable services.
   - Provides links to official patches or detailed guides for resolution where applicable.

---

### **4. Export Options**
- Save scan results and risk assessments to `.txt` or `.json` files for record-keeping or further analysis.

---

### **5. Customizable Themes**
- Switch between **light mode** (`united`) and **dark mode** (`cyborg`) for personalized usability.

---

## **Prerequisites**

Ensure the following are installed and set up on your system:

### **1. Python**
- **Python 3.8 or higher** is required. Download it from [Python Official Website](https://www.python.org/downloads/).

### **2. Nmap**
- Ensure Nmap is installed on your system. Download it from [Nmap Official Website](https://nmap.org/download.html).
- Verify installation by running:
    ```bash
    nmap --version
    ```

### **3. Required Python Libraries**
- The required Python libraries are listed in the `requirements.txt` file. They include:
  - `ttkbootstrap` for modern GUI components.
  - `tkinter` for core GUI functionalities.

---

## **Installation**

Follow these steps to set up and run the NetRiskScanner:

### **1. Clone the Repository**
```bash
git clone https://github.com/yourusername/NetRiskScanner.git
cd NetRiskScanner
```

---

### **2. Install Python Libraries**
```bash
pip install --break-system-packages -r requirements.txt
```

---

### **3. Verify Nmap Installation**
```bash
nmap --version
```

# Usage

## 1. Launching the Tool

Run the tool with the command:
```bash
python Nmap_Main.py
```

## **2. Configuring Scans**

Enter Target Information:

- Specify the target IP address, domain name, or CIDR range in the Target field.
- Optionally, specify a port range (e.g., 20-80) and spoof MAC address.
- Select Scan Type:
- Choose from the available scan types (e.g., SYN Scan, TCP Connect, UDP Scan) in the dropdown menu.
- Enable Advanced Options:
- Enable features like OS detection, service scan, verbose output, or disable ping.


## **3. Executing the Scan**

- Click the Start Scan button to begin scanning.
- Monitor the scan progress with the progress bar.
- View:
  -  Scan Results in the left panel.
  -  Risk Assessment in the right panel.


## **4. Exporting Results**

Save results by navigating to:

File > Export Results

## Export options:

- .txt (plaintext format)
- .json (structured format)

## Tool Structure :

### **1. Core Files :**

- Nmap_Main.py: Main application file for the GUI interface.
- utils: helper functions for Tool.
  - ```validator.py```: Validates target inputs like IP addresses, port ranges, and MAC spoofing.
  - ```nmap_runner.py```: Builds and executes Nmap commands.

### **3. Requirements**

```requirements.txt```: Contains all necessary Python dependencies.
