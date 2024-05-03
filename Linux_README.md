### Question 1: In Ubuntu server, what is a public key and private key?

**Answer:**  
In Ubuntu server, a public key and a private key are cryptographic keys used in asymmetric encryption systems such as RSA. 

- **Public Key:** The public key is used for encryption and is freely distributable. It is typically shared with others to encrypt messages or data that can only be decrypted by the corresponding private key. In Ubuntu servers, public keys are often used for SSH authentication, allowing users to securely access remote servers without needing to transmit sensitive information like passwords.

- **Private Key:** The private key is kept secret and is used for decryption. It is essential for decrypting data or messages encrypted with the corresponding public key. In Ubuntu servers, the private key is securely stored on the client-side and is used to authenticate and establish secure connections to remote servers, such as SSH connections.

Public and private key pairs form the basis of secure communication and authentication in many applications, including SSH, SSL/TLS, and digital signatures.

### Question 2: Write a script of what you do daily?

**Answer:**  
As an example, here's a basic shell script that I might use for routine tasks:

```bash
#!/bin/bash

# Script for daily routine tasks

# Update package repositories and install updates
sudo apt update
sudo apt upgrade -y

# Clean up unused packages and cache
sudo apt autoremove -y
sudo apt autoclean

# Backup important files or directories
# For example, backup important configuration files
cp /etc/nginx/nginx.conf /home/user/backups/nginx.conf_backup

# Send a notification email confirming tasks completion
echo "Daily routine tasks completed." | mail -s "Daily Task Report" user@example.com
```

This script performs tasks such as updating packages, cleaning up the system, backing up important files, and sending a notification email upon completion. It can be customized to include specific tasks based on individual requirements.

### Question 3: `chmod 444 <filename.txt>` in root user? Change the above permissions to 777?

**Answer:**  
The command `chmod 444 <filename.txt>` sets read-only permissions for all users (owner, group, and others) on the specified file `<filename.txt>`. The permissions are represented as `-r--r--r--`, meaning the file is readable but not writable or executable by anyone.

To change the permissions to `777`, allowing all users to read, write, and execute the file, you can use the command:

```bash
sudo chmod 777 <filename.txt>
```

This command grants read, write, and execute permissions to the owner, group, and others on the specified file. However, it's important to use caution when granting such broad permissions, as it can pose security risks, especially for sensitive files.

### Question 4: `curl www.google.com` is not working, but `telnet www.google.com` is working. Why?

**Answer:**  
The command `curl www.google.com` attempts to retrieve the content of the specified URL using the HTTP/HTTPS protocol. If it's not working, it indicates a potential issue with the HTTP/HTTPS connection, such as network configuration, firewall settings, or connectivity problems.

On the other hand, `telnet www.google.com` establishes a TCP connection to the specified host and port (default is port 23 for telnet). If it's working, it suggests that there is connectivity between the client and the server on the specified port (in this case, port 23).

Possible reasons why `curl` is not working while `telnet` is:

1. **Firewall Restrictions**: The server may be blocking outgoing HTTP/HTTPS traffic, but allowing outgoing TCP traffic on port 23 (used by telnet).

2. **Proxy Configuration**: If a proxy server is required for HTTP/HTTPS connections, but not for plain TCP connections, `curl` may fail to connect due to incorrect proxy settings.

3. **DNS Resolution**: There could be DNS resolution issues preventing `curl` from resolving the hostname `www.google.com` to an IP address.

4. **Protocol Issues**: If `curl` is configured to use HTTPS, but the server only supports HTTP, or vice versa, it may fail to establish a connection.

Troubleshooting involves checking network configurations, firewall rules, DNS settings, and proxy configurations to identify and resolve the underlying issue.

### Question 5: What is SSL, and how does it work internally?

**Answer:**  
SSL (Secure Sockets Layer) is a cryptographic protocol used to secure communication over a network, typically between a client (e.g., web browser) and a server (e.g., web server). It ensures that data transmitted between the client and server is encrypted and protected from eavesdropping, tampering, or forgery.

Internally, SSL works through a process called the SSL handshake, which establishes a secure connection between the client and server. The SSL handshake involves the following steps:

1. **Client Hello**: The client sends a hello message to the server, indicating the SSL version and supported cryptographic algorithms.

2. **Server Hello**: The server responds with a hello message, selecting the SSL version and cryptographic algorithms to use for the connection.

3. **Certificate Exchange**: The server sends its digital certificate to the client, containing its public key and other identifying information. The client verifies the authenticity of the certificate and extracts the server's public key.

4. **Key Exchange**: The client generates a random session key, encrypts it with the server's public key from the certificate, and sends it to the server. Both the client and server now have a shared session key for symmetric encryption.

5. **Session Encryption**: Once the session key is established, both the client and server use it to encrypt and decrypt data transmitted during the SSL session. This provides confidentiality and integrity for the exchanged data.

6. **Secure Communication**: With the session key in place, the client and server can securely exchange data over the encrypted SSL connection. The data is encrypted before transmission and decrypted upon receipt, ensuring secure communication.

SSL utilizes cryptographic techniques such as asymmetric encryption (for key exchange and authentication) and symmetric encryption (for data encryption) to achieve secure communication between parties. It forms the basis of modern security protocols such as TLS (Transport Layer Security), which has largely superseded SSL but retains its name for historical reasons.
