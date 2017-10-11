# videoRTC


A simple video chat client implementation using sockets.


Installation
----------
On one session  
> $ python server.py

Another session
> $ python client.py [optional ip]

For example, if you are doing locally
> $ python client.py

If the server is on a remote machine
> $ python client.py {server-ip}

Working
----------
Sockets and OpenCV are two main things in this app.

Client connects to server socket . PyOpenCV library is used to retrieve frames from webcam feed , they are compressed to jpg to save on the amount of data to be sent across the socket and transmitted . At the other end the image is decompressed and shown. The data being well above 4096 is sent split and reassembled at the other end .

PS : This implementation is two way 
