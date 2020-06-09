					Readme File for Chat Server and Client Sytem

/**---------------------------------------------------------------------------
* File: Makefile
*
* Purpose: to compile the server and client programs
*
* Usage: 
* (1) "make" command will compile the server and client programs and creates object files seperately in  "exe" folder
* (2) "make clean" will delete object files and all the support files for the server
* 
*------------------------------------------------------------------------------
*/


/**---------------------------------------------------------------------------
* Program: server
*
* Purpose: allocate a socket and then repeatedly execute the following:
* (1) establish connections to clients as per the listen queue
* (2) receive a short message from the client 
* (3) extract to whom that message has to be delivered
* (4) send that message to that particular recipient
* (5) handle errors, if user types message in wrong format
*
* Syntax: ./server
*
* NOTE: 
* (1) database.txt will be created for successful signup of clients 
* (2) message logs will be created in the name of corresponding clients
* (3) buffer file will be created if the client sends messages to inactive client, he/she will receive the messages once he becomes active and 	     corresponding buffer file will be deleted
*------------------------------------------------------------------------------
*/


/**-----------------------------------------------------------------------------
* Program: client
*
* Purpose: allocate a socket, connect to a server, and print all output
* 
* Syntax for executing: ./client <server_ipaddress>
* Example: ./client 127.0.0.1
*
* server_ipaddress - mention your system ip on which your server code is running
*
* Syntax to send messages, to display active clients and log messages:
* (1) all:<type your message>
* Example: all:hello world ("hello world" message will be received by all active clients")
*
* (2) client_name:<type your message>
* Example: kishore:hi kishore ("hi kishore" message will be send to the client kishore)
*
* (3) active:clients
* Example: active:clients (all the active clients will be displayed)
*
* (4) logs:client
* Example: logs:bala (log messages of bala will be displayed)
*
* NOTE: enter "quit" to close his/her connection
*
* DONT's: client will be closed with corresponding error messages if anyone of the following scenarios happened
* (1) During signup, if the client types the name which already exists in the server database
* (2) During signup, if the password and confirm password doesn't match
* (3) During login, if the user tries to login without signup
* (4) During login, if the username and password doesn't match
* (5) If the user forcefully quits his/her session by typing "quit" or by pressing ctrl+c
*
*---------------------------------------------------------------------------
*/
