# 🔎 NETWORKSWALKS-B082-WK2-PM1-Footprinting-Reconnaissance-with-Kali-Linux

![Cybersecurity](https://img.shields.io/badge/Field-Cybersecurity-red)
![Kali Linux](https://img.shields.io/badge/OS-Kali%20Linux-blue)
![Project](https://img.shields.io/badge/Project-Footprinting%20%26%20Reconnaissance-green)
![Ethical Hacking](https://img.shields.io/badge/Focus-Ethical%20Hacking-orange)
<br/>
Cybersecurity reconnaissance lab using multiple Kali Linux tools for ethical hacking and footprinting

## 📌 Project Overview

This project was completed as part of **Week 2 – Project Module 1 (W2-PM1)** of my cybersecurity ethical hacking training with **Networkwalks**.

The purpose of this lab was to learn how reconnaissance and footprinting can be performed using publicly available information.

I used several Kali Linux tools to collect information about the domain **networkwalks.com**, including:

* Domain registration information
* Web technologies
* Domain/IP resolution
* HTTP response headers
* Web Application Firewall (WAF) detection
* DNS records

The exercise helped me understand how attackers and security professionals gather information about a target before moving to later stages of security testing.

---

# 🎯 Objectives

The main objectives of this project were to:

1. Understand the purpose of reconnaissance in cybersecurity.
2. Use `whois` to retrieve domain registration information.
3. Use `whatweb` to identify web technologies.
4. Use `nslookup` to resolve a domain to an IP address.
5. Use `curl` to inspect HTTP response headers.
6. Use `wafw00f` to identify a Web Application Firewall.
7. Use `dnsrecon` to enumerate DNS records.
8. Document reconnaissance findings.

---

# 🧰 Tools Used

| Tool       | Purpose                                       |
| ---------- | --------------------------------------------- |
| `whois`    | Domain registration and ownership information |
| `whatweb`  | Web technology fingerprinting                 |
| `nslookup` | DNS and IP address resolution                 |
| `curl`     | HTTP response header analysis                 |
| `wafw00f`  | Web Application Firewall detection            |
| `dnsrecon` | DNS record enumeration                        |
| Kali Linux | Penetration testing environment               |

---

# 🌐 Target

**Target Domain:**

```text
networkwalks.com
```

The target was provided as part of the authorized educational lab.

---

# 🔍 Task 1 – WHOIS

## Objective

Use `whois` to retrieve publicly available domain registration information.

## Command

```bash
whois networkwalks.com
```

## What I Looked For

The WHOIS information can contain details such as:

* Registrar
* Registration date
* Expiry date
* Name servers
* Domain status
* Registration information

## Evidence

<img width="602" height="489" alt="image" src="https://github.com/user-attachments/assets/b0405fbe-624d-4a7a-99dc-6d94a3aa15cb" />

## Output

The command output was saved in:

```text
outputs/whois.txt
```

## What I Learned

I learned that WHOIS can provide useful information about a domain without needing to directly interact with the website itself.

This information can help a security professional understand the domain's registration and DNS infrastructure.

---

# 🌐 Task 2 – WhatWeb

## Objective

Identify the technologies used by the target website.

## Command

```bash
whatweb networkwalks.com
```

## What I Looked For

WhatWeb can identify technologies such as:

* Web server
* Content Management System (CMS)
* Frameworks
* Plugins
* JavaScript libraries
* IP address
* Other technologies exposed by the website

## Evidence

<img width="602" height="241" alt="image" src="https://github.com/user-attachments/assets/4b9bf869-3533-4e96-a37e-baef4b2272ff" />

## Output

The command output was saved in:

```text
outputs/whatweb.txt
```

## What I Learned

I learned how technology fingerprinting can reveal information about the software stack behind a website.

This information can later be compared against known vulnerabilities during an authorized security assessment.

---

# 🌍 Task 3 – NSLookup

## Objective

Resolve the target domain name to its IP address.

## Command

```bash
nslookup networkwalks.com
```

## Evidence

<img width="415" height="152" alt="image" src="https://github.com/user-attachments/assets/1581d030-a44e-4ffd-956c-31d7d6b98170" />

## Output

The command output was saved in:

```text
outputs/nslookup.txt
```

## What I Learned

I learned how DNS translates a human-readable domain name into an IP address.

Understanding DNS resolution is important during reconnaissance because it provides information about the infrastructure associated with a domain.

---

# 📡 Task 4 – CURL HTTP Headers

## Objective

Inspect the HTTP response headers returned by the target website.

## Command

```bash
curl -I https://networkwalks.com
```

## What I Looked For

HTTP response headers can reveal information such as:

* HTTP status code
* Server information
* Cookies
* Redirects
* Security headers
* Caching information
* Other technologies or services

## Evidence

<img width="602" height="146" alt="image" src="https://github.com/user-attachments/assets/0749927b-8775-460b-b634-ce541972af44" />

## Output

The command output was saved in:

```text
outputs/curl.txt
```

## What I Learned

I learned that HTTP headers can expose useful information about how a web server is configured.

From a defensive perspective, reviewing these headers can help identify unnecessary information disclosure and missing security headers.

---

# 🛡️ Task 5 – WAFW00F

## Objective

Determine whether the target website is protected by a Web Application Firewall.

## Command

```bash
wafw00f networkwalks.com
```

## Evidence

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/6c25e8ce-c78d-43a7-879a-c394fc5f73e0" />

## Output

The command output was saved in:

```text
outputs/wafw00f.txt
```

## What I Learned

I learned how `wafw00f` can be used to identify whether a website is using a Web Application Firewall.

A WAF can provide an additional security layer by inspecting and filtering malicious web traffic.

---

# 🗂️ Task 6 – DNSRecon

## Objective

Enumerate DNS records associated with the target domain.

## Command

```bash
dnsrecon -d networkwalks.com
```

## What I Looked For

The DNS enumeration included information such as:

* Name servers
* Mail servers
* A records
* TXT records
* SPF information
* Other DNS records
* Service records where available

## Evidence

<img width="602" height="271" alt="image" src="https://github.com/user-attachments/assets/c52afc98-f1da-4695-a84a-c9f8fad47cfa" />

## Output

The command output was saved in:

```text
outputs/dnsrecon.txt
```

## What I Learned

I learned how DNS reconnaissance can reveal different components of an organization's infrastructure.

DNS records are important during security assessments because they can expose information about services, mail infrastructure and other publicly accessible systems.

---

# 📊 Reconnaissance Summary

| Task | Tool     | Information Collected           |
| ---- | -------- | ------------------------------- |
| 1    | WHOIS    | Domain registration information |
| 2    | WhatWeb  | Website technologies            |
| 3    | NSLookup | Domain/IP resolution            |
| 4    | CURL     | HTTP response headers           |
| 5    | WAFW00F  | WAF detection                   |
| 6    | DNSRecon | DNS records                     |

---

# 🧠 Key Lessons

Through this project, I learned that reconnaissance is an important part of ethical hacking and penetration testing.

The different tools provide different pieces of information:

```text
WHOIS
   ↓
Domain Registration Information
   ↓
WhatWeb
   ↓
Technology Fingerprinting
   ↓
NSLookup
   ↓
IP Address Information
   ↓
CURL
   ↓
HTTP Header Information
   ↓
WAFW00F
   ↓
WAF Detection
   ↓
DNSRecon
   ↓
DNS Infrastructure
```

Using the tools together provides a broader understanding of the target's publicly exposed infrastructure.

---

# ⚠️ Ethical Considerations

Reconnaissance tools can be useful for legitimate security testing, but they should only be used against systems that you own or have explicit permission to assess.

For this project, the target was provided as part of an intenship cybersecurity exercise.

I did not attempt to exploit vulnerabilities or gain unauthorized access to the target.

---

# 🚀 Skills Demonstrated

* Linux command-line usage
* Kali Linux
* Passive reconnaissance
* DNS reconnaissance
* Domain enumeration
* Web technology fingerprinting
* HTTP header analysis
* WAF identification
* DNS record enumeration
* Cybersecurity documentation
* Ethical hacking methodology

---

# 📚 References

* Kali Linux security tools
* WHOIS
* WhatWeb
* NSLookup
* cURL
* WAFW00F
* DNSRecon

---

## 👨‍💻 Author

**Malehloa Seroke**

Cybersecurity | IT Infrastructure | Ethical Hacking

This repository documents my practical cybersecurity learning journey and hands-on experience with reconnaissance and penetration-testing tools.
