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
### client.py
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server.py
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
### client.py
![Screenshot 2024-10-03 141322](https://github.com/user-attachments/assets/3097fc09-c925-44d1-a4bd-424759a77a30)

### server.py
![Screenshot 2024-10-03 141436](https://github.com/user-attachments/assets/2cba697b-8f57-41a3-90d1-4f092c80a99b)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
