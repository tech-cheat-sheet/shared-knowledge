- [CompTIA Security+ Exam SY0-701](#comptia-security-exam-sy0-701)
- [1.0 General Security Concepts](#10-general-security-concepts)
  - [1.1 Compare and contrast various types of security controls](#11-compare-and-contrast-various-types-of-security-controls)
    - [📂 Categories of Security Controls](#-categories-of-security-controls)
    - [🧭 Types of Security Controls](#-types-of-security-controls)
    - [🔍 Summary](#-summary)
  - [1.2 Summarize fundamental security concepts](#12-summarize-fundamental-security-concepts)
    - [🧱 Core Principles](#-core-principles)
      - [🔒 CIA Triad](#-cia-triad)
      - [🧾 Non-Repudiation](#-non-repudiation)
    - [🔐 AAA Model (Authentication, Authorization, Accounting)](#-aaa-model-authentication-authorization-accounting)
      - [👤 Authentication](#-authentication)
      - [✅ Authorization](#-authorization)
      - [📊 Accounting](#-accounting)
    - [🔍 Gap Analysis](#-gap-analysis)
    - [🚫 Zero Trust Architecture](#-zero-trust-architecture)
      - [🧠 Control Plane](#-control-plane)
      - [📡 Data Plane](#-data-plane)
    - [🏢 Physical Security](#-physical-security)
      - [🔍 Sensor Types](#-sensor-types)
    - [🕵️ Deception and Disruption Technologies](#️-deception-and-disruption-technologies)
  - [1.3 Explain the importance of change management processes and the impact to security](#13-explain-the-importance-of-change-management-processes-and-the-impact-to-security)
    - [🏢 Business Processes Impacting Security Operations](#-business-processes-impacting-security-operations)
    - [⚙️ Technical Implications](#️-technical-implications)
    - [📚 Documentation](#-documentation)
    - [🔐 Security Impact Summary](#-security-impact-summary)
  - [1.4 Explain the importance of using appropriate cryptographic solutions](#14-explain-the-importance-of-using-appropriate-cryptographic-solutions)
    - [🏛️ Public Key Infrastructure (PKI)](#️-public-key-infrastructure-pki)
    - [🔒 Encryption](#-encryption)
      - [📦 Levels of Encryption](#-levels-of-encryption)
      - [📡 Transport/Communication Encryption](#-transportcommunication-encryption)
      - [🔐 Encryption Types](#-encryption-types)
      - [🧮 Algorithms and Key Length](#-algorithms-and-key-length)
    - [🛠️ Cryptographic Tools](#️-cryptographic-tools)
    - [🧩 Obfuscation Techniques](#-obfuscation-techniques)
    - [🔁 Hashing and Integrity](#-hashing-and-integrity)
    - [✍️ Digital Signatures](#️-digital-signatures)
    - [⛓️ Blockchain and Ledgers](#️-blockchain-and-ledgers)
    - [📜 Certificates](#-certificates)
- [2.0 Threats, Vulnerabilities, and Mitigations](#20-threats-vulnerabilities-and-mitigations)
  - [2.1 Compare and contrast common threat actors and motivations](#21-compare-and-contrast-common-threat-actors-and-motivations)
    - [👥 Common Threat Actors](#-common-threat-actors)
    - [🧬 Attributes of Threat Actors](#-attributes-of-threat-actors)
    - [🎯 Motivations Behind Attacks](#-motivations-behind-attacks)
    - [🧠 Summary](#-summary-1)
# CompTIA Security+ Exam SY0-701
# 1.0 General Security Concepts
## 1.1 Compare and contrast various types of security controls
Security controls are mechanisms used to reduce risk, protect assets, and ensure compliance. They are categorized by how they are implemented and the purpose they serve.
### 📂 Categories of Security Controls
| Category     | Description | Examples |
|--------------|-------------|----------|
| **Technical** | Implemented via hardware/software | Firewalls, antivirus, encryption, access controls |
| **Managerial** | Defined by policies and procedures | Risk assessments, security policies, audits |
| **Operational** | Day-to-day practices and processes | Security awareness training, incident response |
| **Physical** | Protect physical access to systems | Locks, cameras, fences, biometric scanners |
### 🧭 Types of Security Controls
| Control Type   | Purpose | Examples |
|----------------|--------|----------|
| **Preventive** | Stops incidents before they occur | Firewalls, access control lists, encryption |
| **Deterrent**  | Discourages malicious activity | Warning signs, security cameras, policies |
| **Detective**  | Identifies and alerts on incidents | IDS/IPS, audit logs, CCTV monitoring |
| **Corrective** | Restores systems after an incident | Backup restoration, patching, reconfiguration |
| **Compensating** | Alternative control when primary is not feasible | Manual reviews, additional monitoring |
| **Directive**  | Guides behavior and actions | Security policies, training, procedures |
### 🔍 Summary
- **Technical vs. Operational**: Technical controls are automated, while operational controls rely on human actions.
- **Preventive vs. Detective**: Preventive stops threats; detective identifies them after they occur.
- **Corrective vs. Compensating**: Corrective fixes issues; compensating fills gaps when ideal controls aren't possible.
- **Directive vs. Deterrent**: Directive instructs; deterrent discourages.
## 1.2 Summarize fundamental security concepts
Security principles form the foundation of protecting systems, data, and users. These concepts span digital, physical, and strategic domains.
### 🧱 Core Principles
#### 🔒 CIA Triad
| Principle       | Description |
|----------------|-------------|
| **Confidentiality** | Ensures data is accessible only to authorized users |
| **Integrity**       | Ensures data is accurate and unaltered |
| **Availability**    | Ensures systems and data are accessible when needed |
#### 🧾 Non-Repudiation
- Guarantees that actions or communications cannot be denied.
- Achieved through digital signatures, logging, and secure protocols.
### 🔐 AAA Model (Authentication, Authorization, Accounting)
#### 👤 Authentication
- **People**: Passwords, biometrics, MFA.
- **Systems**: Certificates, keys, mutual TLS.
#### ✅ Authorization
- Determines what an authenticated user/system can access.
- **Models**:
  - Role-Based Access Control (RBAC)
  - Attribute-Based Access Control (ABAC)
  - Mandatory Access Control (MAC)
  - Discretionary Access Control (DAC)
#### 📊 Accounting
- Tracks user/system activity.
- Used for auditing, billing, and forensic analysis.
### 🔍 Gap Analysis
- Identifies discrepancies between current security posture and desired state.
- Used to prioritize improvements and align with compliance standards.
### 🚫 Zero Trust Architecture
Security model that assumes no implicit trust, even within the network perimeter.
#### 🧠 Control Plane
| Component                  | Description |
|---------------------------|-------------|
| **Adaptive Identity**      | Dynamically adjusts access based on context |
| **Threat Scope Reduction** | Limits exposure by minimizing trust zones |
| **Policy-Driven Access Control** | Enforces granular access rules |
| **Policy Administrator**   | Distributes policies to enforcement points |
| **Policy Engine**          | Evaluates access requests against policies |
#### 📡 Data Plane
| Component                  | Description |
|---------------------------|-------------|
| **Implicit Trust Zones**   | Legacy concept eliminated in Zero Trust |
| **Subject/System**         | Entity requesting access |
| **Policy Enforcement Point (PEP)** | Enforces access decisions from the control plane |
### 🏢 Physical Security
| Control                  | Purpose |
|--------------------------|---------|
| **Bollards**             | Prevent vehicle-based intrusion |
| **Access Control Vestibule** | Manages secure entry to buildings |
| **Fencing**              | Defines perimeter boundaries |
| **Video Surveillance**   | Monitors and records activity |
| **Security Guard**       | Provides human oversight and response |
| **Access Badge**         | Controls entry based on identity |
| **Lighting**             | Enhances visibility and deters intruders |
| **Sensors**              | Detect unauthorized access |
#### 🔍 Sensor Types
- **Infrared**: Detects heat signatures
- **Pressure**: Detects weight or movement
- **Microwave**: Detects motion via wave disruption
- **Ultrasonic**: Detects movement using sound waves
### 🕵️ Deception and Disruption Technologies
| Technology     | Description |
|----------------|-------------|
| **Honeypot**   | Decoy system to attract attackers |
| **Honeynet**   | Network of honeypots simulating a full environment |
| **Honeyfile**  | Fake file used to detect unauthorized access |
| **Honeytoken** | Embedded data that triggers alerts when accessed |
## 1.3 Explain the importance of change management processes and the impact to security
Change management ensures that modifications to systems, applications, and infrastructure are planned, tested, and documented to minimize risk and maintain security posture.
### 🏢 Business Processes Impacting Security Operations
Effective change management aligns technical changes with business goals while safeguarding operations.
| Element              | Description |
|----------------------|-------------|
| **Approval Process** | Ensures changes are reviewed and authorized by appropriate personnel |
| **Ownership**        | Assigns responsibility for implementing and maintaining changes |
| **Stakeholders**     | Involves relevant parties (e.g., IT, security, compliance) in decision-making |
| **Impact Analysis**  | Assesses potential effects on systems, users, and security |
| **Test Results**     | Validates that changes work as intended without introducing vulnerabilities |
| **Backout Plan**     | Provides a rollback strategy in case of failure |
| **Maintenance Window** | Schedules changes during low-impact periods to reduce disruption |
| **Standard Operating Procedure (SOP)** | Ensures consistency and repeatability in change execution |
### ⚙️ Technical Implications
Changes can affect system behavior, security controls, and service availability.

| Element              | Description |
|----------------------|-------------|
| **Allow Lists / Deny Lists** | Must be updated to reflect new services or restrictions |
| **Restricted Activities** | May need to be redefined based on new configurations |
| **Downtime**         | Planned outages must be communicated and secured |
| **Service Restart**  | Can impact availability and session persistence |
| **Application Restart** | May affect user access and data integrity |
| **Legacy Applications** | Often fragile and may not support modern security controls |
| **Dependencies**     | Changes to one system may affect others; must be mapped and tested |
### 📚 Documentation
Accurate documentation ensures traceability, accountability, and future readiness.

| Element              | Description |
|----------------------|-------------|
| **Updating Diagrams** | Reflects new architecture, connections, and security zones |
| **Updating Policies/Procedures** | Aligns operational practices with current configurations |
| **Version Control**  | Tracks changes to configurations, code, and documentation for audit and rollback purposes |
### 🔐 Security Impact Summary
- Poorly managed changes can introduce vulnerabilities, misconfigurations, and downtime.
- Proper change management enhances visibility, accountability, and resilience.
- Security teams must be involved in every stage—from planning to post-implementation review.
## 1.4 Explain the importance of using appropriate cryptographic solutions
Cryptography is essential for securing data, verifying identities, and ensuring trust in digital systems. Choosing the right cryptographic tools and techniques helps protect confidentiality, integrity, and authenticity.
### 🏛️ Public Key Infrastructure (PKI)
PKI enables secure communication and identity verification through asymmetric encryption.

| Component     | Description |
|---------------|-------------|
| **Public Key** | Shared openly; used to encrypt or verify data |
| **Private Key**| Kept secret; used to decrypt or sign data |
| **Key Escrow** | Third-party storage of keys for recovery or compliance |
### 🔒 Encryption
Encryption transforms readable data into unreadable format to prevent unauthorized access.
#### 📦 Levels of Encryption
| Level        | Description |
|--------------|-------------|
| **Full-Disk** | Encrypts entire storage device |
| **Partition** | Encrypts specific disk partitions |
| **File**      | Encrypts individual files |
| **Volume**    | Encrypts logical storage volumes |
| **Database**  | Encrypts entire databases or tables |
| **Record**    | Encrypts individual rows or entries in a database |
#### 📡 Transport/Communication Encryption
- Protects data in transit (e.g., TLS, VPN).
- Ensures secure communication between endpoints.
#### 🔐 Encryption Types
| Type        | Description |
|-------------|-------------|
| **Symmetric** | Same key used for encryption and decryption (e.g., AES) |
| **Asymmetric**| Uses public/private key pair (e.g., RSA) |
| **Key Exchange** | Securely shares keys (e.g., Diffie-Hellman, ECDH) |
#### 🧮 Algorithms and Key Length
- **Algorithms**: AES, RSA, ECC, ChaCha20, Blowfish.
- **Key Length**: Longer keys = stronger security (e.g., 256-bit AES).
### 🛠️ Cryptographic Tools
| Tool                     | Description |
|--------------------------|-------------|
| **Trusted Platform Module (TPM)** | Hardware chip for secure key storage and device integrity |
| **Hardware Security Module (HSM)** | Dedicated hardware for managing and protecting cryptographic keys |
| **Key Management System (KMS)** | Centralized solution for generating, storing, and rotating keys |
| **Secure Enclave**       | Isolated environment for secure processing and key storage (e.g., Apple Secure Enclave) |
### 🧩 Obfuscation Techniques
| Technique     | Description |
|---------------|-------------|
| **Steganography** | Hides data within other media (e.g., images, audio) |
| **Tokenization**  | Replaces sensitive data with non-sensitive tokens |
| **Data Masking**  | Obscures data to protect privacy during testing or sharing |
### 🔁 Hashing and Integrity
- **Hashing**: Converts data into fixed-length digest (e.g., SHA-256).
- **Salting**: Adds random data to input before hashing to prevent dictionary attacks.
- **Key Stretching**: Strengthens weak passwords using algorithms like PBKDF2, bcrypt, scrypt.
### ✍️ Digital Signatures
- Verifies authenticity and integrity of data.
- Uses private key to sign and public key to verify.
### ⛓️ Blockchain and Ledgers
| Concept              | Description |
|----------------------|-------------|
| **Blockchain**       | Distributed ledger using cryptographic hashes |
| **Open Public Ledger** | Transparent record of transactions, often used in cryptocurrency |
### 📜 Certificates
Used to verify identities and establish trust in PKI systems.
| Component                     | Description |
|------------------------------|-------------|
| **Certificate Authorities (CAs)** | Trusted entities that issue digital certificates |
| **Certificate Revocation Lists (CRLs)** | Lists of invalidated certificates |
| **Online Certificate Status Protocol (OCSP)** | Real-time certificate validation |
| **Self-Signed**              | Issued by the entity itself; less trusted |
| **Third-Party**              | Issued by a recognized CA |
| **Root of Trust**            | Foundation of trust in a certificate chain |
| **Certificate Signing Request (CSR)** | Request to a CA for certificate issuance |
| **Wildcard Certificate**     | Secures multiple subdomains under one certificate (e.g., `*.example.com`) |
# 2.0 Threats, Vulnerabilities, and Mitigations
## 2.1 Compare and contrast common threat actors and motivations
Understanding threat actors—their capabilities, resources, and motivations—is essential for building effective defense strategies and risk assessments.
### 👥 Common Threat Actors
| Threat Actor      | Description | Typical Motivation |
|-------------------|-------------|---------------------|
| **Nation-State**  | Government-sponsored groups targeting other nations or corporations | Espionage, disruption, warfare |
| **Unskilled Attacker** | Individuals with limited knowledge using readily available tools | Curiosity, chaos, bragging rights |
| **Hacktivist**    | Ideologically driven attackers promoting political or social causes | Disruption, awareness, protest |
| **Insider Threat**| Employees or contractors with authorized access who misuse it | Revenge, financial gain, espionage |
| **Organized Crime**| Sophisticated criminal groups targeting financial assets | Financial gain, blackmail |
| **Shadow IT**     | Unauthorized systems or applications deployed by employees | Convenience, bypassing restrictions |
### 🧬 Attributes of Threat Actors
| Attribute               | Internal vs. External | Resources/Funding | Sophistication |
|------------------------|-----------------------|-------------------|----------------|
| **Nation-State**        | External              | High              | Advanced       |
| **Unskilled Attacker**  | External              | Low               | Low            |
| **Hacktivist**          | External              | Variable          | Moderate       |
| **Insider Threat**      | Internal              | Variable          | Moderate–High  |
| **Organized Crime**     | External              | High              | Advanced       |
| **Shadow IT**           | Internal              | Low               | Low–Moderate   |
### 🎯 Motivations Behind Attacks
| Motivation                  | Description |
|----------------------------|-------------|
| **Data Exfiltration**      | Stealing sensitive or proprietary data |
| **Espionage**              | Gathering intelligence for political or economic advantage |
| **Service Disruption**     | Interrupting operations (e.g., DDoS, ransomware) |
| **Blackmail**              | Demanding ransom or leverage through threats |
| **Financial Gain**         | Theft, fraud, or extortion for profit |
| **Philosophical/Political Beliefs** | Driven by ideology or activism |
| **Ethical**                | "White hat" actions to expose vulnerabilities |
| **Revenge**                | Personal retaliation against an organization |
| **Disruption/Chaos**       | Causing instability for entertainment or ideology |
| **War**                    | Cyber warfare as part of military strategy |
### 🧠 Summary
- **Nation-states and organized crime** are the most well-funded and sophisticated.
- **Insider threats and shadow IT** pose unique risks due to their internal access.
- **Hacktivists and ethical hackers** may not seek financial gain but can still cause disruption.
- Understanding the **motivation** helps tailor defenses and incident response strategies.
