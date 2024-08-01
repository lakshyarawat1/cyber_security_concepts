# Introduction to CryptOps

## Key Management In DevSecOps

### Key Management Life Cycle

- __Key Generation__ :

    - The first step in the key management life cycle is key generation. This is the process of creating a new key. The key can be generated using a key generation algorithm or it can be imported from an external source.

- __Key Distribution__ :
    
    - The next step in the key management life cycle is key distribution. This is the process of securely transmitting the key to the intended recipient. The key can be distributed using a secure channel or it can be stored in a secure location.

- __Key Storage__ :

    - The next step in the key management life cycle is key storage. This is the process of securely storing the key. The key can be stored in a secure location or it can be stored in a secure hardware device or Hardware Secure Modules (HSMs)

- __Key Usage__ :

    - Using the key, monitoring and controlling how and when and by whom the key is used are vital.

- __Key Backup and Recovery__ :

    - It involves creating secure copies of cryptographic keys to avoid losing access in case of deletion or corruption.

- __Key Rotation__ :

    - Replacing older keys with new ones at regular intervals in response to specific events like key compromise.

- __Key Revocation__ :

    - Invalidating a key before its scheduled expiration.

- __Key Destruction__ :

    - Ensuring that the key is securely deleted and cannot be recovered.


### Best Practices in key generation

- __Use a strong Random Number Generators(RNGs)__ : 

    - Use Cryptographically secure pseudo-random number generators(CSPRNGs) designed  to produce computationally infeasible output to predict

    - For industry standards, use `FIPS-140-X` for algorithms and best practices.

- __Adhere to industry standards and algorithms__ :

    - Follow current industry standards like NIST for generation algorithms and key lengths.

- __Secure the key generation environment__ : 

    - Ensuring that key is generated in a secure environment and away from unauthorized access and tamper-resistant.

    - This can involve using Hardware security modules(HSMs).

- __Validate key generation parameters__ :

    - Before deploying keys, validate all parameters of key generation. 

- Bastion Hosts : a.k.a. jump servers are securely configured cloud instances that serves as an isolated access point between the external and internal network resources.


### Best practices in key destribution

- __Secure transmission channel__ :

    - Protocols like TLS and mTLS can secure the transmission of keys

- __Employ Public key infrastructure__ :

    - The public key can be openly distributed as the private key can be stored securely with the owner

- __Use trusted Delivery methods__ :

    - Some tools are secure email exchange or encypted file exchange tool.

- __Implement robust authentication mechanism__ 

- __Provide secure key storage solution__ 


### Key storage and usage

- __Hardware Security Modules__ : HSM is a physical device designed to generate, store and manage cryptographic keys securely.

- __Cloud Based key management services__ : Like AWS KMS, or Azure Key vault.

- __Encrypted Databases and keystores__

### Key rotation and revocation strategies

- Define a cryptoperiod : The period after which the keys will be rotated.

- Automate key rotation

- Use versioning and backward compatibility

- Key revocation :

    - Use Certificate Revocation Lists(CRLs) and Online Certificate Status protocol(OCSP)
    