# How are passwords stored

## Early Unix

- Passwords were stored in `/etc/passwd` file

- The passwords were encrypted using a simple algorithm called `crypt`

- The system hashes each password after combining it with a random value called a salt of 12-bits

- The salt value is not secret; it is stored with the hashed password.

- Whenever a user chooses a new password, the system generates a new salt at random.

- Historically, UNIX generates the salt from the time of day or some other weak source
  of entropy (randomness).
- Because of this, it is common for two users at a site to have
  the same salt value.
- Still, the complexity of an offline password-cracking attack greatly
  increases because each word must be re-hashed for each salt value.

## Windows NT/2000/XP

- Windows NT/2000/XP uses a more secure password storage scheme.

- The passwords are hashed using two hashing algorithms, namely, LanMan hash and the NT hash.

### LanMan hash

- The LanMan hash is used for backward compatibility with older versions of Windows.

- It is not secure and is disabled by default in Windows Vista and later.

- Windows limits passwords to 14 characters for the Lanman hash.

- System computes the hash by splitting the password into two 7-character chunks and converting them to uppercase.

- The system then encrypts each chunk separately using DES and then concatenates the two 8-byte hashes to form a 16-byte hash.

- Programs like L0phtCrack can crack LanMan hashes in a matter of seconds.

### NT hash

- The NT hash is a more secure hash.

- It is computed by using the MD4 algorithm.

- MD4 algorithm has 48 steps which turn a 512-bit input to a 128-bit output.

## Windows 2000 and later

- Windows 2000 and later versions use the NTLMv2 and kerberos authentication protocols.

- Kerberos is the default authentication protocol for Windows 2000 and later.

- Kerberos doesnot store passwords directly, instead, it uses a Ticket Granting Ticket (TGT) to authenticate users.

- SAM ( Security Accounts Manager) database : The SAM database is a part of the Windows registry and stores users' passwords in a hashed format.

- The SAM database is encrypted using a 128-bit RC4 encryption key.

- The SAM database is stored in the `C:\Windows\System32\Config` directory.

- The SAM database is locked when the operating system is running.
