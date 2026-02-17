# Laptop/PC HTTP Code Setup Guide

This folder contains the Laptop/PC HTTP code required to connect your Qlubi device to your HTTP server infrastructure to connect your app to your MQTT server broker and protecting your data..

To run this code, users must first configure a local Python environment on their computer.

This guide outlines the full setup process.

---

# Step 1 — Install a Python interpreter

You will need a Python IDE or runtime environment to execute the code in this folder.

You may use any Python interpreter of your choice.

One recommended option is **PyCharm**, which is stable and beginner-friendly.

Download PyCharm here:  
https://www.jetbrains.com/pycharm/

Install the Community Edition unless you require advanced features.

---

# Step 2 — Prepare the Project

Once PyCharm (or your chosen runner) is installed:

1. Open the application.
2. Create a new Python project.
3. Open the main Python file provided in this folder.
4. Copy the contents of the code.
5. Paste the code into your new project file.

Ensure the file is saved with a `.py` extension.

---

# Step 3 — Configure the Code for Your Setup

Before running the script, you must modify the configuration variables to match your system.

Specifically update:

- Device ID
- Board details
- Server address (IP or domain)
- Port configuration (if applicable)
- Any authentication keys or tokens

Refer to the provided reference image in this repository to see where these fields are located in the code.

Failure to update these values will prevent proper communication between:

- Laptop client
- Server
- Board (Lolin S2 Mini)
- Application interface

---

# Step 4 — Run the Script

After configuration:

1. Click **Run** in your Python environment.
2. The IDE may prompt you to install missing libraries.

Accept all required library installations.

Typical libraries may include:

- `requests`
- `flask`
- `json`
- `time`
- `threading`
- or other networking dependencies

Allow the environment to complete installation.

---

# Step 5 — Re-run the Script

Once all dependencies are installed:

1. Run the script again.
2. Confirm that no import errors occur.
3. Observe the console output for successful server communication messages.

If correctly configured, the HTTP client should now be operational.

---

# Final System Check

Before active use, ensure:

- Server is running
- Board is powered and connected to WiFi
- App interface is active
- Correct IP addresses are configured
- Firewall settings are not blocking communication

All three components — **server, app, and board** — must be operational for full functionality.

---

# Troubleshooting

If the script does not run:

- Confirm Python is installed on your system
- Confirm the correct interpreter is selected in your IDE
- Confirm libraries installed successfully
- Verify server address is reachable
- Check that port numbers match your server configuration

---

Once complete, your Laptop7PC HTTP bridge should be fully operational and ready for integration with Qlubi.
