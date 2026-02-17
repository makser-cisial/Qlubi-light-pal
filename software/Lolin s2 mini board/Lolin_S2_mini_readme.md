# Qlubi Board Code Setup Guide (Lolin S2 Mini)

This folder contains the CircuitPython board code required to run Qlubi on the Lolin S2 Mini.

Before uploading this code, users must first prepare their board with CircuitPython and configure it to match their WiFi network and server.

This guide outlines the full setup process from firmware installation to final deployment.

---

# Step 1 — Install CircuitPython on the Lolin S2 Mini

The Lolin S2 Mini must be running CircuitPython before the board code will function.

Follow the official installation guide here:

https://circuitpython.org/board/lolin_s2_mini/

Follow the flashing instructions provided on that page to install the correct UF2 firmware.

After successful installation:

- The board should mount as a USB drive named `CIRCUITPY`
- Default files such as `code.py` should be visible

Do not proceed until CircuitPython is properly installed and the board mounts correctly.

---

# Step 2 — Download and Configure the Board Code

Download the board code from this folder.

Before transferring it to the board, you must edit the configuration values to match your setup.

Update:

- WiFi SSID
- WiFi password
- Server IP address or domain
- Server port (if required)
- Device/board identifier
- HTTP endpoint configuration

If these values are not set correctly, the board will not connect to your network or server and will not function.

Ensure each board has a unique identifier if running multiple devices.

![](https://github.com/makser-cisial/Qlubi-light-pal/blob/main/software/Lolin%20s2%20mini%20board/images/what%20to%20change.png)

---

# Step 3 — Upload the Code to the Board

You have two supported upload methods.

---

## Option 1 — Manual File Copy

1. Connect the Lolin S2 Mini to your computer.
2. Open the `CIRCUITPY` drive.
3. Replace the existing `code.py` file with the configured version from this folder.
4. Copy any additional required files into the root directory.

Ensure the main script file is named:

code.py


CircuitPython automatically runs `code.py` on boot.

---

## Option 2 — Recommended: Use Mu Editor

For easier debugging and serial monitoring, Mu Editor is recommended.

Download Mu here:

https://codewith.mu/

### Using Mu:

1. Open Mu.
2. Select CircuitPython mode.
3. Connect your board.
4. Paste the board code into the editor.
5. Press **Save** and save directly to the board as `code.py`.

Mu allows you to:

- Establish a live serial connection
- View runtime output
- Debug connection issues
- Monitor errors in real time

This is the recommended method for development and troubleshooting.

---

# Step 4 — Replace the `lib` Folder

The board requires specific CircuitPython libraries.

You must:

1. Delete any existing `lib` folder on the `CIRCUITPY` drive.
2. Copy the `lib` folder provided in this repository onto the board.

Your board file structure should look like:

CIRCUITPY/
│
├── code.py
├── lib/
│ ├── (required CircuitPython libraries)


If required libraries are missing, the board will display `ImportError` messages on startup.

---

# Step 5 — Power and Test

Once:

- CircuitPython is installed
- `code.py` is uploaded
- WiFi and server values are configured
- `lib` folder is correctly replaced

Reset the board.

If configured correctly:

- The board should connect to WiFi
- It should establish HTTP communication with your server
- Serial output (via Mu) should confirm successful connection

---

# Final System Check

Before full operation, confirm:

- Server is running
- HTTP endpoint is active
- Laptop7PC HTTP bridge (if used) is running
- WiFi credentials are correct
- Firewall is not blocking outbound requests

The board depends on a reachable server to function correctly.

---

# Troubleshooting

If the board does not operate as expected:

- Recheck WiFi credentials
- Confirm server IP address and port
- Verify correct HTTP endpoint path
- Ensure the `lib` folder contains required libraries
- Monitor serial output in Mu for error messages
- Confirm CircuitPython version matches library compatibility

---

Once all steps are complete, your Lolin S2 Mini should be fully configured and ready to operate within the Qlubi system.
