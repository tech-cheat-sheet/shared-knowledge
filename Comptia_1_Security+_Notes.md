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
