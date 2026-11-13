# NETWORKWALKS-GAURANG-B084-WK2-Recon-and-Scanning
# 🔐 NETWORKWALKS – WEEK 2 PROJECT

## Footprinting & Reconnaissance Using Multiple Kali Linux Tools

**Cybersecurity & Ethical Hacking Internship**

---

## 📌 PROJECT DETAILS

| Field                   | Details                         |
| ----------------------- | ------------------------------- |
| Intern Name             | Gaurang Parmar                  |
| Organization            | Networkwalks                    |
| Internship Domain       | Cybersecurity & Ethical Hacking |
| Internship Week         | Week 2                          |
| Project Module          | W2-PM1                          |
| Project Title           | Footprinting & Reconnaissance   |
| Operating System        | Kali Linux                      |
| Virtualization Platform | Oracle VirtualBox               |
| Target Domain           | networkwalks.com                |
| Date                    | 13 November 2026                |

---

## ⚠️ DISCLAIMER

This project is performed strictly for educational and cybersecurity training purposes as part of the Networkwalks internship program.

All testing activities should only be performed on systems and networks for which appropriate authorization has been obtained.

The information documented in this repository represents observations collected using the tools demonstrated in the internship practical.

Unauthorized access, scanning or testing of systems without permission is prohibited.

---

## 📖 1. INTRODUCTION

Footprinting and reconnaissance are important initial stages of ethical hacking and cybersecurity assessments.

During Week 2 of my Networkwalks internship, I worked on Project Module 1, which focuses on collecting publicly available information about a target website using multiple Kali Linux tools.

The practical involves examining:

- Domain registration information.
- Website technologies.
- DNS records and IP addresses.
- HTTP response headers.
- Web Application Firewall (WAF) information.
- DNS infrastructure.

Six different Kali Linux tools were introduced to perform these activities.

---

## 🎯 2. OBJECTIVES

The main objectives of this project are:

1. Understand the fundamentals of footprinting and reconnaissance.
2. Retrieve domain registration information using WHOIS.
3. Identify website technologies using WhatWeb.
4. Resolve domain names into IP addresses using NSLookup.
5. Examine HTTP response headers using cURL.
6. Identify Web Application Firewalls using WAFW00F.
7. Enumerate DNS records using DNSRecon.
8. Understand how attackers use publicly available information.
9. Document the observations and results obtained from each tool.

---

## 🛠️ 3. TOOLS USED

| No. | Tool       | Purpose                                             |
| --- | ---------- | --------------------------------------------------- |
| 1   | WHOIS      | Retrieve domain registration details.               |
| 2   | WhatWeb    | Identify website technologies and frameworks.       |
| 3   | NSLookup   | Resolve domain names into IP addresses.             |
| 4   | cURL       | Inspect HTTP response headers.                      |
| 5   | WAFW00F    | Detect Web Application Firewalls.                   |
| 6   | DNSRecon   | Enumerate DNS records.                              |
| 7   | Kali Linux | Operating system used for practical implementation. |

---

# 🔎 4. ACTIVITIES PERFORMED

## TASK 1 – WHOIS DOMAIN INFORMATION GATHERING

### Objective

Retrieve publicly available domain registration information.

### Command Executed

```bash
whois networkwalks.com
```

### Observations

| Parameter     | Result               |
| ------------- | -------------------- |
| Domain        | networkwalks.com     |
| Registrar     | GoDaddy.com, LLC     |
| Creation Date | 6 November 2019      |
| Expiry Date   | 6 November 2027      |
| WHOIS Server  | whois.godaddy.com    |
| Name Server 1 | NS6135.HOSTGATOR.COM |
| Name Server 2 | NS6136.HOSTGATOR.COM |
| DNSSEC        | Unsigned             |

### Output File

`task1_whois.txt`

### Result

The WHOIS command successfully retrieved the domain registration details, including the registrar, creation date, expiry date and name servers.

---

## TASK 2 – WHATWEB TECHNOLOGY FINGERPRINTING

### Objective

Identify the technologies and frameworks running on the target website.

### Command Executed

```bash
whatweb networkwalks.com
```

### Observations

| Parameter          | Result           |
| ------------------ | ---------------- |
| Target             | networkwalks.com |
| HTTP Status        | 200 OK           |
| Web Server         | Apache           |
| CMS                | WordPress        |
| WordPress Version  | 7.1.4            |
| Bootstrap          | 7.1.4            |
| jQuery             | 3.7.1            |
| IP Address         | 192.232.216.135  |
| Country            | United States    |
| Google Tag Manager | Detected         |

### Output File

`task2_whatweb.txt`

### Result

WhatWeb successfully identified the website technologies, including Apache, WordPress, Bootstrap and jQuery.

---

## TASK 3 – NSLOOKUP DNS RESOLUTION

### Objective

Resolve the target domain name into its corresponding IP address using DNS.

### Command Executed

```bash
nslookup networkwalks.com
```

### Observations

| Parameter           | Result                   |
| ------------------- | ------------------------ |
| DNS Server          | 8.8.8.8                  |
| DNS Port            | 53                       |
| Domain              | networkwalks.com         |
| Resolved IP Address | 192.232.216.135          |
| Response            | Non-authoritative answer |

