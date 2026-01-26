TLS = Transport Layer Security
Replaces SSL (Secure Socket  Layer)
# How does it work?
### TCP Handshake
Client and server establish a TCP handshake.
1. Client sends to server TCP SYN.
2. Server sends back TCP SYN with ACK
3. Client sends back to server TCP ACK.
This now means the connection has been established.
### Certificate Check
1. Client sends a 'Client Hello' message to server.
	Message contains TLS version supported, Cyber Suite (set of encryption algorithm)
2. Server selects an encryption algorithm from Cyber Suite and the TLS version to use
3. Server sends 'Server Hello' message back to client to provide this information.
4. Server also sends a certificate to the client.
	The certificate includes the public key for the server. 
5. Server lastly sends a 'Server Hello Done' message to finalise the connection.
### Key Exchange
1. The client generates a session key through some key exchange (such as RSA) which is encrypted using the servers public key.
2. The server decrypts the session key using its private key from earlier. 
3. Now both the client and server have the same session key which can be used for communication.
Note: this is the only purpose of the public and private key generated.
### Data Transmission 
From the key exchange that occurred, both sides have derived session keys that is used to encrypt and decrypt messages in both directions.
This means there is communication between the client and server.
# Reasons for Implementation
### Why does the method of communication change from Asymmetric to Symmetric?
Asymmetric algorithms are computationally expensive, and this is not suitable for bulk data transmission.

# Key Definitions
Asymmetric encryption -> pair of mathematically linked keys (public and private key) that handle encryption and decryption.
Symmetric encryption -> same key used for both encryption and decryption