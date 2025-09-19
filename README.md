# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:

## SERVER:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5) c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode() if
ack:
 print(ack)
 continue
else:
 c.close()
 break
```
## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
print(s.recv(1024).decode())
s.send("Acknowledgement Recived".encode())

```


## OUTPUT
# SERVER:
<img width="628" height="227" alt="Screenshot 2025-09-19 104946" src="https://github.com/user-attachments/assets/7367be12-bf63-49af-9daf-4e881f081328" />

# CLIENT:
<img width="625" height="237" alt="Screenshot 2025-09-19 104956" src="https://github.com/user-attachments/assets/db8f1a62-f3a8-4427-b4f4-4979c1b4af2e" />





## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
