- [Useful Tools for cryptography](#useful-tools-for-cryptography)
- [🔐 Cryptographic Algorithms with Security Status](#-cryptographic-algorithms-with-security-status)
  - ["Block Cipher" vs "Block Cipher Mode"](#block-cipher-vs-block-cipher-mode)
    - [🔐 What Is a Block Cipher?](#-what-is-a-block-cipher)
    - [📌 Examples of block ciphers:](#-examples-of-block-ciphers)
  - [🔄 What Is a Block Cipher Mode?](#-what-is-a-block-cipher-mode)
    - [📦 Modes determine:](#-modes-determine)
    - [📌 Common block cipher modes:](#-common-block-cipher-modes)
    - [🔐 Block Cipher Modes Comparison](#-block-cipher-modes-comparison)
    - [🧠 Quick Insights](#-quick-insights)
    - [🧠 Analogy](#-analogy)
  - [🧱 Block Cipher vs 🌊 Stream Cipher: Core Difference](#-block-cipher-vs--stream-cipher-core-difference)
    - [🧱 Block \& 🌊 Stream Ciphers: Symmetric by Nature](#-block---stream-ciphers-symmetric-by-nature)
    - [🔐 What About Asymmetric Algorithms?](#-what-about-asymmetric-algorithms)
      - [📌 Examples: RSA, ECC (Elliptic Curve Cryptography)](#-examples-rsa-ecc-elliptic-curve-cryptography)
      - [🧠 Why the Separation?](#-why-the-separation)
    - [🔄 How Block Cipher Modes Bridge the Gap](#-how-block-cipher-modes-bridge-the-gap)
    - [🧠 Analogy Time](#-analogy-time)
- [Public Key Infrastructure (PKI)](#public-key-infrastructure-pki)
  - [🧰 Top Commercial PKI Products](#-top-commercial-pki-products)
  - [🧪 Popular Open-Source PKI Solutions](#-popular-open-source-pki-solutions)
  - [💡 Why Use PKI Software?](#-why-use-pki-software)
- [IPSec vs TCP/IP vs TLS vs SSL](#ipsec-vs-tcpip-vs-tls-vs-ssl)
  - [🧠 Quick Insight:](#-quick-insight)
- [Encoding format (output format) for binary data](#encoding-format-output-format-for-binary-data)
  - [🧩 What Are Base64 and HEX?](#-what-are-base64-and-hex)
  - [🔐 Where They Show Up](#-where-they-show-up)
  - [🧠 Why Use These Formats?](#-why-use-these-formats)
- [📦 Common Cryptographic File Formats](#-common-cryptographic-file-formats)
  - [🧠 Quick Tips](#-quick-tips)
- [Cryptographic Algorithms primitives:](#cryptographic-algorithms-primitives)
  - [🧠 One-Way Functions = Hash Functions](#-one-way-functions--hash-functions)
  - [🔄 Two-Way Functions = Symmetric, Asymmetric, Certificates](#-two-way-functions--symmetric-asymmetric-certificates)
  - [🧩 Bonus: Hybrid Systems](#-bonus-hybrid-systems)
- [Asymmetric Algorithms vs Digital Certificates](#asymmetric-algorithms-vs-digital-certificates)
  - [🔑 Asymmetric Algorithms](#-asymmetric-algorithms)
  - [📄 Digital Certificates](#-digital-certificates)
  - [🧠 Summary Matrix](#-summary-matrix)
  - [Encryption vs Signing](#encryption-vs-signing)
    - [🔒 Encryption: Keeping Secrets](#-encryption-keeping-secrets)
    - [✍️ Signing: Proving Identity \& Integrity](#️-signing-proving-identity--integrity)
    - [🧠 Key Differences](#-key-differences)
    - [🔄 Often Used Together](#-often-used-together)
- [Encryption vs Signing with OpenSSL](#encryption-vs-signing-with-openssl)
  - [🔒 Encryption with OpenSSL (Confidentiality)](#-encryption-with-openssl-confidentiality)
  - [✍️ Signing with OpenSSL (Authenticity \& Integrity)](#️-signing-with-openssl-authenticity--integrity)
  - [🧠 Summary Table](#-summary-table)
- [OpenSSL Supported Digests](#openssl-supported-digests)
  - [🔐 SHA Hash Algorithm Comparison Table](#-sha-hash-algorithm-comparison-table)
  - [🧠 Quick Family Overview](#-quick-family-overview)
- [Generate a self-signed digital certificate using OpenSSL](#generate-a-self-signed-digital-certificate-using-openssl)
- [Add Subject Alternative Names (SAN) to your self-signed certificate using OpenSSL](#add-subject-alternative-names-san-to-your-self-signed-certificate-using-openssl)
  - [🧠 Why This Works](#-why-this-works)
- [Common Digital Certificate Formats](#common-digital-certificate-formats)
  - [🧠 Quick Tips](#-quick-tips-1)
- [Cipher Suite](#cipher-suite)
  - [🔐 Common Places You’ll Find Cipher Suites](#-common-places-youll-find-cipher-suites)
  - [🧩 Components of a Cipher Suite](#-components-of-a-cipher-suite)
  - [🔍 Example Breakdown](#-example-breakdown)
  - [🧠 TLS 1.3 Simplification](#-tls-13-simplification)
- [Cryptography + TLS](#cryptography--tls)
  - [🔐 TLS = Hybrid Encryption](#-tls--hybrid-encryption)
  - [🧠 How It Works](#-how-it-works)
- [Evolution of TLS (Transport Layer Security) versions:](#evolution-of-tls-transport-layer-security-versions)
  - [🧠 Highlights](#-highlights)
- [TLS Handshake: Step-by-Step Breakdown](#tls-handshake-step-by-step-breakdown)
  - [🔐 TLS Handshake Steps](#-tls-handshake-steps)
  - [🧠 Analogy Time](#-analogy-time-1)
# Useful Tools for cryptography
To check the security posture/status of a cipher suites:
- https://ciphersuite.info/

Websites to play with: "Encryption Tools", "Hashing Tools" and "Encoding Tools":
- https://anycript.com/
- https://cryptotools.net/
# 🔐 Cryptographic Algorithms with Security Status
| Algorithm             | Type          | Key Length(s)          | Cipher Type | Purpose(s)                        | Is Still Secured?                                                                 |
|----------------------|---------------|------------------------|-------------|-----------------------------------|-----------------------------------------------------------------------------------|
| AES                  | Symmetric     | 128, 192, 256 bits     | Block       | Encryption                        | ✅ Yes — quantum-resistant (AES-256 still strong despite Grover’s algorithm)      |
| RSA                  | Asymmetric    | 1024–4096 bits         | N/A         | Encryption, Digital Signature     | ⚠️ At Risk — vulnerable to quantum (Shor’s algorithm) by 2030s                    |
| ECC                  | Asymmetric    | ~160–512 bits          | N/A         | Digital Signature, Key Exchange   | ⚠️ At Risk — quantum-vulnerable (Shor’s algorithm)                               |
| ChaCha20             | Symmetric     | 256 bits               | Stream      | Encryption                        | ✅ Yes — secure and fast; quantum-safe                                            |
| Blowfish             | Symmetric     | 32–448 bits            | Block       | Encryption                        | ⚠️ Weak — outdated; brute-force risk with short keys                             |
| Twofish              | Symmetric     | Up to 256 bits         | Block       | Encryption                        | ✅ Yes — quantum-resistant with long keys                                         |
| Triple DES           | Symmetric     | 112 or 168 bits        | Block       | Encryption                        | ❌ Deprecated — weak key strength; phased out by NIST                             |
| DES                  | Symmetric     | 56 bits                | Block       | Encryption (legacy)               | ❌ Broken — easily brute-forced                                                   |
| Diffie-Hellman       | Asymmetric    | Variable               | N/A         | Key Exchange                      | ⚠️ At Risk — quantum-vulnerable (Shor’s algorithm)                               |
| ElGamal              | Asymmetric    | Variable               | N/A         | Encryption, Digital Signature     | ⚠️ At Risk — same vulnerability as RSA                                           |
| ECDSA                | Asymmetric    | ~256 bits              | N/A         | Digital Signature                 | ⚠️ At Risk — vulnerable to quantum attacks                                       |
| SHA-1                | N/A           | 160 bits (output)      | N/A         | Hashing                           | ❌ Deprecated — collision attacks; retired by NIST                                |
| SHA-2 (SHA-256)      | N/A           | 256 bits (output)      | N/A         | Hashing                           | ✅ Yes — secure; Grover’s algorithm halves strength but remains robust            |
| SHA-3                | N/A           | 224–512 bits (output)  | N/A         | Hashing                           | ✅ Yes — designed with quantum resistance in mind                                 |
| MD5                  | N/A           | 128 bits (output)      | N/A         | Hashing (legacy)                  | ❌ Broken — prone to collisions                                                   |
| HMAC                 | Symmetric     | Variable               | N/A         | Message Authentication            | ✅ Yes — secure when paired with strong hash (e.g. SHA-2/SHA-3)                   |
| RC4                  | Symmetric     | 40–2048 bits           | Stream      | Encryption (deprecated)           | ❌ Broken — statistical biases and vulnerabilities                               |
| Camellia             | Symmetric     | 128, 192, 256 bits     | Block       | Encryption                        | ✅ Yes — secure; comparable to AES                                                |
| CRYSTALS-Kyber       | Asymmetric    | Post-quantum (var.)    | N/A         | Key Exchange (PQ-safe)            | ✅ Yes — NIST-selected post-quantum algorithm                                     |

Think of a block cipher as a core engine that can encrypt one block at a time — but real-world data is usually much larger than a single block.
## "Block Cipher" vs "Block Cipher Mode"
### 🔐 What Is a Block Cipher?
A block cipher is a type of encryption algorithm that:
- Works on fixed-size blocks of data (e.g., 128 bits for AES).
- Uses a secret key to transform plaintext into ciphertext.
- Is deterministic: the same input and key always produce the same output.
### 📌 Examples of block ciphers:
- AES (Advanced Encryption Standard)
- DES (Data Encryption Standard)
- Blowfish
- Camellia
## 🔄 What Is a Block Cipher Mode?
A block cipher mode of operation defines how to apply a block cipher repeatedly to encrypt data larger than one block. It also helps add randomness and security features.
### 📦 Modes determine:
- How blocks are linked together.
- Whether encryption can be done in parallel.
- How to handle padding or streaming data.
- Whether the mode provides authentication (e.g., GCM).
### 📌 Common block cipher modes:
| Mode     | Description                                      | Highlights                                |
|----------|--------------------------------------------------|-------------------------------------------|
| ECB      | Encrypts each block independently                | Fast but insecure — patterns leak         |
| CBC      | Chains blocks together using XOR                 | More secure, but not parallelizable       |
| CFB/OFB  | Converts block cipher into stream cipher         | Good for streaming data                   |
| CTR      | Uses a counter for each block                    | Fast, parallelizable, no padding needed   |
| GCM      | Combines encryption with authentication          | Used in TLS and secure messaging          |
### 🔐 Block Cipher Modes Comparison
| Mode                      | Type                    | Padding Required | Parallelizable        | Authentication | Error Propagation | Use Case                               |
|---------------------------|-------------------------|------------------|------------------------|----------------|-------------------|----------------------------------------|
| ECB (Electronic Codebook) | Encryption only         | Yes              | Yes (encryption only)  | No             | High              | Simple but insecure; not recommended   |
| CBC (Cipher Block Chaining) | Encryption only       | Yes              | No (encryption only)   | No             | Medium            | File encryption; legacy systems        |
| CFB (Cipher Feedback)     | Encryption only         | No               | No (encryption only)   | No             | Medium            | Streaming data; partial block support  |
| OFB (Output Feedback)     | Encryption only         | No               | Yes                   | No             | Low               | Error-resilient streaming              |
| CCM (Counter with CBC-MAC)| Authenticated encryption| No               | Yes                   | Yes            | Low               | Secure messaging; IoT devices          |
| CMAC (Cipher-based MAC)   | Authentication only     | No               | Yes                   | Yes            | N/A               | Message integrity; digital signatures  |
| GCM (Galois/Counter Mode) | Authenticated encryption| No               | Yes                   | Yes            | Low               | TLS, VPNs, secure file transfer        |
### 🧠 Quick Insights
- ECB is fast but leaks patterns — avoid it unless you're encrypting random data.
- CBC improves security over ECB but isn't parallelizable and needs padding.
- CFB/OFB turn block ciphers into stream-like behavior — great for real-time data.
- CCM/GCM are modern modes that combine encryption and authentication.
- CMAC is used when you only need to verify data integrity, not encrypt it.
### 🧠 Analogy
Imagine a block cipher as a lock that secures one box at a time. A block cipher mode is the packing strategy that tells you how to lock a whole shipment of boxes — whether you chain them, label them, or wrap them together.
## 🧱 Block Cipher vs 🌊 Stream Cipher: Core Difference
| Feature              | Block Cipher                                 | Stream Cipher                                  |
|----------------------|----------------------------------------------|------------------------------------------------|
| **Data Unit**        | Encrypts fixed-size blocks (e.g. 128 bits)   | Encrypts one bit or byte at a time             |
| **Example Algorithms** | AES, DES, Blowfish                          | RC4, ChaCha20, Salsa20                         |
| **Padding Required?** | Yes, if data isn't a full block              | No padding needed                              |
| **Speed**            | Slower, more secure                          | Faster, better for real-time use               |
| **Error Propagation**| Can affect the entire block                  | Usually localized to one bit                   |
| **Use Case**         | File encryption, TLS                         | Streaming media, secure messaging              |
### 🧱 Block & 🌊 Stream Ciphers: Symmetric by Nature
block ciphers and stream ciphers are exclusive to symmetric cryptography. Here's how it breaks down:
| Cipher Type   | Key Usage                         | Algorithm Examples           | Notes                                         |
|---------------|-----------------------------------|------------------------------|-----------------------------------------------|
| Block Cipher  | Same key for encryption & decryption | AES, DES, Blowfish          | Encrypts fixed-size blocks                    |
| Stream Cipher | Same key for encryption & decryption | RC4, ChaCha20, Salsa20      | Encrypts data bit-by-bit or byte-by-byte      |
- Both rely on a shared secret key between sender and receiver.
- They're designed for speed and efficiency, especially when encrypting large volumes of data.
### 🔐 What About Asymmetric Algorithms?
Asymmetric cryptography uses two keys:
- A public key for encryption
- A private key for decryption
#### 📌 Examples: RSA, ECC (Elliptic Curve Cryptography)
These algorithms:
- Do not use block or stream cipher structures.
- Are typically used for key exchange, digital signatures, or small data encryption (like encrypting a symmetric key).
#### 🧠 Why the Separation?
- Block/stream ciphers are optimized for bulk data encryption — fast and lightweight.
- Asymmetric algorithms are computationally heavier and better suited for secure key distribution.
### 🔄 How Block Cipher Modes Bridge the Gap
Block cipher modes like CFB, OFB, and CTR actually transform block ciphers into stream-like behavior:
- CFB (Cipher Feedback): Encrypts small chunks (like bytes) using a block cipher — mimics stream cipher flow.
- OFB (Output Feedback): Generates a keystream independent of plaintext — very stream-like.
- CTR (Counter Mode): Uses a counter to produce a keystream — parallelizable and stream-friendly.

So while AES is a block cipher, using it in CTR mode makes it behave like a stream cipher — ideal for encrypting data on the fly.
### 🧠 Analogy Time
Imagine a block cipher is like a typewriter — you type one full line before moving to the next. A stream cipher is like a pen — you write continuously, letter by letter. Block cipher modes like CTR or CFB? They’re like a typewriter with a rolling ribbon — giving you the flexibility of a pen with the structure of a typewriter.
# Public Key Infrastructure (PKI)
"PKI is the set of software, hardware, processes, procedures, and policies that are needed to create, manage, distribute, use, store, and revoke digital certificates across large user populations."

Absolutely, Arthur! You don’t need to build a PKI system from scratch—there are plenty of PKI software solutions that handle certificate management, issuance, and revocation for you. Here’s a mix of enterprise-grade, cloud-based, and open-source options to consider:
## 🧰 Top Commercial PKI Products
| Product                   | Best For                              | Highlights                                                   |
|---------------------------|----------------------------------------|--------------------------------------------------------------|
| DigiCert CertCentral      | TLS/SSL lifecycle management           | Intuitive dashboard, automation, trusted CA                  |
| Keyfactor Command         | Enterprise-scale PKI & IoT security    | Scalable, integrates with DevOps and cloud                   |
| Venafi TLS Protect        | Machine identity protection            | Zero-touch automation, strong policy enforcement             |
| AppViewX CERT+            | Certificate orchestration              | Role-based access, self-service workflows                    |
| SecureW2 JoinNow          | Cloud-native PKI for Wi-Fi & VPN       | Passwordless access, Azure/Okta integration                  |
| Sectigo Certificate Manager | Universal CLM platform              | CA-agnostic, supports public/private certs                   |
| Entrust PKI Hub           | Managed or on-prem PKI                 | Quantum-ready, flexible deployment options                   |
## 🧪 Popular Open-Source PKI Solutions
| Tool         | Strengths                                                             |
|--------------|-----------------------------------------------------------------------|
| EJBCA CE     | Full-featured CA/RA/OCSP; REST API; Docker-ready                      |
| Dogtag PKI   | Web-based UI; supports ACME, SCEP, LDAP                               |
| OpenXPKI     | Perl-based; customizable workflows; browser GUI                       |
| Step-ca      | CLI-based; integrates with Kubernetes & Envoy                         |
## 💡 Why Use PKI Software?
- Saves time and reduces errors with automated certificate lifecycle management
- Ensures compliance with standards like FIPS, GDPR, and FedRAMP
- Provides centralized visibility and control over digital identities
- Supports integration with cloud platforms, DevOps pipelines, and enterprise directories

# IPSec vs TCP/IP vs TLS vs SSL
| Aspect                 | IPSec                                                | TCP/IP                                     | TLS                                                  | SSL                                             |
|------------------------|------------------------------------------------------|--------------------------------------------|------------------------------------------------------|--------------------------------------------------|
| **Definition**         | Security protocol suite for IP communications       | Core protocol stack for internet communication | Cryptographic protocol for securing app-layer traffic | Predecessor to TLS; deprecated encryption protocol |
| **OSI Layer**          | Network Layer (Layer 3)                              | Multiple layers: Network, Transport, Application | Between Transport and Application Layers           | Same as TLS                                      |
| **Purpose**            | Encrypts/authenticates IP packets                   | Enables data transmission across networks   | Secures specific applications (e.g., HTTPS, SMTP)    | Secured web traffic; now replaced by TLS         |
| **Encryption**         | Yes – via ESP and AH protocols                      | No built-in encryption                      | Yes – strong encryption (AES, ChaCha20, etc.)        | Yes – but outdated and vulnerable                |
| **Authentication**     | Mutual (keys or certificates)                       | None                                        | Certificate-based authentication                    | Certificate-based authentication                 |
| **Use Cases**          | VPNs, site-to-site tunnels                          | General communication (web, email, etc.)    | HTTPS, secure APIs, email, VoIP                      | Legacy HTTPS, early web sessions                 |
| **Config Complexity**  | Moderate to High                                     | Low                                         | Low to Moderate                                      | Low – but no longer recommended                  |
| **Modern Status**      | Actively used and evolving                          | Foundation of internet                      | Current standard                                     | Deprecated since 1999                            |
| **Protocol Examples**  | ESP, AH, IKEv2                                       | IP, TCP, UDP, HTTP, DNS                     | TLS 1.2, TLS 1.3                                     | SSL 2.0, SSL 3.0                                  |
## 🧠 Quick Insight:
- TCP/IP is the highway system.
- IPSec is the armored vehicle securing all traffic on that highway.
- TLS is the secure lock on specific packages (like HTTPS).
- SSL is the retired version of TLS—still mentioned, but no longer safe to use.
# Encoding format (output format) for binary data
Base64 and HEX are output formats for binary data, and they’re used across both symmetric and asymmetric cryptography, as well as in hashing and digital signatures.
## 🧩 What Are Base64 and HEX?
| Format   | Purpose                             | Common Use                          |
|----------|-------------------------------------|--------------------------------------|
| Base64   | Encodes binary data into ASCII      | Email attachments, web APIs, JWTs   |
| HEX      | Represents binary as hexadecimal    | Debugging, cryptographic keys, hashes |

These formats are not encryption algorithms — they’re just ways to represent encrypted or hashed data in a readable or transmittable form.
## 🔐 Where They Show Up
- Symmetric encryption (e.g. AES): Encrypted ciphertext is often encoded in Base64 or HEX for storage or transmission.
- Asymmetric encryption (e.g. RSA, ECC): Public/private keys and encrypted payloads are frequently Base64-encoded (like in PEM files).
- Hashing (e.g. SHA-2): Hash outputs are typically shown in HEX (e.g. 5d41402abc4b2a76b9719d911017c592).
- Digital signatures: Signature bytes are often Base64-encoded for inclusion in documents or protocols.
## 🧠 Why Use These Formats?
- Binary data isn’t human-readable — Base64 and HEX make it readable and portable.
- Text-based protocols (like HTTP, SMTP, JSON) require ASCII-safe formats.
- Cross-platform compatibility — ensures consistent representation across systems.

So whether you're encrypting a message with AES or signing a document with RSA, Base64 and HEX are your go-to wrappers for making the results usable. Want to see how a ciphertext or signature looks in both formats? I can show you with a quick example.
# 📦 Common Cryptographic File Formats
| Format               | Encoding             | Contains                  | Extension(s)                   | Notes                                         |
|----------------------|----------------------|----------------------------|--------------------------------|-----------------------------------------------|
| PEM                  | Base64 + headers     | Keys, certs, CSRs         | .pem, .crt, .cer, .key         | Human-readable; widely used in Unix/Linux     |
| DER                  | Binary               | Keys, certs               | .der, .cer                     | Compact; used in Windows & Java               |
| PFX / PKCS#12        | Binary (encrypted)   | Cert + private key        | .pfx, .p12                     | Password-protected; common in Windows         |
| PKCS#7 / P7B         | Base64 or binary     | Certificate chain (no key) | .p7b, .p7c                     | Used in Windows & Java; supports cert chains  |
| CSR (PKCS#10)        | Base64 or binary     | Certificate request        | .csr                           | Sent to CA for certificate issuance           |
| JWK / JWKS           | JSON                 | Web keys                  | .json, .jwk, .jwks             | Used in OAuth, OpenID, JWT                    |
| KEY                  | Usually PEM          | Private key only          | .key                           | Not standardized; convention-based naming     |
| CRT / CER            | PEM or DER           | Certificate               | .crt, .cer                     | Extensions vary by platform                   |
## 🧠 Quick Tips
- PEM vs DER: PEM is Base64-encoded and readable; DER is binary and compact.
- PFX: Ideal for bundling certs + private keys securely.
- PKCS#7: Great for sharing cert chains without private keys.
- JWK: Tailored for web apps and APIs — not compatible with OpenSSL directly.
# Cryptographic Algorithms primitives:
## 🧠 One-Way Functions = Hash Functions
- Definition: Easy to compute in one direction, but hard (ideally impossible) to reverse.
- Examples:
  - SHA-2, SHA-3, MD5, BLAKE2
  - Password hashing (e.g. bcrypt, scrypt)
- Use Cases:
  - Data integrity
  - Digital signatures
  - Password storage
- ✅ No decryption possible — output is fixed-length and irreversible.
## 🔄 Two-Way Functions = Symmetric, Asymmetric, Certificates
| Type                  | Description                                | Examples                | Reversible?           |
|-----------------------|--------------------------------------------|-------------------------|------------------------|
| Symmetric Encryption  | Same key for encryption & decryption       | AES, DES, ChaCha20      | ✅ Yes                |
| Asymmetric Encryption | Public key encrypts, private key decrypts  | RSA, ECC                | ✅ Yes                |
| Digital Certificates  | Bundle public key with identity info       | X.509, TLS certs        | ✅ Yes (via key pair) |

- These are reversible operations — you can decrypt or verify if you have the right key.
- Digital certificates use asymmetric keys to establish trust and secure communication.
## 🧩 Bonus: Hybrid Systems
Many real-world systems combine both:
- PGP, TLS, SSH use asymmetric encryption to exchange a symmetric key, then switch to fast symmetric encryption.
- Digital signatures use hash functions + asymmetric keys.

So yes, your classification works well as a mental model:
- One-way = irreversible hashing
- Two-way = reversible encryption and identity binding
# Asymmetric Algorithms vs Digital Certificates
## 🔑 Asymmetric Algorithms
- Public key → encrypts
- Private key → decrypts
- 📬 Purpose: Confidential communication  Anyone can encrypt a message for you using your public key; only you (with your private key) can open it.
## 📄 Digital Certificates
- Private key is used for signing, not encryption
- Public key is used for verifying the signature, not decryption

Digital certificates are used to prove identity, not to encrypt a message.
- 🔏 Private key → signs data
- ✅ Public key → verifies that signature
- 📄 The certificate itself bundles your public key + identity info, issued by a trusted authority
## 🧠 Summary Matrix
| Goal              | Key Used     | Direction                  |
|-------------------|--------------|----------------------------|
| Encrypt data      | Public key   | Sender → Receiver          |
| Decrypt data      | Private key  | Receiver ← Sender          |
| Sign data         | Private key  | Sender → Signature         |
| Verify signature  | Public key   | Receiver ← Signature       |
## Encryption vs Signing
### 🔒 Encryption: Keeping Secrets
Goal: Ensure confidentiality — only the intended recipient can read the message.
| Step | Action                                                                    |
|------|---------------------------------------------------------------------------|
| 1    | Sender encrypts the message using the recipient’s **public key**          |
| 2    | Only the recipient’s **private key** can decrypt the message              |

🔐 The message remains unreadable to anyone else during transmission.          |

📌 Used for: Secure messaging, file protection, TLS/SSL, VPNs
### ✍️ Signing: Proving Identity & Integrity
Goal: Ensure authenticity, integrity, and non-repudiation — prove who sent the message and that it wasn’t altered.
| Step | Description                                                                 |
|------|------------------------------------------------------------------------------|
| 1    | Sender creates a **hash** of the message                                    |
| 2    | Hash is **encrypted with sender’s private key** (this becomes the signature) |
| 3    | Recipient uses the **sender’s public key** to verify the signature          |

➡️ This ensures message **authenticity** and **integrity** during digital communications.

📌 Used for: Digital signatures, software distribution, legal documents
### 🧠 Key Differences
| Feature      | Encryption                                             | Signing                                                  |
|--------------|--------------------------------------------------------|----------------------------------------------------------|
| **Purpose**  | Ensures message confidentiality                        | Ensures message authenticity and integrity               |
| **Key Used** | Encrypt: Public key<br>Decrypt: Private key            | Sign: Private key<br>Verify: Public key                  |
| **Visibility** | Encrypted message is hidden                          | Message remains visible; signature proves origin         |
| **Reversible?** | Yes — original message can be decrypted             | Yes — signature can be verified using public key         |
### 🔄 Often Used Together
In secure systems like PGP, TLS, or email encryption, both are used:
- 🔐 Encrypt the message so only the recipient can read it
- ✍️ Sign the message so the recipient knows it came from you
# Encryption vs Signing with OpenSSL
## 🔒 Encryption with OpenSSL (Confidentiality)
Goal: Make data unreadable to anyone except the intended recipient.
```shell
# Prepare demo folder:
mkdir Cryptography_Demo
cd Cryptography_Demo
ls -la
# Create a message to be encrypted
echo "secret password" > message.txt
ls -la
cat message.txt
# Generate RSA key pair:
openssl genpkey -algorithm RSA -out private.pem -pkeyopt rsa_keygen_bits:2048
ls -la
cat private.pem
openssl rsa -in private.pem -pubout -out public.pem
ls -la
cat public.pem
# Encrypt a file using the recipient’s public key:
openssl pkeyutl -encrypt -inkey public.pem -pubin -in message.txt -out message.enc
ls -la
cat message.enc
# delete the original message.txt, so we can retrieve it from the encrypted file (ciphertext)
rm -rf message.txt
ls -la
# Decrypt using the recipient’s private key:
openssl pkeyutl -decrypt -inkey private.pem -in message.enc -out message.dec
ls -la
cat message.dec
```
## ✍️ Signing with OpenSSL (Authenticity & Integrity)
Goal: Prove the sender’s identity and ensure the message hasn’t been tampered with.
```shell
# Prepare demo folder:
mkdir Cryptography_Demo
cd Cryptography_Demo
ls -la
# Create a message to be encrypted
echo "secret password" > message.txt
ls -la
cat message.txt
# Generate RSA key pair:
openssl genpkey -algorithm RSA -out private.pem -pkeyopt rsa_keygen_bits:2048
ls -la
cat private.pem
openssl rsa -in private.pem -pubout -out public.pem
# List possible hash functions:
openssl dgst -list
# Create a hash of the message:
openssl dgst -sha3-512 -sign private.pem -out message.sig message.txt
ls -la
cat message.sig
# Verify the signature using the sender’s public key:
openssl dgst -sha3-512 -verify public.pem -signature message.sig message.txt
```
## 🧠 Summary Table
| Feature             | Encryption                     | Signing                           |
|---------------------|--------------------------------|-----------------------------------|
| **Purpose**         | Confidentiality                | Authenticity & Integrity          |
| **Key Used**        | Public key to encrypt          | Private key to sign               |
| **Verified By**     | Private key to decrypt         | Public key to verify              |
| **Output**          | Ciphertext                     | Signature                         |
| **Message Hidden?** | ✅ Yes                          | ❌ No (message stays readable)    |
# OpenSSL Supported Digests
```shell
openssl dgst -list
```
## 🔐 SHA Hash Algorithm Comparison Table
| Algorithm       | SHA Family | Output Size | Block Size | Structure         | Notes                                        |
|----------------|------------|-------------|------------|-------------------|----------------------------------------------|
| SHA-1          | SHA-1      | 160 bits    | 512 bits   | Merkle–Damgård    | ❌ Deprecated due to collision vulnerabilities |
| SHA-224        | SHA-2      | 224 bits    | 512 bits   | Merkle–Damgård    | Truncated version of SHA-256                  |
| SHA-256        | SHA-2      | 256 bits    | 512 bits   | Merkle–Damgård    | Widely used; strong security                  |
| SHA-384        | SHA-2      | 384 bits    | 1024 bits  | Merkle–Damgård    | Truncated SHA-512; better performance         |
| SHA-512        | SHA-2      | 512 bits    | 1024 bits  | Merkle–Damgård    | High security; slower processing              |
| SHA-512/224    | SHA-2      | 224 bits    | 1024 bits  | Merkle–Damgård    | SHA-512 variant with reduced output           |
| SHA-512/256    | SHA-2      | 256 bits    | 1024 bits  | Merkle–Damgård    | SHA-512 variant with reduced output           |
| SHA3-224       | SHA-3      | 224 bits    | 1152 bits  | Sponge (Keccak)   | Resistant to length extension attacks         |
| SHA3-256       | SHA-3      | 256 bits    | 1088 bits  | Sponge (Keccak)   | SHA-3 alternative to SHA-256                  |
| SHA3-384       | SHA-3      | 384 bits    | 832 bits   | Sponge (Keccak)   | Higher security; slower speed                 |
| SHA3-512       | SHA-3      | 512 bits    | 576 bits   | Sponge (Keccak)   | Strongest SHA-3 variant                       |
## 🧠 Quick Family Overview
- SHA-1: Legacy algorithm, now deprecated due to vulnerabilities.
- SHA-2: Robust and widely adopted; includes multiple variants for different output sizes.
- SHA-3: Newer design based on Keccak sponge construction; not a direct upgrade to SHA-2 but an alternative.
# Generate a self-signed digital certificate using OpenSSL
```shell
# 1. Generate a Private Key
openssl genpkey -algorithm RSA -out private.key -pkeyopt rsa_keygen_bits:2048

# 2. Create a Certificate Signing Request (CSR)
openssl req -new -key private.key -out request.csr
# You'll be prompted to enter details like country, organization, and domain name.

# 3. Generate a Self-Signed Certificate
openssl req -x509 -key private.key -in request.csr -out certificate.crt -days 365
# Produces a certificate valid for 1 year.

# 📦 Optional: Combine All in One Command
openssl req -x509 -newkey rsa:2048 -keyout private.key -out certificate.crt -days 365 -nodes
# Skips CSR creation and generates both key and cert in one go.
# -nodes means the private key won’t be password-protected.

# View Certificate Details
openssl x509 -in certificate.crt -text -noout
# Displays human-readable info about the certificate.
```
# Add Subject Alternative Names (SAN) to your self-signed certificate using OpenSSL
```shell
# 1. Create a Private Key
openssl genpkey -algorithm RSA -out private.key -pkeyopt rsa_keygen_bits:2048

# 2. Create a Custom Config File (san.cnf)
ini
[req]
default_bits       = 2048
prompt             = no
default_md         = sha256
distinguished_name = dn
req_extensions     = req_ext

[dn]
C  = CA
ST = Quebec
L  = Montreal
O  = MyCompany
OU = Dev
CN = example.com

[req_ext]
subjectAltName = @alt_names

[alt_names]
DNS.1 = example.com
DNS.2 = www.example.com
IP.1  = 192.168.1.10

# 3. Generate a CSR with SAN
openssl req -new -key private.key -out request.csr -config san.cnf

# 4. Generate a Self-Signed Certificate with SAN
openssl x509 -req -in request.csr -signkey private.key -out certificate.crt -days 365 -extensions req_ext -extfile san.cnf

# 5. Verify SAN in the Certificate
openssl x509 -in certificate.crt -text -noout | grep -A 1 "Subject Alternative Name"
```
## 🧠 Why This Works
- The subjectAltName field is defined in the [req_ext] section.
- The -extensions req_ext -extfile san.cnf flags ensure SANs are embedded in the final certificate.
- This method avoids browser warnings (especially in Chrome and Firefox) that reject certs without SAN.

Sources:
- https://techoverflow.net/2022/12/04/how-to-create-self-signed-certificate-with-san-subjectaltname-using-openssl/
- https://gist.github.com/KeithYeh/bb07cadd23645a6a62509b1ec8986bbc
- https://transang.me/create-a-multiple-domains-self-signed-ssl-certificate-with-testing-scripts/
# Common Digital Certificate Formats
| Format           | Type                      | File Extension(s)         | Notes                                                          |
|------------------|---------------------------|---------------------------|----------------------------------------------------------------|
| PEM              | Base64-encoded            | .pem, .crt, .cer, .key    | Human-readable; includes headers like `-----BEGIN CERTIFICATE-----` |
| DER              | Binary                    | .der, .cer                | Compact binary format; often used in Windows                   |
| PFX / PKCS#12    | Binary (encrypted)        | .pfx, .p12                | Contains both certificate and private key; password protected |
| PKCS#7 / P7B     | Base64 or binary          | .p7b, .p7c                | Includes certificate chain; no private key                    |
| CSR (PKCS#10)    | Base64 or binary          | .csr                      | Certificate Signing Request for CA issuance                   |
| JWK / JWKS       | JSON                      | .json, .jwk, .jwks        | JSON Web Key; used in OAuth, JWT, and OpenID Connect          |
| KEY              | Typically PEM             | .key                      | Stores private key; format depends on use case                |
| CRT / CER        | PEM or DER                | .crt, .cer                | Stores public certificate; extension varies by platform       |
## 🧠 Quick Tips
- PEM is the most flexible and readable — great for manual inspection and OpenSSL.
- DER is binary and compact — preferred in Windows and Java environments.
- PFX is ideal for bundling certs + private keys securely — often used in IIS and enterprise systems.
- PKCS#7 is great for sharing cert chains — but doesn’t include private keys.
- CSR is used to request a certificate from a CA — it contains your public key and identity info.
# Cipher Suite
## 🔐 Common Places You’ll Find Cipher Suites
| Location / Context             | Description                                                                 |
|-------------------------------|-----------------------------------------------------------------------------|
| **Web Servers**               | During HTTPS connections, servers and browsers negotiate cipher suites     |
| **TLS/SSL Handshake**         | Cipher suites are selected to define encryption, authentication, and integrity |
| **VPNs and Secure Tunnels**   | Used to secure data in transit via protocols like IPSec or OpenVPN         |
| **Email Servers**             | For securing SMTP, IMAP, and POP3 over TLS                                 |
| **APIs and Web Services**     | RESTful APIs often use TLS with defined cipher suites for secure access     |
| **Cloud Platforms**           | Cipher suite settings are configurable in services like AWS, Azure, GCP    |
| **Operating Systems & Browsers** | Maintain lists of supported cipher suites for TLS connections           |
| **Security Scanners**         | Tools like Qualys or Nessus report supported/weak cipher suites on endpoints |

Cipher suites are essentially the recipe for how encryption and authentication are handled during a secure session. They combine algorithms for key exchange, encryption, and message authentication.
## 🧩 Components of a Cipher Suite
| Part                       | Role                                                                 | Examples                          |
|----------------------------|----------------------------------------------------------------------|-----------------------------------|
| Protocol Identifier        | Specifies the protocol (usually TLS)                                 | TLS_, SSL_                        |
| Key Exchange Algorithm     | Establishes shared secret between client and server                  | RSA, DHE, ECDHE, PSK              |
| Authentication Algorithm   | Verifies identity of the server (and optionally the client)          | RSA, DSA, ECDSA                   |
| Bulk Encryption Algorithm  | Encrypts the actual data being transmitted                           | AES, 3DES, ChaCha20               |
| Encryption Mode            | Defines how encryption is applied                                    | CBC, GCM, CCM, Poly1305           |
| MAC / Hash Algorithm       | Ensures data integrity and authenticity                              | SHA-1, SHA-256, SHA-384           |

## 🔍 Example Breakdown
```shell
TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256
```
It means:
- TLS: Protocol
- ECDHE: Ephemeral Elliptic Curve - Diffie-Hellman (key exchange)
- RSA: Authentication
- AES_128_GCM: 128-bit AES in Galois/Counter Mode (bulk encryption)
- SHA256: Hash function for integrity
## 🧠 TLS 1.3 Simplification
TLS 1.3 streamlines cipher suites by:
- Removing separate key exchange and authentication identifiers
- Only supporting AEAD (Authenticated Encryption with Associated Data) modes
- Using HKDF for key derivation
Example:
```shell
TLS_AES_256_GCM_SHA384
```
# Cryptography + TLS
TLS uses both symmetric and asymmetric algorithms
## 🔐 TLS = Hybrid Encryption
TLS (Transport Layer Security) combines the strength of asymmetric encryption with the speed of symmetric encryption:
| Phase         | Algorithm Type                   | Purpose                                                  |
|---------------|----------------------------------|----------------------------------------------------------|
| Handshake     | 🧠 Asymmetric (e.g. RSA, ECDHE)   | Securely exchange keys and authenticate identity        |
| Data Transfer | ⚡ Symmetric (e.g. AES, ChaCha20) | Encrypt bulk data efficiently                           |
## 🧠 How It Works
1. Client connects to server (e.g. visiting a website).
2. Server presents its digital certificate (contains public key).
3. Client verifies the certificate and uses the public key to securely exchange a symmetric session key.
4. Both sides now use the shared symmetric key to encrypt and decrypt all data.

This is called a hybrid encryption model — asymmetric for setup, symmetric for speed.
# Evolution of TLS (Transport Layer Security) versions:
| TLS Version | Cipher Suite Types                    | Key Exchange               | Encryption                | MAC / AEAD         | Notes                                                       |
|-------------|----------------------------------------|----------------------------|---------------------------|---------------------|-------------------------------------------------------------|
| TLS 1.0     | Legacy suites (RSA, 3DES, RC4)         | RSA, DH, DHE               | DES, 3DES, RC4            | MD5, SHA-1          | ❌ Weak security; deprecated                                 |
| TLS 1.1     | Same as TLS 1.0 + explicit IV for CBC  | RSA, DH, DHE               | DES, 3DES, RC4            | MD5, SHA-1          | ❌ Minor improvements; still deprecated                      |
| TLS 1.2     | Modern suites (AES, GCM, ChaCha20)     | RSA, DH, DHE, ECDHE        | AES-CBC, AES-GCM, ChaCha20| SHA-2, AEAD         | ✅ Widely used; supports authenticated encryption            |
| TLS 1.3     | AEAD-only suites (AES-GCM, ChaCha20)   | ECDHE, X25519              | AES-GCM, ChaCha20         | AEAD only           | ✅ Simplified; provides forward secrecy by default           |
## 🧠 Highlights
- TLS 1.0 & 1.1: Support outdated ciphers like RC4 and 3DES — vulnerable to attacks.
- TLS 1.2: Introduced support for authenticated encryption (AEAD) and SHA-2.
- TLS 1.3: Removed legacy algorithms (RSA key exchange, static DH), supports only 5 secure cipher suites, including:
  - TLS_AES_128_GCM_SHA256
  - TLS_AES_256_GCM_SHA384
  - TLS_CHACHA20_POLY1305_SHA256
# TLS Handshake: Step-by-Step Breakdown
## 🔐 TLS Handshake Steps

| Step                     | Description                                                                 |
|--------------------------|-----------------------------------------------------------------------------|
| **1. Client Hello**      | Client sends supported TLS versions, cipher suites, and a random number     |
| **2. Server Hello**      | Server replies with chosen TLS version, cipher suite, and its own random    |
| **3. Server Certificate**| Server sends digital certificate with public key to prove identity          |
| **4. Key Exchange**      | Client encrypts premaster secret with server’s public key and sends it      |
| **5. Session Key Derivation** | Both derive shared symmetric key from premaster and randoms          |
| **6. Finished Messages** | Each sends a message encrypted with session key to confirm successful setup |
| **Secure Communication Begins** | All subsequent data is encrypted using the shared session key     |
## 🧠 Analogy Time
Imagine two spies meeting in a café:
- They exchange codebooks (public keys).
- Whisper a secret phrase (premaster secret).
- Use that to create a shared language (session key).
- Then they talk in code (encrypted data) — and no one else can understand.
