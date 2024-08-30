SSL/TLS provides three core security properties: **confidentiality**, **integrity**, and **authentication**.

### 1. **Confidentiality**

**Confidentiality** keeps the data transmitted between the client and server private and prevents unauthorized access.

- **Encryption:** SSL/TLS uses encryption to ensure that data is only readable by the intended recipient. This is achieved through symmetric encryption, where the same key is used for both encrypting and decrypting the data.

- **Session Keys:** During the SSL/TLS handshake, a session key (symmetric key) is established to encrypt all data for the session.

**Example:** When logging into a website with HTTPS, your username and password are encrypted, so even if intercepted, they cannot be read by attackers.

### 2. **Integrity**

**Integrity** ensures that data remains unchanged and untampered during transmission.

- **Message Integrity:** SSL/TLS uses message authentication codes (MACs) or hashes to verify data integrity. A unique hash or MAC is generated before sending data, and the recipient generates a hash of the received data to ensure it matches the original.

- **Hash Functions:** Algorithms like SHA-256 or SHA-384 create these hashes. If the data is altered in transit, the hash or MAC will differ, indicating tampering.

**Example:** If an attacker modifies the contents of a web page during transmission, the mismatch in hash or MAC values will reveal the tampering.

### 3. **Authentication**

**Authentication** verifies the identities of the communicating parties to ensure they are who they claim to be.

- **Server Authentication:** SSL/TLS uses digital certificates from Certificate Authorities (CAs) to authenticate the server. The client checks the server’s certificate for validity and CA trustworthiness.

- **Client Authentication (Optional):** SSL/TLS can also authenticate clients using client certificates.

**Example:** When visiting a secure website, your browser verifies the SSL/TLS certificate to confirm that it is issued by a trusted CA and that you are communicating with the legitimate website.

### Summary

- **Confidentiality:** Ensures data is encrypted and accessible only to authorized parties.
- **Integrity:** Ensures data remains unaltered during transmission through hashing.
- **Authentication:** Verifies the identities of the communicating parties to ensure trust.

These properties together create a secure and reliable communication channel between client and server.
