# HoneyPot


Objective

The objective of this project is to create a basic honeypot. A honeypot is a security mechanism that acts as a decoy to attract attackers, detect intrusion attempts, and gather information about potential threats. This honeypot will listen on a specific port, log details of any incoming connections, and respond to the attacker, simulating a vulnerable service.


Skills Learned

- ' Networking Basics '- Understanding how to use sockets in Python to establish network connections.
- ' Security Concepts '- Learning about honeypots and their role in cybersecurity for detecting and analyzing threats.
- ' Python Programming '- Using Python's standard libraries to create a network-based application, handle connections, and log data.
- ' File Handling '- Write logs for a file for later analysis.


Tools Used

- ' Python 'is the programming language used to develop the honeypot.
- ' Socket Library '- A Python library for low-level networking interface to create and manage connections.
- ' Datetime Library '- A Python library to manage and format date and time data, used for logging.
- ' Text Editor/IDE'-  Any code editor like VS Code, PyCharm, or even a simple text editor to write and execute the Python script.

Step-By-Step

Ref 1 - Importing Libraries




![Importing Libraries](https://github.com/user-attachments/assets/67a53eee-4d65-44ed-a719-e948a105ab12)




- ' socket '- Provides the necessary functions to create network connections.
- ' datetime '- Used to capture the exact time of each connection for logging purposes.



Ref 2 - Configuration Variables



![Configuration Variables](https://github.com/user-attachments/assets/cb2e83f8-0085-4491-a904-bd4428ba5780)




- ' HOST = '0.0.0.0' '- Indicates that the honeypot should listen on all network interfaces available on the machine.
- ' PORT = 9999 '- The port on which the honeypot will listen for incoming connections. This can be customized.
- ' LOG_FILE = 'honeypot_log.txt' '- The file where the connection details will be saved.


Ref 3 - Logging Function


![Logging Function](https://github.com/user-attachments/assets/42fbac13-9041-4d78-bdd1-a19ed69b5ac3)


- ' log_connection(client_ip, client_port) '- This function logs the IP address and port of the connecting client along with the current timestamp. It appends this information to the honeypot_log.txt file and prints it to the console for real-time monitoring.



ref 4 - Handling Incoming Connections





![Handling Incoming Connections](https://github.com/user-attachments/assets/520103b5-daf1-4bb8-bd0b-aefbc50e9d06)



- ' handle_connection(conn, addr) '- This function manages the interaction with each incoming connection. It logs the connection using log_connection, sends a response ("Welcome to the honeypot!\n") to the client, and then closes the connection.




Ref 5 - Setting Up and Starting the Honeypot




![Setting Up and Starting the Honeypot](https://github.com/user-attachments/assets/2a2dc84a-8b39-4c3c-84bc-e22db1e752a0)





- ' socket.socket(socket.AF_INET, socket.SOCK_STREAM) '- Creates a new socket using IPv4 (AF_INET) and TCP (SOCK_STREAM).
- ' s.bind((HOST, PORT)) '- Binds the socket to the specified host and port, making the honeypot ready to accept connections.
- ' s.listen() '- Puts the socket in listening mode, waiting for incoming connections.
- ' conn, addr = s.accept() '- When a connection is received, it is accepted and the connection object (conn) and client address (addr) are retrieved.
- ' handle_connection(conn, addr) '- The connection is passed to handle_connection to be logged and managed.




Ref 6 - Running the Honeypot



![Running the Honeypot](https://github.com/user-attachments/assets/2d8606a3-f59f-4a0c-9e39-3d17333f53bd)


- This part of the code ensures that the honeypot starts running when the script is executed.
















