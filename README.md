# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
REG NO: 212223220013

NAME: BASKAR U
## SERVER.PY
```
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)


print(f"Received {data!r}")
```
## CLIENT.PY
```
import socket


HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)
```
## OUTPUT:
## SERVER.PY
![Screenshot 2025-03-20 222937](https://github.com/user-attachments/assets/7e415137-b6e8-4b0f-9fbf-95b19ba15bdf)

## CLIENT.PY
![Screenshot 2025-03-20 222902](https://github.com/user-attachments/assets/3ed72027-799c-4425-b21a-c2019b7c1980)

## RESULT:
The program is executed successfully