### Output File

`task3_nslookup.txt`

### Result

NSLookup successfully resolved the domain name and returned its corresponding IP address using Google's public DNS server.

---

## TASK 4 – CURL HTTP RESPONSE HEADER ANALYSIS

### Objective

Inspect HTTP response headers to understand the web server's response and configuration.

### Command Executed

```bash
curl -I https://networkwalks.com
```

### Observations

| Parameter          | Result                                               |
| ------------------ | ---------------------------------------------------- |
| Target             | [https://networkwalks.com](https://networkwalks.com) |
| HTTP Protocol      | HTTP/1.1                                             |
| Response Status    | 200 OK                                               |
| Web Server         | Apache                                               |
| Content Type       | text/html; charset=UTF-8                             |
| Cookie             | \_\_wpdm_client                                      |
| HttpOnly           | Present                                              |
| Secure             | Present                                              |
| Referrer Policy    | no-referrer-when-downgrade                           |
| WordPress REST API | Detected                                             |

### Output File

`task4_curl.txt`

### Result

cURL successfully retrieved the HTTP response headers and provided information about the web server, cookies, security attributes and WordPress-related endpoints.

---

## TASK 5 – WAFW00F WEB APPLICATION FIREWALL DETECTION

### Objective

Identify whether a Web Application Firewall protects the target website.

### Command

```bash
wafw00f networkwalks.com
```

### Information to Observe

- Whether a WAF is detected.
- WAF vendor or identification.
- Firewall detection results.

### Output File

`task5_wafw00f.txt`

### Result

To be updated after completing the practical.

---

## TASK 6 – DNSRECON DNS ENUMERATION

### Objective

Enumerate publicly available DNS records associated with the target domain.

### Command

```bash
dnsrecon -d networkwalks.com
```

### Information to Observe

- A records.
- NS records.
- MX records.
- TXT records.
- SPF records.
- SRV records.
- SOA records.

### Output File

`task6_dnsrecon.txt`

### Result

To be updated after completing the practical.

---

# 📊 5. RESULTS AND OBSERVATIONS

The first four practical tasks demonstrated how different tools collect different types of information about a website.

| Tool     | Information Collected       | Status    |
| -------- | --------------------------- | --------- |
| WHOIS    | Domain registration details | Completed |
| WhatWeb  | Website technologies        | Completed |
| NSLookup | DNS and IP resolution       | Completed |
| cURL     | HTTP response headers       | Completed |
| WAFW00F  | Firewall detection          | Pending   |
| DNSRecon | DNS enumeration             | Pending   |

---

# 🛡️ 6. SECURITY SIGNIFICANCE

Footprinting helps cybersecurity professionals understand what information about an organization is publicly accessible.

The information gathered through reconnaissance may help identify:

1. Domain ownership and registration details.
2. Website technologies and software versions.
3. Public IP addresses.
4. Web server configuration.
5. Security-related HTTP headers.
6. DNS infrastructure.

Organizations can use the same reconnaissance techniques to understand their external exposure and improve their security configurations.

---

# 🎓 7. LEARNING OUTCOMES

Through this practical, I gained experience in:

1. Using Kali Linux for cybersecurity activities.
2. Understanding domain registration information through WHOIS.
3. Identifying website technologies using WhatWeb.
4. Understanding DNS resolution using NSLookup.
5. Inspecting HTTP headers using cURL.
6. Understanding the purpose of Web Application Firewalls.
7. Learning DNS enumeration techniques.
8. Saving terminal outputs for technical documentation.
9. Capturing screenshots as practical evidence.
10. Understanding the importance of reconnaissance in ethical hacking.

---

# 📁 8. REPOSITORY STRUCTURE

```text
NETWORKWALKS-WEEK2-PM1/
│
├── README.md
│
├── task1_whois.txt
├── task2_whatweb.txt
├── task3_nslookup.txt
├── task4_curl.txt
├── task5_wafw00f.txt
├── task6_dnsrecon.txt
│
└── Screenshots/
    ├── Task1_WHOIS.png
    ├── Task2_WhatWeb.png
    ├── Task3_NSLookup.png
    ├── Task4_Curl.png
    ├── Task5_WAFW00F.png
    └── Task6_DNSRecon.png
```

---

# 📝 9. CONCLUSION

The Week 2 Project Module 1 practical provided hands-on experience with footprinting and reconnaissance using multiple Kali Linux tools.

By using WHOIS, WhatWeb, NSLookup and cURL, I successfully collected domain registration information, identified website technologies, resolved DNS records and examined HTTP response headers.

The remaining practical activities involve WAF detection using WAFW00F and DNS enumeration using DNSRecon.

This exercise helped me understand the importance of reconnaissance in cybersecurity and how publicly available information can be used to understand an organization's digital footprint.

---

# 👩‍💻 10. AUTHOR

**Gaurang Parmar**

Cybersecurity & Ethical Hacking Intern

Networkwalks – Week 2

Project Module: W2-PM1

---

