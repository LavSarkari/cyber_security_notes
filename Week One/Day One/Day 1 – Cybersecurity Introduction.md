
> **Cybersecurity ≠ Just Hacking – It’s Digital Defense**

Cybersecurity is the practice of protecting:

- 🕵️‍♂️ Confidentiality → Keeping data private
- 🛠 Integrity → Ensuring data isn't altered
- 🔁 Availability → Ensuring services stay online

Together, these form the **CIA Triad**, the core principle of cybersecurity.

---
### 🧭 **2. Cybersecurity Domains**

Cybersecurity has multiple domains:
- 🌐 **Network Security**
  - Firewalls, VPNs, Intrusion Detection Systems
- 📱 **Application Security**
  - Code auditing, preventing XSS, SQL injection
- 💻 **Endpoint Security**
  - Protecting laptops, phones, IoT devices
- ☁️ **Cloud Security**
  - Securing AWS, Azure, GCP, cloud APIs
- 🧑‍💼 **Operational Security**
  - Policies, access control, incident response
- 🔐 **Cryptography**`
  - Encryption, hashing, key management
- ⚔️ **Red Team / Blue Team**
  - Simulated attackers vs defenders
---
# 🧱 Attack Surface – Every Digital Entry Point

> **"The attack surface is every potential vulnerability exposed to attackers."**

Common components of an attack surface:

- 📡 Open ports (e.g., SSH, HTTP)
- 🔑 Weak or default passwords
- 🗃 Exposed APIs or services
- 🧓 Outdated software with known exploits
- ☁️ Misconfigured cloud buckets (e.g., public S3)

🧠 Real World:
> A dev server with default credentials left open = attacker’s playground.

---
# 🌍 Threat Landscape – Who and What Are We Defending Against?

| 🧙 Threat Actor      | 🎯 Motivation                  |
| -------------------- | ------------------------------ |
| Script Kiddies       | Fun, curiosity, low skill      |
| Hacktivists          | Ideological or political cause |
| Cybercriminals       | Financial gain                 |
| State-Sponsored APTs | Espionage, infrastructure      |
| Insider Threats      | Disgruntled employees, leaks   |

## Attack Vectors
- 📨 Phishing
- 🐛 Malware
- 🧠 Social Engineering
- 🌐 Drive-by downloads
- 🧨 DDoS attacks

---
# 💻 Hacking Operating Systems – Kali, Parrot, Arch

| 🐧 OS         | 👍 Strengths                          | 🧪 Use Case                     |
|--------------|--------------------------------------|--------------------------------|
| Kali Linux   | Most tools, stable, large community  | Pentesting, standard hacking   |
| Parrot OS    | Lightweight, anonymous by default    | Privacy, forensics, education  |
| Arch Linux   | Minimalist, build-your-own           | Advanced users, custom setups  |
### Why Linux for hacking?
- Full control over permissions and processes
- Powerful command-line tools
- Better network stack manipulation

---
# 🧪 Lab Setup – Today's Practical Goals

We'll be using **Kali Linux**. Your goal is to:

1. ✅ Boot into Kali (via VM or USB)
2. ✅ Explore the desktop and terminal
3. ✅ Launch and test tools like:
    - `nmap`
    - `ping`
    - `whois`
4. ✅ Check network mode (NAT or Bridged)
5. ✅ Start documenting everything in Obsidian!

> Keep a habit of logging tools, syntax, output.  
> Obsidian will be your **hacker's diary** 📓

⚠️ Ensure network access and virtualization are configured correctly.
