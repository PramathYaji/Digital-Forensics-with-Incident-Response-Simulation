# Digital Forensics with Incident Response Simulation

##### This project is fictional and is deidcated for those who would like to learn through narration.

---
### Preface - Scenario Design
I started off with the idea of simulating a cyberattack and then performing forensic analysis to understand what kind of data might have been exfiltrated. The initial approach was purely technical, there was no storyline behind it. It was just about carrying out an attack and analyzing the system later. At first, I explored the idea of DNS tunneling, but that plan was dropped since it would have required a registered domain to make it work well. 

From there, the scenario began to evolve. I decided to bring in a social engineering angle - something like phishing - and that’s when the story started taking shape. Instead of treating the insider as simply malicious, I thought it would be more interesting to present the user as someone who had been manipulated or coerced. This added a more layered perspective to the situation. 

As the storyline developed, I added in technical elements like phishing emails, Remote File Inclusion (RFI), and privilege escalation through sudoers misconfiguration. The final scenario blended both behavioral and technical aspects, giving a well-rounded case to investigate from a forensic standpoint.

---
### Bruce Industries
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
