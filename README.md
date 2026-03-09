# Symmetric Encryption Lab — AES Encryption using OpenSSL

## Overview
This lab demonstrates symmetric encryption using the AES-256-CBC algorithm via OpenSSL on Kali Linux. Symmetric encryption uses the same key for both encryption and decryption.

---

## Environment
- **OS:** Kali Linux
- **Tool:** OpenSSL
- **Algorithm:** AES-256-CBC

---

## What is Symmetric Encryption?
Symmetric encryption is a type of encryption where the same key is used to encrypt and decrypt data. It is fast and efficient, making it suitable for encrypting large amounts of data. A common example is **AES (Advanced Encryption Standard)**.

---

## Steps

### Step 1 — Create a Plaintext File
A plaintext file was created containing a simple message:
```bash
mkdir cryptography-fundamentals
cd cryptography-fundamentals
echo "I am a cybersecurity student. I want to be a SOC Analyst" > mygoal.txt
cat mygoal.txt
```
![Plaintext File](Plaintext%20File.png)

---

### Step 2 — Encrypt the File using AES-256-CBC
The file was encrypted using OpenSSL AES-256-CBC:
```bash
openssl enc -aes-256-cbc -salt -in mygoal.txt -out mygoal.enc
```
A password was entered when prompted. The output file `mygoal.enc` contains the encrypted data.

![Encrypted File](encrypted%20file.png)

---

### Step 3 — Decrypt the File
The encrypted file was decrypted using the same password:
```bash
openssl enc -aes-256-cbc -d -in mygoal.enc -out mygoal_decrypted.txt
cat mygoal_decrypted.txt
```
![Decrypted File](File%20decrypted.png)

---

## Result
- The original message was successfully encrypted into an unreadable format
- Using the correct password, the file was successfully decrypted back to the original message
- This demonstrates that **the same key (password) is used for both encryption and decryption**

---

## Key Concepts
- **AES-256-CBC** — Advanced Encryption Standard with 256-bit key in Cipher Block Chaining mode
- **Salt** — Random data added to make encryption stronger and prevent dictionary attacks
- **Same key** — Both encryption and decryption use the same password/key

---

## Author
**Temitope Christiana Alausa**
GitHub: [TemmyNetGuard](https://github.com/TemmyNetGuard)
