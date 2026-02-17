# Qlubi — Full System Setup & Operation Guide

This guide explains the complete process required to get Qlubi fully operational.

Qlubi relies on four coordinated components:

- MQTT Broker  
- HTTP Server  
- Sensor Logger App (Heart Rate Source)  
- Lolin S2 Mini Board (Qlubi Device)  

All components must be configured correctly for full functionality.

---

# Step 1 — Establish an MQTT Broker

Qlubi requires an active MQTT broker to manage communication between devices.

If you already operate an MQTT broker, you may use that.

If not, this resource provides detailed comparisons of free MQTT broker options:

https://sourceforge.net/software/mqtt-brokers/free-version/#

Choose a broker that supports:

- Public or hosted deployment  
- Custom topic configuration  
- Username/password authentication (recommended)  
- Stable uptime  

---

## Configure Your Broker

Once your broker is established:

1. Create your broker instance.
2. Define:
   - Broker URL (domain or IP)
   - Broker port
   - Username (if required)
   - Password (if required)
3. Save these details.

You will paste these values into:

- Board code  
- Laptop HTTP bridge code  
- Server configuration  

Without matching credentials across all systems, communication will fail.

---

# Step 2 — Install and Configure Sensor Logger

Qlubi uses **Sensor Logger** as the heart rate data source.

Official website:  
https://www.tszheichoi.com/sensorlogger

Download Sensor Logger from your device’s app store and install it.

Sensor Logger must be connected to your smartwatch or heart rate monitor.

---

## Sensor Logger Configuration

After installation:

1. Connect your smartwatch or heart rate monitor.
2. Enable **heart rate monitoring only** (disable unnecessary sensors).
3. Open **Settings** in Sensor Logger.
4. Enable **Data Streaming (HTTP Push)**.
5. Enter:
   - Your HTTP server URL
   - Your HTTP server port

⚠ Important:

- The HTTP server IP and port may change depending on your network.
- Always verify these values before starting a session.
- Your phone/device and HTTP server must be on the same internet connection.

If they are not on the same network, data will not reach your server.

---

# Step 3 — Prepare the HTTP Server

Your HTTP server must be:

- Running  
- Listening on the configured port  
- Accessible from your phone/device  
- Configured to relay or process data as required  

If your HTTP server is not running:

- Qlubi devices may still communicate via MQTT.
- However, no heart rate data will be processed.
- No stress detection will trigger alerts.

For full functionality, the HTTP server must be active.

---

# Step 4 — Prepare the Qlubi Board

Ensure:

- CircuitPython is installed.
- Board code includes:
  - WiFi credentials  
  - Broker URL  
  - Broker port  
  - Device identifier  
- The board connects successfully to WiFi.
- The board connects successfully to MQTT.

Power on the Qlubi device before beginning use.

---

# Step 5 — Starting a Session

To fully activate Qlubi:

1. Power on your Qlubi device.
2. Start your HTTP server.
3. Open Sensor Logger.
4. Begin a heart rate recording session.

Once recording begins:

- Heart rate data is pushed to your HTTP server.
- The server processes incoming data.
- If distress thresholds are reached:
  - MQTT messages are triggered.
  - Connected Qlubi devices activate.

---

# Important Operational Notes

- Qlubi devices can communicate via MQTT even if the HTTP server is not running.
- Without the HTTP server:
  - No heart rate tracking occurs.
  - No stress detection occurs.
  - No distress alerts will be triggered.

To enable full functionality:

- Sensor Logger must be actively recording.
- HTTP server must be running.
- MQTT broker must be online.
- Board must be powered and connected.

---

# Daily Use Workflow

When sitting down to work:

1. Power on Qlubi.
2. Verify WiFi connection.
3. Confirm HTTP server is running.
4. Start heart rate recording in Sensor Logger.
5. Confirm data is being received by the server.

Qlubi will now monitor stress levels and activate alerts when thresholds are exceeded.

The more Qlubis in one's network the better the device experience so feel free to set them up for friends and family

---

# Troubleshooting Checklist

If alerts are not triggering:

- Confirm MQTT broker is online.
- Confirm broker credentials match across all systems.
- Confirm HTTP server is running.
- Confirm correct IP and port are set in Sensor Logger.
- Confirm Sensor Logger is actively recording.
- Confirm all devices are on the same network.
- Check firewall settings.
- Verify board serial output for connection errors.

---

Once all systems are synchronized, Qlubi will operate as a live stress-aware communication device.
