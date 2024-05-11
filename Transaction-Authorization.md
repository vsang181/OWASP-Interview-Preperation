# Transaction Authorization

## Purpose and Audience:

This cheat sheet offers guidance on securely implementing transaction authorization to prevent bypassing. It's useful for:

- Banks: Defining functional and non-functional requirements for transaction authorization.
- Developers: Designing and implementing secure transaction authorization.
- Pentesters: Testing transaction authorization security.

## Introduction:

Transaction authorization adds an extra layer of security, commonly used in sensitive operations like wire transfers in banking apps. It's crucial for protecting against malware, phishing, and other attacks.

### Functional Guidelines:

1. **User Awareness**: Users must be able to identify and confirm transaction details on an external device to prevent malware threats.
2. **Token Change Authorization**: Changing authorization tokens should require current credentials for verification.
3. **Method Change Authorization**: Switching authorization methods should also require current credentials to avoid vulnerabilities.
4. **Authentication Distinction**: Differentiate between authentication and transaction authorization processes to prevent malware tricks.
5. **Unique Credentials**: Each transaction should use unique authorization credentials to prevent unauthorized use.

### Non-functional Guidelines:

1. **Server-side Enforcement**: Authorization should be enforced server-side to prevent client-side tampering.
2. **Method Enforcement**: Server should enforce the current chosen authorization method to prevent downgrading attacks.
3. **Server-side Data Generation**: Significant transaction data should be generated and stored server-side to prevent client manipulation.
4. **Brute-Force Prevention**: Implement measures to prevent brute-forcing of authorization credentials.
5. **Sequential Process**: Ensure transactions follow a sequential process to prevent unauthorized steps or data modifications.
6. **Data Protection**: Protect transaction data against modifications or replay attacks.
7. **Confidentiality**: Maintain transaction data confidentiality during client-server communication.
8. **Authorization Verification**: Verify authorization before executing transactions to prevent time-based attacks.
9. **Time-limited Credentials**: Authorization credentials should have a limited validity period to prevent misuse.
10. **Unique Credentials**: Ensure each operation has unique authorization credentials to prevent replay attacks.

## Remarks:

- Considerations like cryptographic protection, device pairing, user awareness, and anti-malware solutions are essential but not covered here.
- Protecting signing keys and using second-factor authentication are critical for security.
- Utilizing secure elements like TEE, TPM, or smart cards can enhance key protection.
- User education on verifying transaction data from trusted sources is important.

By adhering to these guidelines, applications can implement robust transaction authorization systems to safeguard against various security threats.

## Let's Connect

I welcome your insights, feedback, and opportunities for collaboration. Together, we can make the digital world safer, one challenge at a time.

- **LinkedIn**: (https://www.linkedin.com/in/aashwadhaama/)

I look forward to connecting with fellow cybersecurity enthusiasts and professionals to share knowledge and work together towards a more secure digital environment.
