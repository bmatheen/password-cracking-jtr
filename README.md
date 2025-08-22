# password-cracking-jtr
Beginner demo: generating md5crypt hashes with OpenSSL and cracking with John the Ripper in Kali Linux (education only).

# Password Cracking with John the Ripper (Beginner Demo)

This project demonstrates how weak passwords can be cracked from **md5crypt** hashes using **John the Ripper** on **Kali Linux**.  
**For education only. Do not use on systems/data you don’t own or have explicit permission to test.**

## Project Goals
- Generate a password hash with `openssl`
- Crack it with `john`
- Show why strong passwords and modern KDFs (bcrypt/scrypt/Argon2) matter
  
## Snap Shot
![alt Text](/screenshot_of_encrypting_password.png)

## Quick Start
```bash
echo '12345' | openssl passwd -1 -stdin > demo/password.txt
john demo/password.txt
john --show demo/password.txt

