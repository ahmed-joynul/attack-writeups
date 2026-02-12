# DNS Enumeration Lab — Microsoft

## Target
microsoft.com

Purpose: Educational reconnaissance practice in authorized lab-style environment.

---

## Tools Used
- host
- nslookup
- dig

---

## 1 — Name Server Enumeration

Command:

host -t ns microsoft.com


Findings:
- ns1-39.azure-dns.com
- ns2-39.azure-dns.net
- ns3-39.azure-dns.org
- ns4-39.azure-dns.info

Insight:
Target infrastructure uses Microsoft Azure DNS.

---

## 2 — Mail Server Enumeration

Command:

host -t mx microsoft.com

Result:

microsoft-com.mail.protection.outlook.com


Insight:
Mail handled through Outlook protection gateway.

---

## 3 — NSLookup Enumeration

Commands:

nslookup
set type=ns
microsoft.com


Result:
Confirms Azure DNS nameservers.

---

## 4 — Advanced DNS Enumeration With DIG

Commands:

dig microsoft.com a
dig microsoft.com aaaa
dig microsoft.com mx
dig microsoft.com txt
dig microsoft.com cname


Purpose:
Extract deeper infrastructure intelligence.

---

## Record Types Investigated

| Record | Purpose |
|------|--------|
A | IPv4 mapping |
AAAA | IPv6 mapping |
MX | Mail routing |
TXT | SPF / verification |
CNAME | Domain aliases |

---

## Recon Intelligence Value

DNS enumeration reveals:

- infrastructure provider
- mail system provider
- redundancy configuration
- external dependencies

Attackers use this information to map attack surface before exploitation.

---

## Defensive Perspective

Organizations should:

- avoid unnecessary DNS exposure
- restrict zone transfers
- monitor enumeration activity

DNS is public intelligence. Treat it as visible attack surface.

---

## Skills Demonstrated

- Passive Reconnaissance
- DNS Intelligence Gathering
- Enumeration Tool Usage
- Infrastructure Mapping

---

## MITRE ATT&CK Mapping

Technique:
T1590 — Gather Victim Network Information

