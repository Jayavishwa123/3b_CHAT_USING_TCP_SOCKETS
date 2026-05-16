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
SERVER.PY:
```
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
CLIENT.PY
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUTPUT
<img width="1852" height="214" alt="image" src="https://github.com/user-attachments/assets/b5b82f89-c529-4653-ab1e-a42a71547b51" />
<img width="1865" height="237" alt="image" src="https://github.com/user-attachments/assets/985bda03-bec4-4e98-8a59-730b9b807542" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
