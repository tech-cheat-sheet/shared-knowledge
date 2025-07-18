- [CompTIA CySA+ Exam CSO-003](#comptia-cysa-exam-cso-003)
- [1.0 Security Operations](#10-security-operations)
  - [1.1 Explain the importance of system and network architecture concepts in security operations](#11-explain-the-importance-of-system-and-network-architecture-concepts-in-security-operations)
    - [🧾 Log Ingestion and Time Integrity](#-log-ingestion-and-time-integrity)
    - [🖥️ Operating System (OS) Concepts](#️-operating-system-os-concepts)
    - [🏗️ Infrastructure Concepts](#️-infrastructure-concepts)
    - [🌐 Network Architecture](#-network-architecture)
    - [🔐 Identity and Access Management (IAM)](#-identity-and-access-management-iam)
    - [🔐 Encryption and Secure Communications](#-encryption-and-secure-communications)
    - [🛡️ Sensitive Data Protection](#️-sensitive-data-protection)
    - [🧠 Summary](#-summary)
  - [1.2 Given a scenario, analyze indicators of potentially malicious activity](#12-given-a-scenario-analyze-indicators-of-potentially-malicious-activity)
    - [🌐 Network-Related Indicators](#-network-related-indicators)
    - [💻 Host-Related Indicators](#-host-related-indicators)
    - [🧩 Application-Related Indicators](#-application-related-indicators)
    - [🧠 Other Indicators](#-other-indicators)
    - [🧠 Summary](#-summary-1)
# CompTIA CySA+ Exam CSO-003
# 1.0 Security Operations
## 1.1 Explain the importance of system and network architecture concepts in security operations
Well-architected systems and networks form the backbone of effective security operations. Their configurations, interactions, and monitoring mechanisms directly impact threat detection, prevention, and response capabilities.
### 🧾 Log Ingestion and Time Integrity
| Element            | Importance |
|--------------------|------------|
| **Time Synchronization** | Ensures accurate timestamping across logs, enabling precise incident correlation |
| **Logging Levels**        | Controls the verbosity of logs to balance performance and detail; critical for filtering noise during analysis |
### 🖥️ Operating System (OS) Concepts
| Concept                 | Security Relevance |
|-------------------------|--------------------|
| **Windows Registry**     | Centralized database for OS settings; a target for malware and key auditing spot |
| **System Hardening**     | Reduces attack surface by disabling unnecessary services and applying security configurations |
| **File Structure**       | Helps identify unusual file placement or tampering |
| - **Configuration Files**| Stores system/application settings; monitoring changes is critical for integrity |
| **System Processes**     | Abnormal or rogue processes may indicate malware or compromise |
| **Hardware Architecture**| Impacts vulnerability profiles, firmware trust, and system isolation capabilities (e.g., TPM chips, UEFI vs. BIOS) |
### 🏗️ Infrastructure Concepts
| Model             | Impact on Security Operations |
|-------------------|-------------------------------|
| **Serverless**     | Abstracts the infrastructure but requires strict IAM and API security |
| **Virtualization** | Enables segmentation, sandboxing, and isolation; requires hypervisor security |
| **Containerization**| Accelerates deployment but needs image scanning and runtime monitoring |
### 🌐 Network Architecture
| Architecture Type       | Description |
|--------------------------|-------------|
| **On-Premises**           | Full control; physical security and internal patch management required |
| **Cloud**                 | Shared responsibility model; identity and data-centric controls vital |
| **Hybrid**                | Blends flexibility and complexity; unified visibility is essential |
| **Network Segmentation** | Limits lateral movement and contains breaches within subnet boundaries |
| **Zero Trust**           | “Never trust, always verify”; enforces strict access policies and microsegmentation |
| **SASE** (Secure Access Service Edge) | Merges networking and security functions in the cloud; centralizes control |
| **SDN** (Software-Defined Networking) | Dynamic network provisioning; allows real-time control and policy enforcement |
### 🔐 Identity and Access Management (IAM)
| Technique/Tool        | Purpose |
|------------------------|--------|
| **Multifactor Authentication (MFA)** | Adds additional verification layers to prevent unauthorized access |
| **Single Sign-On (SSO)**             | Reduces password fatigue and centralizes control |
| **Federation**                       | Enables trusted identity sharing across organizations |
| **Privileged Access Management (PAM)** | Secures administrative accounts and logs elevated actions |
| **Passwordless**                     | Enhances user experience and mitigates credential theft |
| **CASB (Cloud Access Security Broker)** | Monitors and enforces security policies for cloud apps and services |
### 🔐 Encryption and Secure Communications
| Feature                  | Function |
|--------------------------|----------|
| **Public Key Infrastructure (PKI)** | Enables trust via digital certificates and asymmetric encryption |
| **SSL/TLS Inspection**              | Decrypts and inspects secure traffic to detect hidden threats |
### 🛡️ Sensitive Data Protection
| Methodology              | Significance |
|--------------------------|--------------|
| **Data Loss Prevention (DLP)** | Prevents unauthorized data exfiltration and enforces protection rules |
| **PII (Personally Identifiable Information)** | Must be safeguarded against identity theft and privacy violations |
| **CHD (Cardholder Data)**      | Governed by PCI-DSS; requires encryption, limited access, and secure storage |
### 🧠 Summary
- Security operations rely on **architecture awareness** to ensure visibility, containment, and resilience.
- From **logs to identity**, each layer introduces controls and risks.
- Strategic architecture choices—like **Zero Trust** and **SDN**—enable scalable, policy-driven security.
- Proper integration of OS, infrastructure, and network elements is essential for robust threat defense.
## 1.2 Given a scenario, analyze indicators of potentially malicious activity
Recognizing suspicious patterns is critical for detecting cyberattacks early. These indicators help analysts triage alerts, initiate investigation, and coordinate response actions.
### 🌐 Network-Related Indicators
| Indicator                    | Significance |
|------------------------------|--------------|
| **Bandwidth Consumption**     | Excessive usage may signal data exfiltration or DoS attempts |
| **Beaconing**                 | Periodic traffic to external IPs may indicate C2 (Command & Control) behavior |
| **Irregular Peer-to-Peer Communication** | Can be used to bypass centralized monitoring and spread malware |
| **Rogue Devices on Network**  | Unauthenticated endpoints pose serious risk to network hygiene |
| **Scans/Sweeps**              | Repeated probing can signify reconnaissance or vulnerability scanning |
| **Unusual Traffic Spikes**    | May align with botnet activation, ransomware deployment, or service abuse |
| **Activity on Unexpected Ports** | Indicative of protocol tunneling, port hijacking, or policy violations |
### 💻 Host-Related Indicators
| Indicator                    | Significance |
|------------------------------|--------------|
| **Processor Consumption**     | Unusual CPU spikes may result from mining software or malware execution |
| **Memory Consumption**        | Memory leaks or spikes may accompany malicious processes |
| **Drive Capacity Consumption**| Full storage can hide logs or result from data staging for exfiltration |
| **Unauthorized Software**     | Unapproved apps could be remote tools or malicious payloads |
| **Malicious Processes**       | Unknown or obfuscated processes often operate in background silently |
| **Unauthorized Changes**      | Config tampering may reduce system security or enable persistence |
| **Unauthorized Privileges**   | Privilege escalation attempts for lateral movement or control |
| **Data Exfiltration**         | Evidence of outgoing sensitive data beyond expected patterns |
| **Abnormal OS Process Behavior** | E.g., `svchost.exe` spawning unexpected network connections |
| **File System Changes**       | New or modified files (especially executables or scripts) may signal compromise |
| **Registry Anomalies**        | Registry manipulation can embed persistence mechanisms or disable security tools |
| **Unauthorized Scheduled Tasks** | Can enable time-triggered malicious activity (e.g., script execution) |
### 🧩 Application-Related Indicators
| Indicator                    | Description |
|------------------------------|-------------|
| **Anomalous Activity**        | E.g., excessive logins, API misuse, account hopping |
| **Introduction of New Accounts** | May indicate an attacker creating persistence pathways |
| **Unexpected Output**         | Apps generating corrupted files, strange logs, or unexpected errors |
| **Unexpected Outbound Communication** | Applications transmitting data to unknown or foreign hosts |
| **Service Interruption**      | May result from targeted DoS or internal sabotage |
| **Application Logs**          | Reveal unauthorized access, errors, or behavior anomalies during compromise |
### 🧠 Other Indicators
| Indicator                    | Analysis |
|------------------------------|----------|
| **Social Engineering Attacks** | Phishing, pretexting, baiting — often precursors to deeper system infiltration |
| **Obfuscated Links**           | Masked URLs may redirect users to malicious payloads or phishing sites |
### 🧠 Summary
Early detection of malicious activity requires attention to:
- Behavioral anomalies across endpoints and network flows
- Discrepancies between expected and observed resource usage
- Logging inconsistencies and unexplained configurations

Analysts should **correlate multiple indicators**, apply **contextual intelligence**, and prioritize according to **risk and impact**.
