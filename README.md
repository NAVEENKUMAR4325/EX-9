# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

DATE :04-05-2003

AIM :

To write a python program for creating Chat using TCP Sockets Links

ALGORITHM :

1.Import the necessary modules in python

2.Create a socket connection to using the socket module.

3.Send message to the client and receive the message from the client using the Socket module in server

4.Send and receive the message using the send function in socket.


PROGRAM :

CLIENT:

```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

SERVER:

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


OUTPUT :

CLIENT:

![CL9](https://github.com/NAVEENKUMAR4325/EX-9/assets/119479566/ffa334c4-d9cc-4dee-bdb8-37f01b21a70c)

SERVER:

![SE9](https://github.com/NAVEENKUMAR4325/EX-9/assets/119479566/1b2e2829-56d2-402e-8a1c-be5b31784176)





RESULT :

Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed
