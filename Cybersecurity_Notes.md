- [Information Security](#information-security)
  - [Principles of Security = Security Concepts + Security Controls](#principles-of-security--security-concepts--security-controls)
    - [Security Concepts = CIA + AAA](#security-concepts--cia--aaa)
    - [Security Controls](#security-controls)
      - [Security Control Categories](#security-control-categories)
      - [Security Control Types](#security-control-types)
- [Popular Security Flaws](#popular-security-flaws)
- [Threat Actor vs Threat Vector](#threat-actor-vs-threat-vector)
- [Threat Vector vs Attack Surface](#threat-vector-vs-attack-surface)
- [Attack Surfaces by Category](#attack-surfaces-by-category)
- [Vulnerability Type vs Threat Vector](#vulnerability-type-vs-threat-vector)
  - [🔍 Real-World Analogy](#-real-world-analogy)
  - [🧩 How They Interact](#-how-they-interact)
- [MITRE ATT\&CK® framework](#mitre-attck-framework)
  - [🔍 What does ATT\&CK stand for?](#-what-does-attck-stand-for)
  - [🧠 Key Features of MITRE ATT\&CK:](#-key-features-of-mitre-attck)
  - [📊 Structure of the Framework:](#-structure-of-the-framework)
- [Cybersecurity Frameworks](#cybersecurity-frameworks)
  - [Comparison Table: MITRE ATT\&CK vs OWASP vs CWE vs NIST vs ISO/IEC 27001](#comparison-table-mitre-attck-vs-owasp-vs-cwe-vs-nist-vs-isoiec-27001)
    - [🧠 Summary](#-summary)
  - [MITRE ATT\&CK® framework](#mitre-attck-framework-1)
  - [🧩 Lockheed Martin Cyber Kill Chain](#-lockheed-martin-cyber-kill-chain)
  - [💎 Diamond Model of Intrusion Analysis](#-diamond-model-of-intrusion-analysis)
  - [📚 NIST Cybersecurity Framework (CSF)](#-nist-cybersecurity-framework-csf)
  - [🧠 CAPEC (Common Attack Pattern Enumeration and Classification)](#-capec-common-attack-pattern-enumeration-and-classification)
  - [🔐 STRIDE Threat Modeling](#-stride-threat-modeling)
  - [🧪 Unified Kill Chain](#-unified-kill-chain)
  - [🛠️ PASTA, DREAD, and OCTAVE](#️-pasta-dread-and-octave)
- [🏆 Most Widely Recognized Frameworks](#-most-widely-recognized-frameworks)
  - [🧠 Why These Stand Out](#-why-these-stand-out)
- [IDS vs IPS vs EDR vs XDR](#ids-vs-ips-vs-edr-vs-xdr)
  - [🧠 Quick Summary](#-quick-summary)
- [SOC vs Vulnerability Management vs Threat Intelligence](#soc-vs-vulnerability-management-vs-threat-intelligence)
  - [🛡️ SOC vs Vulnerability Management vs Threat Intelligence](#️-soc-vs-vulnerability-management-vs-threat-intelligence)
  - [🧠 Quick Insight](#-quick-insight)
  - [🧠 Why Threat Intelligence Matters in Vulnerability Management](#-why-threat-intelligence-matters-in-vulnerability-management)
  - [🔍 How the Big Three Integrate Threat Intelligence](#-how-the-big-three-integrate-threat-intelligence)
  - [📊 What This Means for You](#-what-this-means-for-you)
- [Physical Security Controls](#physical-security-controls)
- [Data Controls](#data-controls)
  - [Data Classifications](#data-classifications)
  - [Types of Data](#types-of-data)
  - [States of Data](#states-of-data)
- [Types of Authentication Credentials](#types-of-authentication-credentials)
# Information Security
## Principles of Security = Security Concepts + Security Controls
### Security Concepts = CIA + AAA
- **Confidentiality** ensures that only authorized parties can
view the information.
- **Integrity** ensures that the information is correct and no unauthorized person or malicious software has altered the data.
- **Availability** ensures that data is accessible to only authorized users and not to unapproved individuals.
- **Authentication** Checking the delivery person’s credentials to be sure that they are authentic and not fabricated.
- **Authorization** granting permission to take an action. Computer users are granted access only to the specific services, devices,applications, and files needed to perform their job duties.
- **Accounting** creates a record that is preserved of who accessed the enterprise network, what resources they accessed, and when they disconnected from the network.
### Security Controls
A security control is a safeguard (sometimes called a countermeasure) that is employed within an enterprise to protect
the CIA of information. A control attempts to limit the exposure of an asset to a danger.
#### Security Control Categories
| **Action**        | **Description**                    | **Scenario Example**                            | **Computer Process**                    |
|-------------------|------------------------------------|--------------------------------------------------|------------------------------------------|
| Identification    | Review of credentials              | Delivery person shows employee badge            | User enters username                     |
| Authentication    | Validate credentials as genuine    | Gabe reads badge to confirm it is real          | User provides password                   |
| Authorization     | Permission granted for admittance  | Gabe opens door to allow delivery person in     | User allowed to access specific data     |
| Accounting        | Record of user actions             | Gabe signs to confirm package pickup            | Information recorded in log file         |
#### Security Control Types
| Control Category | Description                                         | Example                                                                      |
|------------------|-----------------------------------------------------|------------------------------------------------------------------------------|
| Managerial       | Controls using administrative methods               | Acceptable use policy restricting access to malicious websites              |
| Operational      | Controls implemented and executed by individuals    | Training workshops teaching users to identify and delete suspicious emails  |
| Technical        | Controls embedded in hardware, software, or firmware| Devices that block malicious content from entering the network              |
| Physical         | Controls enforcing security through physical means  | Installing a fence to prevent unauthorized building access                   |


| Control Type          | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| Deterrent controls     | Attempt to discourage security violations before they occur                 |
| Preventive controls    | Work to block threats from interacting with vulnerabilities                 |
| Detective controls     | Identify threats that have already reached the system                       |
| Compensating controls  | Provide alternative protections when standard controls can't be used       |
| Corrective controls    | Lessen damage and help recover after an incident                            |
| Directive controls     | Ensure specific outcomes are achieved through policy or guidance            |

| Control Type         | Description                         | When It Occurs   | Example                                                        |
|----------------------|-------------------------------------|------------------|----------------------------------------------------------------|
| Deterrent Control     | Discourages potential attacks       | Before attack     | Signs indicating area is under video surveillance              |
| Preventive Control    | Prevents threat exploitation        | Before attack     | Security awareness training for users                          |
| Directive Control     | Guides desired behavior             | Before attack     | Incentives for completing a training course                    |
| Detective Control     | Identifies an active attack         | During attack     | Motion detection sensors                                       |
| Compensating Control  | Alternative safeguards during attack| During attack     | Isolating an infected computer on a separate network           |
| Corrective Control    | Reduces damage and recovers systems| After attack      | Cleaning a virus from an infected server                       |

# Popular Security Flaws
| Vulnerability Type           | Description                                                        | Example                                                   | CVSS Score Range          |
|------------------------------|--------------------------------------------------------------------|------------------------------------------------------------|---------------------------|
| Remote Code Execution (RCE)  | Allows attackers to run arbitrary code remotely                    | Exploiting a buffer overflow in a web server              | 9.0–10.0 (Critical)       |
| Broken Access Control        | Users bypass access restrictions                                   | Accessing admin functions without authorization           | 7.0–9.5 (High–Critical)   |
| Unpatched Software           | Known flaws exploitable due to missing updates                     | Running vulnerable Apache Struts (e.g., CVE-2017-5638)    | 7.0–9.8 (High–Critical)   |
| Injection Attacks            | Malicious input alters backend behavior                            | SQL injection in a login form                             | 7.5–9.8 (High–Critical)   |
| Misconfigured Cloud Services | Incorrect settings expose sensitive data                           | Public AWS S3 bucket leaking customer data                | 6.0–8.5 (Medium–High)     |
| Cross-Site Scripting (XSS)   | Injected scripts executed in browsers                              | Reflected XSS in search results                           | 6.1–8.8 (Medium–High)     |
| Insecure Authentication      | Weak or flawed login mechanisms                                    | Passwords stored in plaintext                             | 6.0–8.0 (Medium–High)     |
| Default Credentials          | Systems shipped with known default logins                          | Router using admin/admin                                  | 5.0–7.5 (Medium–High)     |
| Missing MFA                  | No second factor of authentication                                 | Single-factor login to sensitive dashboard                | 4.0–6.5 (Medium)          |
| Cross-Site Request Forgery   | Tricking users into unwanted actions                               | Changing account email via forged request                 | 5.0–7.0 (Medium–High)     |
| Insecure Deserialization     | Untrusted data leads to code execution or logic flaws              | Java app deserializing attacker-controlled object         | 8.0–9.8 (High–Critical)   |
# Threat Actor vs Threat Vector
| Aspect             | Threat Actor                                | Threat Vector                                    |
|--------------------|---------------------------------------------|--------------------------------------------------|
| **Definition**     | Entity responsible for initiating a threat  | Path or method used to carry out the threat      |
| **Role**           | The attacker or malicious source            | The technique or channel exploited               |
| **Examples**       | Hackers, nation-states, insiders, malware   | Phishing emails, USB drives, open ports          |
| **Intent**         | Often intentional (malicious), sometimes accidental | Passive channel for delivering threats      |
| **Focus**          | Who is behind the attack                    | How the attack reaches the target                |
| **Security Usage** | Helps identify motives and capabilities     | Helps map out points of vulnerability            |
# Threat Vector vs Attack Surface
| Aspect              | Threat Vector                                       | Attack Surface                                          |
|---------------------|----------------------------------------------------|---------------------------------------------------------|
| **Definition**       | Method or pathway used to exploit a vulnerability | Total number of potential entry points or vulnerabilities |
| **Focus**            | How an attack is carried out                      | Where an attack could occur                            |
| **Scope**            | Specific and targeted                             | Broad and comprehensive                                |
| **Examples**         | Phishing, malware, SQL injection, social engineering | Open ports, outdated software, misconfigured systems, exposed APIs |
| **Nature**           | Dynamic and constantly evolving                   | Relatively stable but can grow with system changes     |
| **Measurement**      | Frequency and effectiveness of attack methods     | Number and severity of vulnerabilities                 |
| **Mitigation Strategy** | Block or neutralize specific methods           | Harden systems and minimize exposure                   |
| **Detection Approach** | Reactive—respond to active threats              | Proactive—identify and secure potential vulnerabilities |
| **Impact**           | Depends on success of attack method               | Larger surface increases chance of exploitation        |
| **Analogy**          | The weapon used in a burglary                     | All the doors and windows that could be used to break in |

🧠 Think of it this way: the attack surface is the playground, and threat vectors are the ways attackers play dirty on it.
Want to explore how to reduce your attack surface or defend against common threat vectors?
# Attack Surfaces by Category
| **Category** | **Attack Surface**             | **Explanation**                                                                 |
|--------------|-------------------------------|----------------------------------------------------------------------------------|
| Software     | Vulnerable software           | Contains security flaws exploitable by attackers; includes both client and agentless software |
| Software     | File-based                    | Individual files targeted for infection or compromise                           |
| Software     | Image-based                   | Entire system images can be vulnerable and subject to exploitation               |
| Hardware     | Unsupported systems & apps    | No longer updated or monitored, increasing exposure to threats                   |
| Hardware     | Removable devices             | USBs or external drives can introduce malware between systems                    |
| Network      | Unsecure networks             | Weak wired or wireless networks provide broad access to connected devices        |
| Network      | Open service ports            | Enabled but unused ports may become access points for attackers                  |
| Network      | Default credentials           | Preconfigured admin accounts with known passwords can be exploited               |

# Vulnerability Type vs Threat Vector
| Aspect               | Threat Vector                                           | Vulnerability Type                                      |
|----------------------|--------------------------------------------------------|----------------------------------------------------------|
| **Definition**        | The pathway or method used to exploit a system         | A weakness or flaw in a system that can be exploited     |
| **Role in Attack**    | Describes how an attack is delivered                   | Describes what is being exploited                        |
| **Focus**             | Attack delivery mechanism                              | System or software weakness                              |
| **Examples**          | Phishing, malware, social engineering, open ports      | Buffer overflow, SQL injection, misconfigurations        |
| **Dynamic vs Static** | Dynamic — changes with attacker tactics                | Static — exists until patched or mitigated               |
| **Mitigation**        | Block or monitor attack paths                          | Patch or fix the underlying flaw                         |
## 🔍 Real-World Analogy
- Threat Vector: Like a burglar choosing a window to break in.
- Vulnerability Type: The fact that the window was left unlocked.
## 🧩 How They Interact
- A threat vector exploits a vulnerability type. For example:
- A phishing email (threat vector) may exploit insecure authentication (vulnerability type).
- A malicious website (threat vector) may exploit a cross-site scripting flaw (vulnerability type).
# MITRE ATT&CK® framework
a globally accessible knowledge base that catalogs the tactics, techniques, and procedures (TTPs) used by cyber adversaries based on real-world observations2.
## 🔍 What does ATT&CK stand for?
- Adversarial
- Tactics
- Techniques
- &
- Common
- Knowledge
## 🧠 Key Features of MITRE ATT&CK:
- Models attacker behavior from the attacker’s perspective, not the defender’s
- Helps organizations detect, prevent, and respond to cyber threats
- Continuously updated with input from cybersecurity professionals worldwide
- Used by security teams, threat hunters, red teams, and penetration testers
## 📊 Structure of the Framework: 
MITRE ATT&CK is organized into matrices for different environments:
| Matrix     | Focus Area                                                       |
|------------|------------------------------------------------------------------|
| Enterprise | Windows, macOS, Linux, cloud, containers, and network infrastructure |
| Mobile     | Android and iOS                                                  |
| ICS        | Industrial Control Systems (e.g., utilities, factories)          |

Each matrix includes:
- Tactics: The attacker’s goals (e.g., Initial Access, Persistence, Exfiltration)
- Techniques: How those goals are achieved (e.g., Phishing, Credential Dumping)
- Sub-techniques: More granular methods within a technique

💡 Why it matters: MITRE ATT&CK helps organizations understand how attackers operate, simulate attacks, and strengthen defenses. It’s like a playbook of how cyber adversaries think and act.

# Cybersecurity Frameworks
## Comparison Table: MITRE ATT&CK vs OWASP vs CWE vs NIST vs ISO/IEC 27001

| Feature / Focus Area                | MITRE ATT&CK                            | OWASP Top Ten                            | CWE (Common Weakness Enumeration)       | NIST Cybersecurity Framework            | ISO/IEC 27001                          |
|------------------------------------|-----------------------------------------|------------------------------------------|-----------------------------------------|-----------------------------------------|----------------------------------------|
| 🔍 Primary Focus                   | Adversary behavior & attack techniques  | Web application security risks           | Software and hardware weaknesses        | Cyber risk management & resilience      | Information security management system |
| 🎯 Scope                           | Threat actor tactics, techniques & procedures | Web app vulnerabilities & misconfigurations | Broad software flaws across platforms   | Identify, protect, detect, respond, recover | Organizational security controls       |
| 🧠 Use Case                        | Threat modeling, detection, red teaming | Developer awareness, secure coding       | Vulnerability classification & mapping  | Strategic planning, compliance, resilience | Certification, audit, governance       |
| 🧩 Structure                       | Tactics → Techniques → Sub-techniques   | 10 categories of common risks            | Hierarchical: Pillars → Classes → Bases | Core Functions → Implementation Tiers → Profiles | Clauses → Controls → Annex A           |
| 🛠️ Examples                       | T1210: Exploitation of Remote Services  | A01: Broken Access Control               | CWE-94: Code Injection, CWE-502: Deserialization | PR.AC: Access Control, DE.CM: Monitoring | A.9: Access Control, A.12: Operations Security |
| 🔗 Relationship to CVEs            | Maps techniques to real-world exploits  | Maps categories to CWEs                  | Directly referenced in CVEs             | Indirect — supports risk-based CVE response | Indirect — supports control-based CVE mitigation |
| 🧪 Detection & Mitigation Guidance | Yes — includes data sources & procedures | Yes — includes prevention recommendations | Yes — includes mitigation strategies    | Yes — includes best practices & maturity tiers | Yes — includes control objectives       |
| 🧭 Ideal Audience                  | SOC teams, threat hunters, red teams    | Developers, app security teams           | Developers, security analysts           | CISOs, risk managers, compliance teams   | Executives, auditors, IT governance     |
| 🧠 Maintained By                   | MITRE                                   | OWASP                                    | MITRE                                   | NIST (U.S. government)                   | ISO (International Organization for Standardization) |

### 🧠 Summary
- MITRE ATT&CK: Tactical lens on attacker behavior.
- OWASP Top Ten: Developer-focused web app risks.
- CWE: Granular catalog of software weaknesses.
- NIST CSF: Strategic framework for cyber resilience.
- ISO/IEC 27001: Global standard for security governance and certification.
## MITRE ATT&CK® framework
## 🧩 Lockheed Martin Cyber Kill Chain
- Breaks down cyberattacks into seven linear stages: Reconnaissance, Weaponization, Delivery, Exploitation, Installation, Command & Control, and Actions on Objectives
- Focuses on early detection and prevention
- Best for training and understanding attack progression
- Limitation: Less effective for post-compromise detection and modern, multi-vector attacks
## 💎 Diamond Model of Intrusion Analysis
- Emphasizes four core components: Adversary, Infrastructure, Capability, and Victim
- Useful for threat attribution and understanding attacker motivations
- Often used in threat intelligence and APT analysis
- Can be combined with MITRE ATT&CK for deeper insights
## 📚 NIST Cybersecurity Framework (CSF)
- Structured around five core functions: Identify, Protect, Detect, Respond, Recover
- Focuses on risk management and governance
- Widely adopted across industries for compliance and strategic planning
- Less tactical than ATT&CK; more about policy and process alignment
## 🧠 CAPEC (Common Attack Pattern Enumeration and Classification)
- Catalogs known attack patterns, especially for application-level threats
- Often paired with CWE (Common Weakness Enumeration)
- Ideal for secure software development and penetration testing
- Less suited for real-time threat detection
## 🔐 STRIDE Threat Modeling
- Developed by Microsoft; focuses on six threat categories: Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege
- Great for design-phase threat modeling
- Often used in secure architecture reviews
- Can be mapped to ATT&CK for more granular analysis
## 🧪 Unified Kill Chain
- Combines elements of Cyber Kill Chain and MITRE ATT&CK
- Offers a more holistic view of attacker behavior across multiple campaigns
- Useful for advanced threat hunting and defense-in-depth strategies
## 🛠️ PASTA, DREAD, and OCTAVE
- These are risk-centric threat modeling frameworks
- Focus on impact analysis, likelihood scoring, and business risk
- Often used in enterprise risk assessments and DevSecOps pipelines
# 🏆 Most Widely Recognized Frameworks
| Framework                     | Recognition & Use                                                                 |
|-------------------------------|-----------------------------------------------------------------------------------|
| NIST Cybersecurity Framework  | Adopted across industries worldwide; used by governments, enterprises, and critical infrastructure sectors |
| ISO/IEC 27001                 | Internationally certified standard for information security management systems (ISMS) |
| PCI DSS                       | Mandatory for any organization handling payment card data; enforced by major card brands |
| SOC 2                         | Essential for cloud service providers and SaaS companies; focuses on data privacy and trust |
| HIPAA                         | Required in the U.S. healthcare industry for protecting patient health information |
| GDPR                          | Legal requirement for handling EU citizens’ data; sets global privacy standards     |
| MITRE ATT&CK                  | Highly respected in threat intelligence and red teaming; integrated into many security tools |
## 🧠 Why These Stand Out
- NIST CSF is flexible and scalable, making it ideal for organizations of all sizes.
- ISO 27001 offers formal certification, which boosts trust and compliance.
- PCI DSS and HIPAA are regulatory must-haves in finance and healthcare.
- SOC 2 is often a deal-breaker for B2B tech companies.
- GDPR has global influence—even non-EU companies must comply.
- MITRE ATT&CK is the go-to for understanding attacker behavior and mapping defenses.
#  IDS vs IPS vs EDR vs XDR
🛡️ IDS vs IPS vs EDR vs XDR Comparison Table
| Feature                   | Intrusion Detection System (IDS)               | Intrusion Prevention System (IPS)               | Endpoint Detection & Response (EDR)            | Extended Detection & Response (XDR)              |
|---------------------------|-----------------------------------------------|------------------------------------------------|------------------------------------------------|--------------------------------------------------|
| **Primary Function**      | Monitors and alerts on suspicious activity    | Monitors and actively blocks malicious activity| Detects, investigates, and responds to endpoint threats | Correlates and responds to threats across multiple security layers |
| **Response Type**         | Passive (alerts only)                         | Active (blocks/prevents threats)               | Active (isolation, remediation, hunting)       | Active (automated, cross-domain response)        |
| **Deployment Location**   | Network perimeter or host-based               | Network perimeter or host-based                | Installed on endpoints                         | Cloud-native or hybrid across infrastructure      |
| **Threat Visibility**     | Network-level traffic                         | Network-level traffic                          | Endpoint-level behavior and processes          | Unified across endpoints, cloud, identity, etc.   |
| **Detection Methods**     | Signature-based, anomaly-based                | Signature-based, anomaly-based                 | Behavioral analysis, ML, threat intelligence   | AI/ML, behavioral analytics, threat intelligence  |
| **Automated Response**    | No                                            | Yes                                            | Yes                                            | Yes                                              |
| **Use Case**              | Alerting and forensic analysis                | Real-time threat prevention                    | Endpoint threat detection and remediation      | Holistic threat detection across the security stack |
| **False Positives**       | Moderate                                      | Can be high                                    | Lower (context-aware)                          | Lower (correlated across domains)                 |
| **Integration**           | SIEM, firewalls                               | SIEM, firewalls                                | SIEM, SOAR, XDR                                | SIEM, SOAR, EDR, cloud, email, identity, network  |
| **Examples**              | Snort, Suricata                               | Cisco Firepower, Palo Alto Threat Prevention   | CrowdStrike Falcon, SentinelOne, Microsoft Defender for Endpoint | Microsoft Defender XDR, Palo Alto Cortex XDR, Trend Micro Vision One |
## 🧠 Quick Summary
- IDS watches and alerts.
- IPS watches and blocks.
- EDR investigates and responds at the endpoint.
- XDR connects the dots across your entire security ecosystem.
# SOC vs Vulnerability Management vs Threat Intelligence
## 🛡️ SOC vs Vulnerability Management vs Threat Intelligence
| Category              | Security Operations Center (SOC)                         | Vulnerability Management                                    | Threat Intelligence                                         |
|-----------------------|----------------------------------------------------------|-------------------------------------------------------------|-------------------------------------------------------------|
| **Primary Function**   | Monitor, detect, and respond to threats in real time    | Identify, assess, and remediate system vulnerabilities      | Gather, analyze, and contextualize threat data              |
| **Approach**           | Reactive and proactive threat response                  | Proactive risk reduction                                    | Predictive and strategic                                     |
| **Key Activities**     | Alert triage, incident response, log analysis           | Scanning, prioritization, patching                          | Data collection, enrichment, dissemination                  |
| **Tools Used**         | SIEM, SOAR, XDR                                          | Vulnerability scanners, asset management, patch tools       | Threat intelligence platforms, feeds, analytics             |
| **Human Involvement**  | Analysts and incident responders                        | Security engineers and IT operations                        | Threat analysts and researchers                             |
| **Output**             | Incident reports, alerts, metrics                       | Vulnerability dashboards, remediation plans                 | Threat advisories, IOCs, TTPs                               |
| **Integration Potential** | High — ties into EDR, firewalls, and ticketing systems | High — feeds SOC, GRC, and patching systems                 | High — informs SOC, vulnerability, and IR teams             |
| **Goal**               | Minimize damage and response time                       | Reduce attack surface and risk                              | Improve decision-making and threat preparedness             |
| **Examples**           | Responding to ransomware alerts                         | Addressing CVE-2023-XXXXX vulnerabilities                   | Tracking APT group tactics or phishing campaigns            |
## 🧠 Quick Insight
- SOC is your digital fire brigade 🚒
- Vulnerability Management is your building inspector 🏗️
- Threat Intelligence is your neighborhood watch 👁️
## 🧠 Why Threat Intelligence Matters in Vulnerability Management
- Helps prioritize vulnerabilities based on real-world exploitability
- Adds context to CVEs (e.g., is it actively exploited in the wild?)
- Enables risk-based remediation instead of patching everything blindly
- Supports faster response to zero-day threats and emerging campaigns
## 🔍 How the Big Three Integrate Threat Intelligence
| Platform           | Threat Intelligence Integration                                                              |
|--------------------|-----------------------------------------------------------------------------------------------|
| **Qualys VMDR**    | Uses TruRisk scoring powered by 25+ threat feeds; integrates with MITRE ATT&CK and CISA KEV |
| **Tenable One**    | Offers Vulnerability Priority Rating (VPR) using exploitability data, threat feeds, and asset context |
| **Rapid7 InsightVM** | Uses Real Risk Score based on threat intel, CVSS, and asset criticality; integrates with Metasploit for exploit validation |
## 📊 What This Means for You
- These platforms don’t just scan—they analyze threat data to tell you which vulnerabilities are most dangerous.
- They help security teams focus on the 3–5% of vulnerabilities that truly matter, reducing noise and improving efficiency.

So yes, threat intelligence is baked into the DNA of modern vulnerability scanners—and if a tool doesn’t offer it, it’s falling behind.
# Physical Security Controls
- Perimeter Defenses: Barriers, Security Guards, Sensors, Security Buffers
- Locks
- Preventing Data Leakage: Faraday Cage, Protected Distribution System
# Data Controls
## Data Classifications
| **Data Type**    | **Description**                                                                 | **Recommended Handling**                                                                       |
|------------------|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| Confidential     | Highest level of data sensitivity                                                | Only accessible by users with the highest level of preapproved authentication                 |
| Private          | Medium confidentiality; access should be limited                                | Available only to users with a need-to-know basis                                              |
| Sensitive        | Disclosure could cause catastrophic harm                                         | Restricted to employees with business need and formal approval                                |
| Critical         | Essential for organizational functionality; must be available                    | Must be rigorously protected to maintain availability and mission                             |
| Public           | No risk associated with release                                                  | Accessible by all; assumed public if no other data label is present                           |
| Restricted       | Not available to the public                                                      | Exercise caution before using in emails or external communications                            |
## Types of Data
- **Regulated** is that which external stipulations are placed on it regarding who can see and use the data and in what contexts. Examples of regulated data include Protected Health Information (PHI), which is data about a person’s health status, provision of healthcare, or payment for healthcare, and is regulated by the Health Insurance Portability and Account- ability Act of 1996 (HIPAA).
- **Intellectual property (IP)** is an invention or a work that is the result of creativity. The owner of IP can apply for protection from others who attempt to duplicate it;
these protections over IP or its expression are patent, trademark, copyright, or trade secret.
- **Trade secret** is enterprise data that is undisclosed. A trade secret has three
elements: it is information that has either actual or potential independent economic value by
virtue of not being generally known, it has value to others who cannot legitimately obtain the
information, and it is subject to reasonable efforts to maintain its secrecy. All three of these
­elements are required and, if any one of them ceases to exist, then the trade secret will also
cease to exist. Otherwise, there is no limit on the amount of time a trade secret is protected.
## States of Data
- **Data in processing** Data in use (also called data in processing) is data on which actions are
being performed by devices, such as printing a report from a device.
- **Data in transit** Actions that transmit the data across a network, like an email sent across the
Internet, are called data in transit (sometimes called data in motion).
- **Data at rest** \is data that is stored on electronic media.
# Types of Authentication Credentials
| **Element**              | **Description**                                                  | **Scenario Example**                       |
|--------------------------|------------------------------------------------------------------|--------------------------------------------|
| Somewhere you are        | Restricted location                                               | Restricted military base                   |
| Something you are        | Unique biological trait that cannot be changed                   | Fingerprint reader to enter building       |
| Something you have       | Possession of a unique item                                       | Riker’s ID card                            |
| Someone you know         | Validated by a known individual                                   | Li knows Peyton                            |
| Something you exhibit    | Genetically determined physical characteristic                    | Peyton’s flaming red hair                  |
| Something you can do     | A personal behavior or skill difficult to replicate               | Paolo’s signature                          |
| Something you know       | Private knowledge known only to the individual                    | Combination to unlock locker               |
