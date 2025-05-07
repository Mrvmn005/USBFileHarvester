# USBFileHarvester

This PowerShell script scans all local drives for files with a specified extension (e.g., .txt),
copies them to a temporary folder, compresses them into a ZIP archive, and saves the archive to a 
USB drive labeled by the user. It is designed for ethical use in data collection, audits, backups, 
or forensic training environments.

===================================================
      USBFileHarvester Script - Instructions
===================================================

📌 Purpose:
This script searches all local drives for files with a specific extension 
(e.g., *.txt), copies them to a temporary folder, compresses them into a ZIP file, 
and saves the ZIP to your USB drive.

---------------------------------------------------
🔧 Setup Steps:
---------------------------------------------------
1. CHOOSE A LABEL FOR YOUR USB DRIVE:
   - Your USB can be labeled anything you want (e.g., BadUSB, TOOLKIT, SECUREUSB).
   - To label the drive:
     - Open File Explorer
     - Right-click your USB drive
     - Click "Properties"
     - Set the "Label" to your desired name (e.g., MYUSB), then click OK

2. EDIT THE PowerShell SCRIPT:
   - Open `USBFileHarvester.ps1` in Notepad
   - Find this line:
       `$usbLabel = "DUCKYDRIVE"`
   - Change `"BadUsb"` to the **label you gave your USB drive**
     (e.g., `"MYUSB"`, `"SECUREUSB"`, etc.)

   - OPTIONAL: To target a different file type, edit this line:
       `$targetExtension = "*.txt"`
     Replace `.txt` with `.jpg`, `.docx`, etc.

3. RENAME THE FILES:
   - If you downloaded or saved the script as `USBFileHarvester.txt`, **rename it to**:
       `USBFileHarvester.ps1`
   - If you saved the launcher as `Launcher.txt`, **rename it to**:
       `Launcher.vbs`

4. PLACE THESE FILES ON THE ROOT OF YOUR USB:
   - `USBFileHarvester.ps1`       ← The main PowerShell script
   - `Launcher.vbs`               ← (Optional) Runs the script silently
   - `Instructions.txt`           ← (This file, for reference)

---------------------------------------------------
▶️ How to Run the Script:
---------------------------------------------------
🔹 Option 1: Visible Method (PowerShell)
   - Double-click `USBFileHarvester.ps1`
   - This opens a PowerShell window showing progress

🔹 Option 2: Stealth Mode (VBS Launcher)
   - Double-click `Launcher.vbs`
   - This runs the script **silently** (no window)
   - You'll get a small popup once the ZIP file is saved

---------------------------------------------------
📁 What Happens:
---------------------------------------------------
- The script searches all local drives (C:\, D:\, etc.) for files matching your chosen extension
- Matching files are copied to a temporary folder
- The collected files are zipped and saved to your USB as:
    `CollectedFiles.zip`
- The temporary folder is deleted automatically after completion

---------------------------------------------------
⚠️ Important Reminders:
---------------------------------------------------
- This tool is for ethical, authorized use only
- Do **not** use on systems you do not own or have permission to audit
- Useful for:
   - Digital forensics
   - Disaster recovery
   - Internal file audits
   - Training in cybersecurity labs

---------------------------------------------------
💡 Optional: Enable AutoRun (Legacy Support Only)
---------------------------------------------------
To make the script run automatically when the USB is inserted (on older Windows versions):

1. Download and install **USB AutoRun Creator** (from a trusted source)
2. Set the launcher (`Launcher.vbs`) as the auto-run file
3. Note: AutoRun is blocked by default on modern Windows versions for security reasons

===================================================
✅ Created for Responsible and Educational Use Only
===================================================
