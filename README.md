# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
```
client.py

import socket
s=socket.socket()
s.connect(('localhost',9300))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())

    
server.py

import socket
s=socket.socket()
s.bind(('localhost',9300))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg=input("Server > ")
    c.send(msg.encode())
```

## OUPUT:
client.py
<img width="1481" height="288" alt="WhatsApp Image 2026-11-04 at 8 26 35 AM" src="https://github.com/user-attachments/assets/df98678c-9cb9-4544-a6fc-41888ec05ad8" />

server.py
<img width="1483" height="284" alt="WhatsApp Image 2026-11-04 at 8 29 05 AM" src="https://github.com/user-attachments/assets/f15a0b4a-6f6c-44a2-b478-cfd6f71cff6f" />




## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
