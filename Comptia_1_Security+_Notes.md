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
  - [2.2 Explain common threat vectors and attack surfaces](#22-explain-common-threat-vectors-and-attack-surfaces)
    - [✉️ Message-Based Vectors](#️-message-based-vectors)
    - [🖼️ Image-Based Vectors](#️-image-based-vectors)
    - [📁 File-Based Vectors](#-file-based-vectors)
    - [📞 Voice Call Vectors](#-voice-call-vectors)
    - [💾 Removable Device Vectors](#-removable-device-vectors)
    - [🧱 Vulnerable Software](#-vulnerable-software)
    - [🧟 Unsupported Systems and Applications](#-unsupported-systems-and-applications)
    - [🌐 Unsecure Networks](#-unsecure-networks)
    - [🔓 Open Service Ports](#-open-service-ports)
    - [🔑 Default Credentials](#-default-credentials)
    - [🔗 Supply Chain Vectors](#-supply-chain-vectors)
    - [🧠 Human Vectors / Social Engineering](#-human-vectors--social-engineering)
    - [🧠 Summary](#-summary-2)
  - [2.3 Explain various types of vulnerabilities](#23-explain-various-types-of-vulnerabilities)
    - [🖥️ Application Vulnerabilities](#️-application-vulnerabilities)
    - [🧩 Operating System (OS)-Based Vulnerabilities](#-operating-system-os-based-vulnerabilities)
    - [🌐 Web-Based Vulnerabilities](#-web-based-vulnerabilities)
    - [🧱 Hardware Vulnerabilities](#-hardware-vulnerabilities)
    - [🧮 Virtualization Vulnerabilities](#-virtualization-vulnerabilities)
    - [☁️ Cloud-Specific Vulnerabilities](#️-cloud-specific-vulnerabilities)
    - [🔗 Supply Chain Vulnerabilities](#-supply-chain-vulnerabilities)
    - [🔐 Cryptographic Vulnerabilities](#-cryptographic-vulnerabilities)
    - [⚙️ Misconfiguration Vulnerabilities](#️-misconfiguration-vulnerabilities)
    - [📱 Mobile Device Vulnerabilities](#-mobile-device-vulnerabilities)
    - [🕳️ Zero-Day Vulnerabilities](#️-zero-day-vulnerabilities)
    - [🧠 Summary](#-summary-3)
  - [2.4 Given a scenario, analyze indicators of malicious activity](#24-given-a-scenario-analyze-indicators-of-malicious-activity)
    - [🦠 Malware Attacks](#-malware-attacks)
    - [🔐 Physical Attacks](#-physical-attacks)
    - [🌐 Network Attacks](#-network-attacks)
    - [🧩 Application Attacks](#-application-attacks)
    - [🔐 Cryptographic Attacks](#-cryptographic-attacks)
    - [🔑 Password Attacks](#-password-attacks)
    - [🚨 Indicators of Malicious Activity](#-indicators-of-malicious-activity)
    - [🧠 Summary](#-summary-4)
  - [2.5 Explain the purpose of mitigation techniques used to secure the enterprise](#25-explain-the-purpose-of-mitigation-techniques-used-to-secure-the-enterprise)
    - [🧩 Segmentation](#-segmentation)
    - [🔐 Access Control](#-access-control)
    - [✅ Application Allow List](#-application-allow-list)
    - [🧱 Isolation](#-isolation)
    - [🔧 Patching](#-patching)
    - [🔒 Encryption](#-encryption-1)
    - [📈 Monitoring](#-monitoring)
    - [🧑‍💼 Least Privilege](#-least-privilege)
    - [⚙️ Configuration Enforcement](#️-configuration-enforcement)
    - [🗑️ Decommissioning](#️-decommissioning)
    - [🛠️ Hardening Techniques](#️-hardening-techniques)
    - [🧠 Summary](#-summary-5)
- [3.0 Security Architecture](#30-security-architecture)
  - [3.1 Compare and contrast security implications of different architecture models](#31-compare-and-contrast-security-implications-of-different-architecture-models)
    - [☁️ Cloud Architecture](#️-cloud-architecture)
    - [🧾 Infrastructure as Code (IaC)](#-infrastructure-as-code-iac)
    - [🧠 Serverless Architecture](#-serverless-architecture)
    - [🧩 Microservices](#-microservices)
    - [🌐 Network Infrastructure](#-network-infrastructure)
    - [🏢 On-Premises](#-on-premises)
    - [🧭 Centralized vs. Decentralized](#-centralized-vs-decentralized)
    - [📦 Containerization](#-containerization)
    - [🖥️ Virtualization](#️-virtualization)
    - [📡 Internet of Things (IoT)](#-internet-of-things-iot)
    - [🏭 ICS / SCADA Systems](#-ics--scada-systems)
    - [⏱️ Real-Time Operating System (RTOS)](#️-real-time-operating-system-rtos)
    - [🔧 Embedded Systems](#-embedded-systems)
    - [🛠️ High Availability](#️-high-availability)
    - [📊 Key Considerations Across Architectures](#-key-considerations-across-architectures)
  - [3.2 Given a scenario, apply security principles to secure enterprise infrastructure](#32-given-a-scenario-apply-security-principles-to-secure-enterprise-infrastructure)
    - [🏗️ Infrastructure Considerations](#️-infrastructure-considerations)
    - [⚙️ Device Attributes](#️-device-attributes)
    - [🧱 Network Appliances](#-network-appliances)
    - [🔌 Port Security](#-port-security)
    - [🔥 Firewall Types](#-firewall-types)
    - [🔐 Secure Communication and Access](#-secure-communication-and-access)
    - [✅ Selection of Effective Controls](#-selection-of-effective-controls)
    - [🧠 Summary](#-summary-6)
  - [3.3 Compare and contrast concepts and strategies to protect data](#33-compare-and-contrast-concepts-and-strategies-to-protect-data)
    - [📂 Data Types](#-data-types)
    - [🏷️ Data Classifications](#️-data-classifications)
    - [📊 General Data Considerations](#-general-data-considerations)
      - [📌 Data States](#-data-states)
      - [🌍 Data Sovereignty \& Geolocation](#-data-sovereignty--geolocation)
    - [🛠️ Methods to Secure Data](#️-methods-to-secure-data)
    - [🧠 Summary](#-summary-7)
  - [3.4 Explain the importance of resilience and recovery in security architecture](#34-explain-the-importance-of-resilience-and-recovery-in-security-architecture)
    - [⚙️ High Availability](#️-high-availability-1)
    - [🏢 Site Considerations](#-site-considerations)
    - [🧬 Platform Diversity](#-platform-diversity)
    - [☁️ Multi-Cloud Systems](#️-multi-cloud-systems)
    - [🔄 Continuity of Operations](#-continuity-of-operations)
    - [📊 Capacity Planning](#-capacity-planning)
    - [🧪 Testing Strategies](#-testing-strategies)
    - [💾 Backup Strategies](#-backup-strategies)
    - [⚡ Power Resilience](#-power-resilience)
    - [🧠 Summary](#-summary-8)
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
## 2.2 Explain common threat vectors and attack surfaces
Threat vectors are pathways attackers use to infiltrate systems, while attack surfaces are the sum of all possible entry points. Understanding both is essential for reducing exposure and strengthening defenses.
### ✉️ Message-Based Vectors
| Medium         | Description | Risk |
|----------------|-------------|------|
| **Email**      | Used for phishing, malware delivery, and scams | High |
| **SMS**        | Smishing attacks via text messages | Moderate |
| **Instant Messaging (IM)** | Social engineering via chat platforms | Moderate |
### 🖼️ Image-Based Vectors
- **Description**: Malicious code embedded in image files (e.g., steganography).
- **Risk**: Can bypass filters and exploit vulnerabilities in image processing software.
### 📁 File-Based Vectors
- **Description**: Malware hidden in documents, executables, or compressed files.
- **Risk**: Common in phishing and drive-by download attacks.
### 📞 Voice Call Vectors
- **Description**: Vishing (voice phishing) to trick users into revealing sensitive info.
- **Risk**: Exploits trust and urgency over phone calls.
### 💾 Removable Device Vectors
- **Description**: USB drives or external media used to deliver malware.
- **Risk**: Bypasses network defenses; often used in insider or physical attacks.
### 🧱 Vulnerable Software
| Type           | Description | Risk |
|----------------|-------------|------|
| **Client-Based** | Requires installation; may have exploitable flaws | High |
| **Agentless**   | Web-based or remote access tools; may lack robust security | Moderate |
### 🧟 Unsupported Systems and Applications
- **Description**: Legacy systems no longer receiving updates or patches.
- **Risk**: High vulnerability to known exploits.
### 🌐 Unsecure Networks
| Type         | Description | Risk |
|--------------|-------------|------|
| **Wireless** | Susceptible to eavesdropping, rogue APs | High |
| **Wired**    | Vulnerable to physical tapping and MAC flooding | Moderate |
| **Bluetooth**| Exploitable via proximity-based attacks | Moderate |
### 🔓 Open Service Ports
- **Description**: Unused or misconfigured ports left open.
- **Risk**: Entry points for scanning, exploitation, and unauthorized access.
### 🔑 Default Credentials
- **Description**: Factory-set usernames/passwords not changed.
- **Risk**: Easily exploited by attackers using known credentials.
### 🔗 Supply Chain Vectors
| Entity                    | Description | Risk |
|---------------------------|-------------|------|
| **Managed Service Providers (MSPs)** | Third-party IT support | High |
| **Vendors**               | Software or hardware providers | Moderate |
| **Suppliers**             | External partners with access | Moderate |
### 🧠 Human Vectors / Social Engineering
| Technique                  | Description |
|----------------------------|-------------|
| **Phishing**               | Fraudulent emails to steal credentials |
| **Vishing**                | Voice-based phishing |
| **Smishing**               | SMS-based phishing |
| **Misinformation/Disinformation** | False info to manipulate behavior |
| **Impersonation**          | Pretending to be someone trusted |
| **Business Email Compromise (BEC)** | Hijacking or spoofing executive emails |
| **Pretexting**             | Creating a fabricated scenario to gain trust |
| **Watering Hole**          | Compromising websites frequented by targets |
| **Brand Impersonation**    | Mimicking trusted brands to deceive users |
| **Typosquatting**          | Registering misspelled domains to trick users |
### 🧠 Summary
- **Attack surfaces** grow with complexity, connectivity, and user behavior.
- **Threat vectors** exploit both technical and human vulnerabilities.
- Mitigation requires layered defenses, user education, and continuous monitoring.
## 2.3 Explain various types of vulnerabilities
Vulnerabilities are weaknesses in systems, applications, or configurations that can be exploited to compromise security. Understanding their types helps in prioritizing mitigation and defense strategies.
### 🖥️ Application Vulnerabilities
| Type                  | Description |
|-----------------------|-------------|
| **Memory Injection**  | Injecting malicious code into memory space |
| **Buffer Overflow**   | Writing beyond buffer limits to execute arbitrary code |
| **Race Conditions**   | Exploiting timing flaws in concurrent processes |
| - **TOC (Time-of-Check)** | Check occurs before state changes |
| - **TOU (Time-of-Use)**   | Use occurs after state changes |
| **Malicious Update**  | Compromised or spoofed software updates |
### 🧩 Operating System (OS)-Based Vulnerabilities
- **Description**: Flaws in OS components or services.
- **Examples**: Privilege escalation, kernel exploits, unpatched services.
### 🌐 Web-Based Vulnerabilities
| Type                  | Description |
|-----------------------|-------------|
| **SQL Injection (SQLi)** | Injecting SQL commands via input fields |
| **Cross-Site Scripting (XSS)** | Injecting scripts into web pages viewed by others |
### 🧱 Hardware Vulnerabilities
| Type            | Description |
|-----------------|-------------|
| **Firmware**     | Exploitable code embedded in hardware devices |
| **End-of-Life**  | Unsupported hardware with no security updates |
| **Legacy**       | Old systems incompatible with modern security controls |
### 🧮 Virtualization Vulnerabilities
| Type              | Description |
|-------------------|-------------|
| **VM Escape**      | Attacker breaks out of VM to access host system |
| **Resource Reuse** | Improper isolation allows access to residual data |
### ☁️ Cloud-Specific Vulnerabilities
- **Description**: Risks unique to cloud environments.
- **Examples**: Misconfigured storage buckets, insecure APIs, tenant isolation failures.
### 🔗 Supply Chain Vulnerabilities
| Source             | Description |
|--------------------|-------------|
| **Service Provider** | Third-party services with weak security |
| **Hardware Provider**| Compromised components or firmware |
| **Software Provider**| Vulnerable or malicious code in dependencies |
### 🔐 Cryptographic Vulnerabilities
- **Description**: Weak or broken encryption algorithms, poor key management.
- **Examples**: Deprecated ciphers, short key lengths, flawed implementations.
### ⚙️ Misconfiguration Vulnerabilities
- **Description**: Incorrect settings that expose systems to risk.
- **Examples**: Open ports, default credentials, excessive permissions.
### 📱 Mobile Device Vulnerabilities
| Type          | Description |
|---------------|-------------|
| **Side Loading** | Installing apps from unofficial sources |
| **Jailbreaking** | Removing OS restrictions, increasing exposure |
### 🕳️ Zero-Day Vulnerabilities
- **Description**: Unknown or unpatched flaws actively exploited before discovery.
- **Impact**: High risk due to lack of defenses or fixes.
### 🧠 Summary
- Vulnerabilities span across software, hardware, and human factors.
- Regular patching, secure coding, and configuration audits are essential.
- Threat actors often chain multiple vulnerabilities for deeper compromise.
## 2.4 Given a scenario, analyze indicators of malicious activity
Malicious activity can manifest across systems, networks, applications, and user behavior. Recognizing indicators helps detect, respond to, and mitigate threats effectively.
### 🦠 Malware Attacks
| Type         | Description |
|--------------|-------------|
| **Ransomware** | Encrypts data and demands payment |
| **Trojan**     | Disguised as legitimate software to deliver payloads |
| **Worm**       | Self-replicates across systems without user action |
| **Spyware**    | Secretly monitors user activity |
| **Bloatware**  | Unnecessary software that degrades performance |
| **Virus**      | Infects files and spreads through user actions |
| **Keylogger**  | Records keystrokes to steal credentials |
| **Logic Bomb** | Malicious code triggered by specific conditions |
| **Rootkit**    | Hides malicious processes and grants privileged access |
### 🔐 Physical Attacks
| Type         | Description |
|--------------|-------------|
| **Brute Force** | Repeated attempts to guess credentials |
| **RFID Cloning** | Duplicating access cards or tags |
| **Environmental** | Damage or disruption due to temperature, humidity, or power issues |
### 🌐 Network Attacks
| Type         | Description |
|--------------|-------------|
| **DDoS (Distributed Denial-of-Service)** | Overwhelms systems with traffic |
| - **Amplified** | Uses vulnerable services to multiply traffic |
| - **Reflected** | Spoofs source IP to redirect responses |
| **DNS Attacks** | Poisoning, spoofing, or hijacking DNS queries |
| **Wireless**    | Rogue APs, evil twins, deauthentication attacks |
| **On-Path**     | Intercepts and alters communication between parties |
| **Credential Replay** | Reuses stolen credentials to gain access |
| **Malicious Code** | Injected into network traffic or endpoints |
### 🧩 Application Attacks
| Type               | Description |
|--------------------|-------------|
| **Injection**       | SQL, command, or code injection via input fields |
| **Buffer Overflow** | Overwrites memory to execute arbitrary code |
| **Replay**          | Reuses valid data transmissions for unauthorized access |
| **Privilege Escalation** | Gains higher access than intended |
| **Forgery**         | Fakes requests or data (e.g., CSRF) |
| **Directory Traversal** | Accesses restricted directories via path manipulation |
### 🔐 Cryptographic Attacks
| Type         | Description |
|--------------|-------------|
| **Downgrade** | Forces use of weaker encryption protocols |
| **Collision** | Two inputs produce the same hash output |
| **Birthday**  | Exploits probability of hash collisions in large datasets |
### 🔑 Password Attacks
| Type         | Description |
|--------------|-------------|
| **Spraying**   | Tries common passwords across many accounts |
| **Brute Force**| Tries all possible combinations for one account |
### 🚨 Indicators of Malicious Activity
| Indicator                  | Description |
|----------------------------|-------------|
| **Account Lockout**        | Multiple failed login attempts |
| **Concurrent Session Usage** | Same account used in multiple locations simultaneously |
| **Blocked Content**        | Access to known malicious domains or files |
| **Impossible Travel**      | Logins from geographically distant locations in short time |
| **Resource Consumption**   | Unusual CPU, memory, or bandwidth usage |
| **Resource Inaccessibility** | Services or files suddenly unavailable |
| **Out-of-Cycle Logging**   | Log entries outside normal operational hours |
| **Published/Documented**   | Known indicators from threat intelligence feeds |
| **Missing Logs**           | Gaps in logging may indicate tampering or compromise |
### 🧠 Summary
- **Indicators** are clues, not proof—correlation and context are key.
- **Early detection** relies on monitoring, baselining, and anomaly analysis.
- **Response** should be swift, documented, and aligned with incident handling procedures.
## 2.5 Explain the purpose of mitigation techniques used to secure the enterprise
Mitigation techniques are proactive and reactive measures designed to reduce risk, prevent exploitation, and maintain the confidentiality, integrity, and availability of enterprise systems.
### 🧩 Segmentation
- **Purpose**: Divides the network into isolated zones to limit lateral movement.
- **Benefits**: Contains breaches, improves traffic control, and enhances security posture.
### 🔐 Access Control
| Technique       | Description |
|----------------|-------------|
| **Access Control List (ACL)** | Filters traffic based on IP, port, or protocol |
| **Permissions**              | Defines user or group access to resources (files, systems, apps) |

- **Purpose**: Ensures only authorized users and systems can access sensitive data or services.
### ✅ Application Allow List
- **Purpose**: Permits only approved applications to run on systems.
- **Benefits**: Blocks unauthorized or malicious software execution.
### 🧱 Isolation
- **Purpose**: Separates systems or processes to prevent cross-contamination.
- **Examples**: Sandboxing, virtual machines, quarantined networks.
### 🔧 Patching
- **Purpose**: Fixes known vulnerabilities in software and firmware.
- **Benefits**: Reduces exposure to exploits and zero-day attacks.
### 🔒 Encryption
- **Purpose**: Protects data at rest and in transit from unauthorized access.
- **Benefits**: Ensures confidentiality and compliance with data protection regulations.
### 📈 Monitoring
- **Purpose**: Continuously observes systems and networks for anomalies.
- **Tools**: SIEM, IDS/IPS, log analysis platforms.
- **Benefits**: Enables early detection and rapid response to threats.
### 🧑‍💼 Least Privilege
- **Purpose**: Grants users and systems only the access necessary to perform their tasks.
- **Benefits**: Minimizes potential damage from compromised accounts.
### ⚙️ Configuration Enforcement
- **Purpose**: Ensures systems adhere to security baselines and policies.
- **Tools**: Configuration management systems, compliance scanners.
- **Benefits**: Prevents drift and maintains consistent security posture.
### 🗑️ Decommissioning
- **Purpose**: Securely retires outdated or unused systems.
- **Steps**: Data wiping, hardware destruction, access revocation.
- **Benefits**: Eliminates unnecessary attack surfaces.
### 🛠️ Hardening Techniques
| Technique                        | Description |
|----------------------------------|-------------|
| **Encryption**                   | Secures data and communications |
| **Installation of Endpoint Protection** | Detects and blocks malware |
| **Host-Based Firewall**          | Controls inbound/outbound traffic at the device level |
| **Host-Based Intrusion Prevention System (HIPS)** | Monitors and blocks suspicious activity locally |
| **Disabling Ports/Protocols**    | Reduces exposure by turning off unused services |
| **Default Password Changes**     | Prevents exploitation of known credentials |
| **Removal of Unnecessary Software** | Minimizes attack surface and resource usage |
### 🧠 Summary
- Mitigation techniques work best when layered and tailored to the enterprise environment.
- Regular audits, automation, and user training enhance effectiveness.
- A proactive approach reduces risk and improves resilience against evolving threats.
# 3.0 Security Architecture
## 3.1 Compare and contrast security implications of different architecture models
Different architecture models introduce unique security challenges and benefits. Understanding these implications helps organizations design resilient, scalable, and secure environments.
### ☁️ Cloud Architecture
| Aspect                  | Security Implication |
|-------------------------|----------------------|
| **Responsibility Matrix** | Shared responsibility between provider and customer; misalignment can lead to gaps |
| **Hybrid Considerations** | Complexity increases risk; requires consistent policies across environments |
| **Third-Party Vendors**   | Introduces supply chain risk; requires vendor risk management and contract controls |
### 🧾 Infrastructure as Code (IaC)
- **Security Implication**: Misconfigured templates can propagate vulnerabilities at scale.
- **Benefit**: Enables consistent, auditable deployments with version control.
### 🧠 Serverless Architecture
- **Security Implication**: Limited visibility into runtime; relies heavily on provider security.
- **Benefit**: Reduces attack surface by abstracting infrastructure.
### 🧩 Microservices
- **Security Implication**: Increases complexity; requires secure APIs and inter-service communication.
- **Benefit**: Isolates functionality, improving fault tolerance and scalability.
### 🌐 Network Infrastructure
| Type                     | Security Implication |
|--------------------------|----------------------|
| **Physical Isolation (Air-Gapped)** | Strong protection against external threats; limited usability |
| **Logical Segmentation** | Reduces lateral movement; requires proper configuration |
| **Software-Defined Networking (SDN)** | Centralized control; risk if controller is compromised |
### 🏢 On-Premises
- **Security Implication**: Full control over security; higher responsibility and cost.
- **Benefit**: Customizable and compliant with strict data locality requirements.
### 🧭 Centralized vs. Decentralized
| Model         | Security Implication |
|---------------|----------------------|
| **Centralized** | Easier to manage; single point of failure |
| **Decentralized** | More resilient; harder to secure uniformly |
### 📦 Containerization
- **Security Implication**: Requires isolation and runtime protection; vulnerable to escape and misconfiguration.
- **Benefit**: Lightweight, scalable, and portable.
### 🖥️ Virtualization
- **Security Implication**: VM escape and hypervisor attacks; requires patching and isolation.
- **Benefit**: Efficient resource use and flexible deployment.
### 📡 Internet of Things (IoT)
- **Security Implication**: Often lacks built-in security; vulnerable to botnets and data leaks.
- **Benefit**: Enhances automation and data collection.
### 🏭 ICS / SCADA Systems
- **Security Implication**: Legacy systems with limited patching; critical infrastructure risk.
- **Benefit**: Enables industrial automation and control.
### ⏱️ Real-Time Operating System (RTOS)
- **Security Implication**: Prioritizes timing over security; limited resources for protection.
- **Benefit**: Essential for time-sensitive applications.
### 🔧 Embedded Systems
- **Security Implication**: Hard to patch; often lacks encryption and authentication.
- **Benefit**: Specialized functionality in constrained environments.
### 🛠️ High Availability
- **Security Implication**: Requires redundancy and failover security; complexity can introduce risk.
- **Benefit**: Ensures uptime and resilience against outages.
### 📊 Key Considerations Across Architectures
| Consideration         | Impact on Security |
|-----------------------|--------------------|
| **Availability**       | High availability reduces downtime but requires secure failover mechanisms |
| **Resilience**         | Systems must recover securely from failures or attacks |
| **Cost**               | Budget constraints may limit security investments |
| **Responsiveness**     | Fast systems must balance performance with secure processing |
| **Scalability**        | Growth must not outpace security controls |
| **Ease of Deployment** | Rapid deployment can lead to misconfigurations |
| **Risk Transference**  | Outsourcing shifts risk but requires strong contracts and oversight |
| **Ease of Recovery**   | Backup and restore processes must be secure and tested |
| **Patch Availability** | Timely updates are critical for vulnerability management |
| **Inability to Patch** | Legacy or embedded systems may require compensating controls |
| **Power**              | Power loss can disrupt security systems and logging |
| **Compute**            | Resource constraints may limit encryption and monitoring capabilities |
## 3.2 Given a scenario, apply security principles to secure enterprise infrastructure
Securing enterprise infrastructure requires strategic placement of devices, segmentation of networks, and implementation of layered controls to reduce risk and maintain operational integrity.
### 🏗️ Infrastructure Considerations
| Element            | Description |
|--------------------|-------------|
| **Device Placement** | Positioning devices to optimize performance and security (e.g., DMZ for public-facing servers) |
| **Security Zones**   | Segregating networks by trust level (e.g., internal, external, DMZ) |
| **Attack Surface**   | Minimizing exposed services, ports, and interfaces |
| **Connectivity**     | Ensuring secure and controlled communication between zones |
| **Failure Modes**    | Behavior of systems during failure |
| - **Fail-Open**      | Continues operation without restriction (less secure) |
| - **Fail-Closed**    | Shuts down access to prevent compromise (more secure) |
### ⚙️ Device Attributes
| Attribute         | Description |
|-------------------|-------------|
| **Active**         | Actively processes and filters traffic (e.g., firewall) |
| **Passive**        | Monitors traffic without altering flow (e.g., IDS) |
| **Inline**         | Positioned directly in traffic path; can block threats |
| **Tap/Monitor**    | Observes traffic via mirrored ports or taps; used for analysis |
### 🧱 Network Appliances
| Appliance         | Purpose |
|-------------------|---------|
| **Jump Server**    | Secure intermediary for accessing sensitive systems |
| **Proxy Server**   | Mediates requests between clients and external servers |
| **IPS/IDS**        | Detects and/or blocks malicious traffic |
| **Load Balancer**  | Distributes traffic across multiple servers for availability |
| **Sensors**        | Collects data for monitoring and threat detection |
### 🔌 Port Security
| Protocol          | Description |
|-------------------|-------------|
| **802.1X**         | Port-based network access control using authentication |
| **EAP (Extensible Authentication Protocol)** | Framework for various authentication methods over 802.1X |
### 🔥 Firewall Types
| Type                      | Description |
|---------------------------|-------------|
| **Web Application Firewall (WAF)** | Protects web apps from attacks like XSS and SQLi |
| **Unified Threat Management (UTM)** | Combines multiple security functions (e.g., firewall, antivirus, VPN) |
| **Next-Generation Firewall (NGFW)** | Deep packet inspection, application awareness, and threat intelligence |
| **Layer 4/Layer 7**        | Filters traffic based on transport (L4) or application (L7) layers |
### 🔐 Secure Communication and Access
| Method                    | Description |
|---------------------------|-------------|
| **VPN (Virtual Private Network)** | Encrypts traffic between remote users and internal network |
| **Remote Access**         | Secure connection for offsite users |
| **Tunneling Protocols**   | Encapsulates data for secure transmission |
| - **TLS (Transport Layer Security)** | Encrypts application-level traffic (e.g., HTTPS) |
| - **IPSec (Internet Protocol Security)** | Encrypts network-level traffic |
| **SD-WAN (Software-Defined WAN)** | Secure, flexible WAN routing with centralized control |
| **SASE (Secure Access Service Edge)** | Combines networking and security functions in the cloud |
### ✅ Selection of Effective Controls
| Principle                | Application |
|--------------------------|-------------|
| **Least Privilege**       | Restrict access to only what's necessary |
| **Defense in Depth**      | Layered controls across endpoints, networks, and applications |
| **Segmentation**          | Isolate sensitive systems to limit exposure |
| **Monitoring and Logging**| Enable visibility and forensic capabilities |
| **Patch Management**      | Regular updates to fix vulnerabilities |
| **Encryption**            | Protect data in transit and at rest |
| **Access Control**        | Enforce identity verification and role-based permissions |
### 🧠 Summary
- Security must be embedded at every layer—from physical placement to cloud access.
- Effective controls are context-dependent and should align with business needs and risk tolerance.
- Continuous monitoring, adaptive policies, and secure design principles are key to resilient infrastructure.
## 3.3 Compare and contrast concepts and strategies to protect data
Protecting data requires understanding its type, classification, state, and applying appropriate security controls. These strategies help ensure confidentiality, integrity, and availability while meeting legal and business requirements.
### 📂 Data Types
| Type                  | Description | Protection Needs |
|-----------------------|-------------|------------------|
| **Regulated**         | Governed by laws (e.g., HIPAA, GDPR) | High compliance and encryption |
| **Trade Secret**      | Proprietary business knowledge | Strong access control and monitoring |
| **Intellectual Property** | Patents, designs, source code | Legal protection and secure storage |
| **Legal Information** | Contracts, case files | Confidentiality and integrity |
| **Financial Information** | Banking, payroll, transactions | Encryption and fraud detection |
| **Human-Readable**    | Easily interpreted by users (e.g., text, reports) | Masking and access control |
| **Non-Human-Readable**| Machine data (e.g., logs, binaries) | Integrity and secure parsing |
### 🏷️ Data Classifications
| Classification | Description | Example |
|----------------|-------------|---------|
| **Sensitive**   | Could cause harm if exposed | PII, credentials |
| **Confidential**| Internal use only | Business plans |
| **Public**      | No harm if disclosed | Marketing materials |
| **Restricted**  | Limited access due to risk | Source code |
| **Private**     | Personal or internal data | Employee records |
| **Critical**    | Essential to operations | Financial systems, backups |
### 📊 General Data Considerations
#### 📌 Data States
| State           | Description | Protection Strategy |
|-----------------|-------------|---------------------|
| **Data at Rest** | Stored data (e.g., databases, files) | Full-disk encryption, access control |
| **Data in Transit** | Moving across networks | TLS, VPN, IPSec |
| **Data in Use** | Actively processed by applications | Memory protection, secure coding |
#### 🌍 Data Sovereignty & Geolocation
- **Data Sovereignty**: Data must comply with laws of the country where it's stored.
- **Geolocation**: Physical location affects latency, compliance, and risk exposure.
### 🛠️ Methods to Secure Data
| Method               | Description |
|----------------------|-------------|
| **Geographic Restrictions** | Limits access based on location to enforce compliance |
| **Encryption**            | Converts data into unreadable format without a key |
| **Hashing**               | One-way transformation for integrity checks |
| **Masking**               | Obscures data for testing or display |
| **Tokenization**          | Replaces sensitive data with non-sensitive tokens |
| **Obfuscation**           | Makes data harder to interpret (e.g., code obfuscation) |
| **Segmentation**          | Isolates data by type or sensitivity level |
| **Permission Restrictions** | Limits access based on roles and policies |
### 🧠 Summary
- **Data protection** must align with its classification, type, and state.
- **Layered strategies** such as encryption, access control, and segmentation enhance security.
- **Compliance** with legal and geographic requirements is essential for regulated data.
- **Visibility and control** over data flow and access are key to preventing breaches.
## 3.4 Explain the importance of resilience and recovery in security architecture
Resilience and recovery ensure that systems can withstand disruptions and restore operations quickly. These principles are essential for maintaining business continuity, minimizing downtime, and protecting data integrity.
### ⚙️ High Availability
| Strategy         | Description | Benefit |
|------------------|-------------|---------|
| **Load Balancing** | Distributes traffic across multiple servers | Improves performance and fault tolerance |
| **Clustering**     | Links servers to act as a single system | Enhances redundancy and failover capability |
### 🏢 Site Considerations
| Site Type     | Description | Recovery Speed | Cost |
|---------------|-------------|----------------|------|
| **Hot Site**   | Fully operational replica | Fast | High |
| **Warm Site**  | Partially configured with some data | Moderate | Medium |
| **Cold Site**  | Basic infrastructure only | Slow | Low |
| **Geographic Dispersion** | Sites located in different regions | Protects against regional disasters | Variable |
### 🧬 Platform Diversity
- **Description**: Using varied operating systems, hardware, and software.
- **Benefit**: Reduces risk of single point of failure or platform-specific vulnerabilities.
### ☁️ Multi-Cloud Systems
- **Description**: Leveraging multiple cloud providers.
- **Benefit**: Enhances redundancy, avoids vendor lock-in, and improves availability.
### 🔄 Continuity of Operations
- **Purpose**: Ensures critical functions continue during and after a disruption.
- **Includes**: Alternate work sites, emergency communication plans, and prioritized recovery.
### 📊 Capacity Planning
| Resource     | Consideration |
|--------------|---------------|
| **People**    | Staffing for recovery and support roles |
| **Technology**| Sufficient hardware/software to handle failover |
| **Infrastructure** | Network, power, and physical space to support operations |
### 🧪 Testing Strategies
| Method              | Description |
|---------------------|-------------|
| **Tabletop Exercises** | Simulated discussions to walk through scenarios |
| **Failover Testing**   | Validates automatic switch to backup systems |
| **Simulation**         | Mimics real-world disaster conditions |
| **Parallel Processing**| Runs backup systems alongside production for comparison |
### 💾 Backup Strategies
| Element         | Description |
|-----------------|-------------|
| **Onsite/Offsite** | Local vs. remote storage for redundancy |
| **Frequency**       | Determines recovery point objective (RPO) |
| **Encryption**      | Secures backup data from unauthorized access |
| **Snapshots**       | Point-in-time copies of systems or data |
| **Recovery**        | Ability to restore systems and data |
| **Replication**     | Real-time or scheduled duplication of data |
| **Journaling**      | Logs changes for granular recovery and auditing |
### ⚡ Power Resilience
| Component                  | Description |
|----------------------------|-------------|
| **Generators**             | Backup power for extended outages |
| **Uninterruptible Power Supply (UPS)** | Immediate power during short-term outages or transitions |
### 🧠 Summary
- **Resilience** ensures systems stay operational under stress.
- **Recovery** enables rapid restoration of services and data.
- **Testing and planning** are critical to validate readiness and reduce impact.
- **Layered strategies** across infrastructure, cloud, and personnel provide robust protection.
