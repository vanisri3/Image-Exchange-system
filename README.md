# Image-Exchange-system
This is a Image exhange or sharing system that we created as our project for Distributed System class

This system is about sharing photos where client and server can send the photos through network using the IP Address

# Instruction 
1. First of all this system can run using 1 or 2 Laptop to transfer the data 
2. If using 2 Desktop need to make sure both devices are connected to the same WIFI

# Server Coding Explanation 
1. The server creates a new ServerSocket object on port 9388 and waits for clients to connect.
2. When a client connects, the server creates a new Socket object that represents the connection to the client.
3. The server uses the input stream of the socket to read data from the client, which contains the client's name and the file that the client wants to send.
4. The server continuously reads data from the client and adds it to a DefaultListModel, which is used to display the files on the GUI.
5. The IP address is not specified in the code, so the server will listen for connections on the localhost IP address which manually entered

# Client Coding Explanation 
1. It creates a new Socket object and connects to a server on a specific IP address and port number (9388).
2. When the "connect" button is clicked, the client creates a new Socket object and tries to connect to the specified IP address and port number.
3. Once the connection is established, the client creates an ObjectOutputStream object to send data to the server.
4. When the "send" button is clicked, the client opens a file chooser to select a file, reads the contents of the file into a byte array, creates a new Data object and sets the status, name, and file to send to the server.
5. Finally, it sends the data object to the server using the output stream.
6. The code uses the IP address and port number specified in the text field txtIp and 9388 respectively.
7. The data sent is a file, along with its name and status.

# Process of exchange the photos
1. The server creates a ServerSocket and binds it to a specific port (9388) to waiting for the connections.
2. The client creates a Socket and connects to the server using the IP address and port number.
3. The server uses an ObjectInputStream to read data from the client and a DefaultListModel object to store the received files.
4. The client uses an ObjectOutputStream to send data (in this case, a file, its name, and status) to the server.
5. The server receives this data and stores it in the DefaultListModel object.
6. When the user double-clicks on an item in the list, the server can open the image file by creating a new ShowImage object, and set the received image as the image to be displayed.
7. The server can also save the received file by prompting the user to choose a location and then writing the file to that location.


