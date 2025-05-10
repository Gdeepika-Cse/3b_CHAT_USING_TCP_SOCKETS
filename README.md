# NAME: DEEPIKA G
# REG.NO: 212224040060

# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client.py
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## server.py
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUTPUT
## client.py
![client (1)](https://github.com/user-attachments/assets/17a8d4bb-76e0-4c01-9805-29573529575f)

## server.py
![server (1)](https://github.com/user-attachments/assets/f1db5ac7-0a2a-4fda-a562-e89b1d3ff855)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
