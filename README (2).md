
# Port Scanner and SSH Brute Force Script

This Python script performs basic port scanning on a target host and optionally attempts an SSH brute-force attack if port 22 is open.

## ⚠️ Legal Warning

**This script is for educational purposes and authorized penetration testing only.**  
Do not use it against systems you do not have explicit permission to test. Unauthorized access is illegal and unethical.

---

## 🔧 Features

- Scan a range of TCP ports on a target host.
- Identify open ports.
- Attempt SSH brute-force login if port 22 is open, using a supplied username and password list.

---

## 🖥 Sample Usage

```bash
python port_scanner.py 192.168.1.10 --ports 20-25,80,443 --username admin --passwords PasswordList.txt
```

### Command Line Arguments

| Argument        | Description                                  | Default             |
|-----------------|----------------------------------------------|---------------------|
| `target_host`   | Target IP or hostname                        | _Required_          |
| `--ports`       | Comma-separated ports or ranges to scan      | `1-1000`            |
| `--username`    | SSH username for brute-force                 | `root`              |
| `--passwords`   | Path to password list file                   | `PasswordList.txt`  |

---

## 📄 Password List

A sample password list file (`PasswordList.txt`) is included for testing purposes. You can replace it with your own list as needed.

---

## 🛡️ Requirements

- Python 3.x
- `paramiko` library

Install dependencies with:

```bash
pip install paramiko
```

---

## 📂 Files Included

- `port_scanner.py` - Main script
- `PasswordList.txt` - Sample password list
- `sample_output.html` - Example output as HTML
- `README.md` - Project documentation

---

## ✅ Example Output

```
Scanning the ports 20-25,80,443 on 192.168.1.10...
Port 22 is opened.
Port 23 is opened.
Port 80 is opened.
3 opened port(s) found: [22, 23, 80]

Performing SSH BF attack on 192.168.1.10...
Login successful: admin@192.168.1.10:22 with password: admin123
SSH BF attack successful.
```

---

## 👨‍💻 Author

Developed for cybersecurity learning and ethical testing environments.
