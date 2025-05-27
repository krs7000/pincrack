Overview:
This project involves a Python script designed to brute-force a 3-digit PIN for a web application. It works by sending raw HTTP POST requests using Python’s socket library, systematically attempting every possible PIN from 000 to 999 until the correct one is discovered.

Solution Approach:

1. Server Details
After launching the executable file (ctf1_for_x86.exe), the server was found running at IP address 172.20.10.3 on port 8888.

2. Server Interaction
The script communicates with the server via an HTTP POST request to the /verify endpoint.
The POST data must include the magicNumber parameter containing the PIN (e.g., magicNumber=123).
A successful attempt returns a response containing the phrase "Access Granted".

3. Managing Server Limitations
The server enforces a delay mechanism after each request.
To prevent being blocked, a delay of 1 seconds (time.sleep(1)) is added between each attempt.

4.Brute-Force Strategy:
Iterate through all 3-digit numbers from 000 to 999.
Send each PIN using raw socket communication.
Check the server’s response for "Access Granted".
Stop once the correct PIN is found.

Instructions to Run:
1. Start the web server by running the ctf1_for_x86.exe file.
2. Open a terminal or command prompt.
3. Run the Python script client.py
