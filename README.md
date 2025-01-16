# CNT4007-Project-2

## Code made by: Ibet Gonzalez Viltres and Erin Hargrave.

## Project Structure:
```
|-- Makefile
|-- clientDirectory
|   |-- *client files*
|   |-- client
|   `-- client.c
`-- serverDirectory
    |-- *server files*
    |-- server
    `-- server.c
```
* The makefile is placed in the current/main directory
* The clientDirectory and the serverDirectory are both placed inside the same directory as the Makefile
* Client.c is located within the clientDirectory
* Server.c is located within the serverDirectory
* When the Makefile runs it will create:
    * A ./client executable inside the clientDirectory
    * A ./server executable inside the serverDirectory
* All files related to the client should be located within the clientDirectory
* All files related to the server should be located within the serverDirectory

## How to Run the Files:
1. Within the main directory, run ```make``` to create the executables within their respective directories
2. To run the server, set up a terminal and run ```cd ./serverDirectory``` and then ```./server``` to run the server 
3. To run the client(s), set up another terminal for each client and run ```cd ./clientDirectory``` and then ```./client``` to run the client

## The Client Interface
### The client will present the user with four options:
1. To list all of the files located on the server
    * This runs the LIST method
2. To show the files that the server has but the client does not
    * This runs the DIFF method
3. To get the files that the client does not hvae
    * This runs the PULL method
4. To close the connection
    * This runs the LEAVE method

### How to choose an option:
* Enter the number of the option (1, 2, 3, 4) into the command line
    * Any value that is not 1-4 will be marked as invalid

### How the interface works:
* Each option operates on its own
    * This means that the user does not have to pick option 1 (LIST) for option 2 to work (DIFF)
* Running the LIST method will provide the user with a list of files that the server has
* Running DIFF will provide the user with a list of files that the server has but the client does not
* If a file in the client side has the same name as a file in the server side but different contents, the PULL method will replace the contents of the file in the client
