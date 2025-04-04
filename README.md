# Keylogger

A **Keylogger** is a software or hardware tool designed to record keystrokes made by a user. It is often used for legitimate purposes like monitoring employees, parental control, and user behavior analytics. However, it can also be misused for unethical or illegal activities like stealing passwords and sensitive information.

---

## Project: Keylogger in Python

### **Objective**
The goal of this project is to develop a Python-based keylogger that records keystrokes and stores them in a log file. Optionally, the keylogger can send logs via email or upload them to a server.

---

## **Technologies Used**
- **Programming Language:** Python  
- **Libraries:** `pynput` (to capture keystrokes), `smtplib` (for sending logs via email), `os`, `time`, `threading`, and `platform`

---

## **Project Features**
✅ **Capture Keystrokes**: Logs every key pressed on the keyboard.  
✅ **Store Logs**: Saves logs in a local file (`.txt` or `.log`).  
✅ **Stealth Mode (Optional)**: Runs in the background without a visible console window.  
✅ **Auto Email Logs (Optional)**: Sends captured keystrokes via email periodically.  
✅ **Upload to Server (Optional)**: Stores logs on a remote server using FTP or a database.  
✅ **Screenshot Capture (Optional)**: Takes periodic screenshots.  

---

## **Implementation Steps**

### **1. Install Dependencies**
```bash
pip install pynput
```

### **2. Capture Keystrokes**
- Use the `pynput.keyboard.Listener` to log keystrokes.
- Convert keystrokes into a readable format.

### **3. Save Data to a File**
- Store logs in a `.txt` or `.log` file.

### **4. Send Logs via Email (Optional)**
- Use `smtplib` to send logs to an email address.

### **5. Run in the Background**
- Hide the console window using `os` functions.

### **6. Convert to Executable (Optional)**
- Use `pyinstaller` to create an executable file.

---

## **Basic Python Keylogger Code**
```python
from pynput.keyboard import Listener

log_file = "keylog.txt"

def on_press(key):
    with open(log_file, "a") as f:
        f.write(str(key) + "\n")

with Listener(on_press=on_press) as listener:
    listener.join()
```

---

## **Enhancements**
✨ Encrypt log files before storing.  
✨ Use threading to send logs without delay.  
✨ Auto-delete logs after sending.  

---

## **Legal & Ethical Considerations**
⚠ **Use Only for Ethical Purposes**: Keylogging without consent is illegal in most countries.  
⚠ **Inform Users**: If used for monitoring, notify the user.  
⚠ **Avoid Misuse**: Unauthorized use can lead to legal consequences.  

---


