An alternative to passwords using public key cryptography.
# Summarised
A token is generated and given to the user. The user signs the token using their private key. Then the website is able to verify the token using the public key that it is given.
# More Detailed
Reliant party -> entity that you are authenticating on (most likely the website you are accessing)
Client -> device used to talk to the reliant party (the user end such as browser or app)
Authenticator -> the entity that handles the signing (for example Apple Face ID, Windows Hello etc.)
- The RP holds the public key.
- Authenticator holds the private key
## Overview of Generation Process
1. RP communicates to client that it will be creating a passkey
	ID of website, User information, etc.
2. Client sends information to Authenticator
3. Authenticator generates Public and Private key pairs (unique to the passkey being generated)
4. Public key and ID associated with key pair shared with RP and stored
## Overview of Signing Process
1.  RP generates token and other information sends this to client.
2. Client verifies the ID of the website and token generated.
3. Client sends some of these information hashed to the Authenticator.
4. Authenticator signs various information including the token and ID with private key. 
## Improvements
- Phishing cannot be done since the public key and URL hashing is hard to reverse engineer, so requests from unusual RPs are rejected.
- Cannot be replayed -> the tokens generated are unique and never repeated.
- Do not remember passwords, although user prompt may be requested such as biometrics or pin
## Points of Failure
- If the client or Authenticator loses information (by for example losing devices), then the private key to sign tokens cannot be done. To recover this, a password is used (at the current moment)
- Without user verification, someone with access to your device can access various sites
# Key Definitions
Context-binding -> the private and public keys generated are only specific for one purpose and cannot be used multi-purposely. 
# Source
https://www.youtube.com/watch?v=xYfiOnufBSk