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

### Client:
```
import socket
s=socket.socket()
s.connect(('localhost',3080))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

```

### Server:
```
import socket
s=socket.socket()
s.bind(('localhost',3080))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```
## OUTPUT
### Client:
![Screenshot 2024-04-29 133934](https://github.com/Anas536/3b_CHAT_USING_TCP_SOCKETS/assets/139841834/4f9da8c8-4e05-4499-854f-4020e60685a0)

### Server:
![Screenshot 2024-04-29 133940](https://github.com/Anas536/3b_CHAT_USING_TCP_SOCKETS/assets/139841834/c84aacfe-141c-4fd6-b473-c438e750e9cf)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
