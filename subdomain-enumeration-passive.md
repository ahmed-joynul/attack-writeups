# Passive Subdomain Enumeration — Microsoft

## Target
microsoft.com

Purpose: Educational reconnaissance demonstration in safe lab context.

---

## What is a Subdomain?

A subdomain is a subdivision of a main domain used to organize services or sections.

Examples:
- blog.example.com
- shop.example.com

Structure:
```
[subdomain].[domain].[tld]
```

Example:
```
portal.microsoft.com
```

---

## Why Subdomain Enumeration Matters (Attacker View)

Subdomains often reveal:

- hidden services
- staging environments
- admin panels
- dev systems
- legacy servers

Attackers use these to find weak entry points.

---

## Tool Used

subfinder — passive subdomain enumeration tool by ProjectDiscovery.

Type: Passive Recon Tool  
Noise Level: Low  
Detectability: Minimal

---

## Command Executed

```
subfinder -d microsoft.com
```

---

## Result

Tool returned ~8000 discovered subdomains.

Sample findings:

```
watson103.watson.microsoft.com
logbuilderqa.mspartner.microsoft.com
lync25.lyncweb.microsoft.com
openisv.partners.extranet.microsoft.com
windowsupdate.microsoft.com
```

---

## Intelligence Value

Enumeration revealed:

- internal infrastructure naming patterns
- service segmentation
- environment separation
- partner portals
- staging environments

This provides attackers with a map of target surface area.

---

## Alternative Enumeration Tool

Website Tool:
```
https://subdomainfinder.c99.nl/
```

Feature:
Private Scan mode allows hidden queries.

---

## Security Perspective (Defense)

Organizations should:

- monitor DNS enumeration traffic
- remove unused subdomains
- avoid predictable naming
- isolate internal environments

Subdomains increase attack surface.

---

## Skills Demonstrated

- Passive Reconnaissance
- OSINT Gathering
- Subdomain Discovery
- Attack Surface Mapping

---

## MITRE ATT&CK Mapping

Technique:
T1590 — Gather Victim Network Information
