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
```
CLIENT

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
```
SERVER

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

## OUPUT

CLIENT

![436598943-4370ffea-3654-4036-9d8f-ce7feed2a01b](https://github.com/user-attachments/assets/d2b09874-d50b-43a7-9fcb-08d6d5f804da)

SERVER

![436599107-d3399aff-f016-43cc-ab32-ef3a87e8de46](https://github.com/user-attachments/assets/71ccc5e1-e30a-474a-8b2c-6916f9e30fba)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
