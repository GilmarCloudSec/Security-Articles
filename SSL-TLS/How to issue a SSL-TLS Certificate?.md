### Process of Obtaining and Using an SSL/TLS Certificate

1. **Generate the Certificate Signing Request (CSR):**
   - **Create CSR:** On your server, generate a CSR containing:
     - **Public Key:** Included in the CSR.
     - **Information:** Your organization’s and domain details.
   - **Private Key:** Generated with the CSR but kept secure on your server and never shared.

2. **Submit the CSR to the Certificate Authority (CA):**
   - **Send CSR:** Submit the CSR to the CA. The CSR includes your public key and details but not the private key.

3. **Certificate Authority (CA) Verification:**
   - **Verify Details:** The CA verifies the CSR information, including domain ownership and organizational details if applicable.
   - **Issue Certificate:** After verification, the CA issues a certificate with:
     - **Your Public Key:** From the CSR.
     - **CA’s Digital Signature:** The CA signs the certificate with its private key.

4. **Receive and Install the Certificate:**
   - **Certificate Issuance:** The CA sends the signed certificate, which includes your public key and the CA’s signature. Install this certificate and any intermediate certificates on your server.
   - **Private Key:** Keep the private key secure on your server for decrypting data encrypted with your public key.

5. **User Connection to Your Website:**
   - **SSL/TLS Handshake:** When a user connects:
     - **Request Certificate:** Your server sends the SSL/TLS certificate to the user’s device.
     - **Verify Certificate:** The user’s device checks:
       - **Validity:** Ensures the certificate is not expired.
       - **Trust Chain:** Confirms the certificate is signed by a trusted CA by verifying the CA’s certificate is in its list of trusted root certificates and the chain leads back to a trusted root CA.
       - **Domain Match:** Verifies the certificate matches the accessed domain.

6. **Establish Secure Connection:**
   - **Session Key Exchange:** After certificate verification, a secure session key is established, often using asymmetric encryption during the handshake, and used for encrypting the session with symmetric encryption.

### Summary of Key Points:
- **CSR Submission:** Send only the CSR with your public key and details; keep the private key secure.
- **CA Verification:** The CA verifies your information and signs the certificate.
- **Certificate Usage:** Use the signed certificate during the SSL/TLS handshake to establish a secure connection. The user's device verifies the certificate by checking the CA’s signature and the trust chain.

The CA issues a signed certificate based on the CSR but does not retain the CSR itself. Your server sends this certificate to clients, who then verify it.
