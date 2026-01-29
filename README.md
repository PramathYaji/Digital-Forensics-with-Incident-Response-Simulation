# Digital Forensics with Incident Response Simulation

##### This project is fictional and is deidcated for those who would like to learn through narration.

---
## Preface - Scenario Design
I started off with the idea of simulating a cyberattack and then performing forensic analysis to understand what kind of data might have been exfiltrated. The initial approach was purely technical, there was no storyline behind it. It was just about carrying out an attack and analyzing the system later. At first, I explored the idea of DNS tunneling, but that plan was dropped since it would have required a registered domain to make it work well. 

From there, the scenario began to evolve. I decided to bring in a social engineering angle - something like phishing - and that’s when the story started taking shape. Instead of treating the insider as simply malicious, I thought it would be more interesting to present the user as someone who had been manipulated or coerced. This added a more layered perspective to the situation. 

As the storyline developed, I added in technical elements like phishing emails, Remote File Inclusion (RFI), and privilege escalation through sudoers misconfiguration. The final scenario blended both behavioral and technical aspects, giving a well-rounded case to investigate from a forensic standpoint.

---
## Bruce Industries
Bruce Industries is a globally recognized leader in Very-Large-Scale Integration (VLSI) design and
semiconductor manufacturing. With decades of innovation, the company is known for developing advanced microarchitecture solutions that power next-generation computing technologies. It serves clients
across a broad range of high-tech sectors.

To safeguard its digital assets - particularly against espionage and insider leaks - Bruce Industries has
heavily invested in internal security infrastructure. A key measure is the deployment of a Transport Layer
Security (TLS) interception system, or SSL proxy, which decrypts, inspects, and re-encrypts employee
HTTPS traffic to detect anomalies such as phishing attempts, malware infections, and unauthorized
data transfers.

Acknowledging the increasing complexity of modern cyberattacks, the company proactively initiated a
Red Team simulation to evaluate the effectiveness of its Incident Response procedures and the readiness of
its Digital Forensics team. The simulation centered on a potential insider threat under external coercion,
testing the organization’s ability to detect, analyze, and respond to blended, real-world threats.

---
## Objectives
The purpose of this investigation was to examine how Bruce Industries’ security team would detect and
handle a subtle, high-stakes security scenario involving an internal user influenced by external pressure. By
simulating a blended threat that combined social engineering with technical exploitation, the exercise tested
the organization’s ability to respond to ambiguous and evolving risks.

The investigation aimed to:

• Reconstruct key events leading to the unauthorized exposure of sensitive data.

• Identify how vulnerabilities were introduced and exploited.

• Assess the readiness and decision-making process of the forensic team.

• Inform future improvements to insider threat detection, user monitoring, and training protocols.

---
## Tools and Procedures
The investigation primarily relied on the following forensic tools:

• **Autopsy**: Used for disk image analysis, timeline reconstruction, keyword searches, and file system
exploration.

• **Wireshark**: Used to examine PCAP files capturing HTTP traffic from within the internal network.
These packets included decrypted HTTPS sessions made available through TLS interception, allowing
the forensic team to identify suspicious POST requests and file uploads to vulnerable endpoints.

All tools used in this investigation are widely accepted within the digital forensics community and maintain a strong reputation for forensic reliability. Autopsy, in particular, is built on The Sleuth Kit and adheres
to recognized standards for forensic integrity and evidence handling

The forensic process began with the review of network traffic captures using Wireshark. These captures included decrypted HTTPS sessions obtained through Bruce Industries’ TLS interception infrastructure. Analysts observed unusual POST requests and file uploads to the HR web server, suggesting potential
exploitation of upload functionality.

Following this, a disk image of the affected HR system was examined using Autopsy. The analysis
focused on file access patterns, user activity, and indicators of privilege escalation.

Key forensic procedures included:

• Analysis of authentication logs to track account elevation and privilege misuse.

• Examination of file transfers, including the movement of sensitive encrypted files and the extraction
of decryption keys.

• Detection of steganographic behavior, where confidential data was embedded in media files.

• Timeline reconstruction by correlating user commands, timestamps, and system responses.

• Validation of actions through screenshots and command history for evidentiary support.
The disk image was mounted in a read-only state to ensure evidence integrity. All actions taken were
documented and aligned with forensic best practices to ensure repeatability and reliability of findings.

---
## Findings

<div align="center">
  <img width="985" height="555" alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Phishing%20Email%20from%20Spoofed%20Domain.png" />
  <p><em>Fig 1. Phishing Email from a Spoofed Domain</em></p>
</div>

<div align="center">
  <img width="985" height="555" alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Follow-Up%20Phishing%20Email%20with%20Exploit%20Instructions.png" />
  <p><em>Fig 2. Follow-Up Phishing Email with Exploit Instructions</em></p>
</div>

## Steganographic Evidence

<div align="center">
  <img width="985" height="555" alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Initial%20Inspection%20of%20Image%20File%20Using%20strings%20Utility.png" />
  <p><em>Fig 3. Initial Inspection of Image File Using strings Utility</em></p>
</div>

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Extracted%20Employee%20Data%20from%20Steganographic%20Image.png" />
  <p><em>Fig 4. Extracted Employee Data from Steganographic Image</em></p>
</div>

---
## Vulnerability Exploitation Evidence

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/SQL%20Injection%20Attempt.png" />
  <p><em>Fig 5. SQL Injection Attempt</em></p>
</div>

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Successful%20Upload%20of%20a%20PHP%20Reverse%20Shell.png" />
  <p><em>Fig 6. Successful Upload of PHP Reverse Shell</em></p>
</div>

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Evidence%20of%20Remote%20Root%20Shell%20Session.png" />
  <p><em>Fig 7. Evidence of Remote Root Shell Session</em></p>
</div>

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Wireshark%20Capture%20Showing%20Privilege%20Escalation%20via%20vim.png" />
  <p><em>Fig 7. Wireshark Capture Showing Privilege Escalation via vim</em></p>
</div>

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Reconnaissance%20in%20the%20HR%20Manager%E2%80%99s%20Directory.png" />
  <p><em>Fig 8. Reconnaissance in HR Manager's Directory</em></p>
</div>

<div align="center">
  <img alt="image" src="https://github.com/PramathYaji/Digital-Forensics-with-Incident-Response-Simulation/blob/main/images/Exfiltrating%20Data%20Through%20Python%20Server.png" />
  <p><em>Fig 9. Exfiltrating Data Through Python Server</em></p>
</div>

---
## Mitigation Steps

To address the gaps identified during the simulation, the following general mitigation strategies are recommended:

• Deliver ongoing, role-specific training to improve employee recognition of phishing, social engineering, and abnormal system behavior.

• Regularly audit user permissions and privilege escalation pathways to ensure alignment with operational needs.

• Identify and remediate web application flaws through secure development practices and vulnerability scans.

• Utilize system and network monitoring to flag unusual activities, such as unsanctioned sudo changes, shell activity, and data movements.

• Perform regular integrity checks on files like sudoers, and enforce hardened defaults for services exposed internally or externally.

• Continue regular assessments to evaluate detection, response, and containment capabilities in evolving threat scenarios.

---
