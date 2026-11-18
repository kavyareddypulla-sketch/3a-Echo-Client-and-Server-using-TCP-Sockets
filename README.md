## DATE:- 18/11/2026

## NAME:- PULLA KAVYA

## REG NO:- 212225240110

# 3a-Echo-Client-and-Server-using-TCP-Sockets

## AIM

To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM:

Import the necessary modules in python

Create a socket connection to using the socket module.

Send message to the client and receive the message from the client using the Socket module in server .

Send and receive the message using the send function in socket.

## PROGRAM

## CILENT
```
import socket

client = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
client.connect(('localhost', 8000))

while True:
    data = input("Client > ")
    client.sendall(data.encode())

    response = client.recv(1024)
    print("Server > ", response.decode())
```
## SERVER
```
import socket

server = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
server.bind(('localhost', 8000))
server.listen(5)

print("Connection is sucessfully...")
conn, addr = server.accept()

while True:
    message = conn.recv(1024).decode()
    conn.sendall(message.encode())
```

## OUPUT:

## SERVER
<img width="832" height="190" alt="image" src="https://github.com/user-attachments/assets/c90039f7-3fd8-42c9-a154-a5e38afde136" />


## CILENT
<img width="895" height="342" alt="image" src="https://github.com/user-attachments/assets/b4d07823-3998-4bcb-a4db-a6844bad034e" />

## RESULT

Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
