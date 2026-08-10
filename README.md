CONNECT ESP32 TO WIFI
This is the most important step for integration.
Your ESP32 needs internet access so it can:
• send live data,
• sync with the dashboard,
• and update the app.
 
BASIC FLOW
ESP32
 ↓
WiFi
 ↓
FastAPI Backend
 ↓
Website / Mobile App
 
SEND DATA TO THE WEBSITE
Your ESP32 should send 
JSON data using HTTP POST requests.
Example:
{
 "module": "SafeCharge",
 "status": "Unsafe",
 "voltage": 6.2,
 "current": 2.5

WHAT YOUR TEAMMATES MUST BUILD
Ask them for:
1. Backend API URL
Example:
https://thabashield-api.com/safecharge
OR locally:
http://192.168.1.5:8000/safecharge
 
ESP32 CODE STRUCTURE
Your ESP32 code should:
Loop
1. Read voltage
2. Read current
3. Determine SAFE/UNSAFE
4. Activate LED/buzzer
5. Send JSON to backend
6. Repeat every few seconds
 
HOW THE WEBSITE DISPLAYS DATA
The frontend team should create:
• status cards,
• live readings,
• alert notifications,
• event logs.
 
EXAMPLE WEBSITE PANEL
SAFECHARGE PANEL
Metric

Value

Voltage

5.1V

Current

1.8A

Status

SAFE

Last Alert

None

If unsafe:
Status

UNSAFE

LED

RED

Alert

Triggered
