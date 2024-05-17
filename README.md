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
## PROGRAM
## client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
  i=input("Enter a data: ")
  c.send(i.encode())
  ack=c.recv(1024).decode()
  if ack:
    print(ack)
    continue
  else:
    c.close()
    break
```
## OUTPUT
## client:
![321726208-f6c7607d-7e9c-4142-a30e-def35b72db2c](https://github.com/Rithviknathan/2a_Stop_and_Wait_Protocol/assets/148410509/f3dc81bb-d12c-4723-a52d-c1f69f41fd28)
## server:
![321726297-553fc679-cac0-47e7-b3f3-4d6e592d134d](https://github.com/Rithviknathan/2a_Stop_and_Wait_Protocol/assets/148410509/3ad37779-4dc8-4b5e-81a0-87096efaeef9)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
