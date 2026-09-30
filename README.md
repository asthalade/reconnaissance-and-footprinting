# Reconnaissance & Footprinting

Passive and semi-passive information gathering to map a target's public attack surface before any active testing. Performed in an authorized, controlled setting as part of an ethical hacking internship.

## Objective
Understand how publicly available data (domains, subdomains, emails, DNS records) can be used to map an attack surface without directly interacting with the target.

## Environment & Tools
| Tool | Purpose |
|------|---------|
| theHarvester | Collect emails, subdomains and hostnames from public sources |
| WHOIS | Domain registration, registrar and ownership details |
| dig | DNS queries (A, MX, NS, TXT records) |
| nslookup | Domain-to-IP mapping and DNS lookups |
| Kali Linux | Platform for running the tools |

## Workflow
```
Recon tools -> Public data sources -> Information extraction -> Analysis & attack surface mapping
```

## What Was Gathered
- Domain registration details (WHOIS): [registrar, creation/expiry dates]
- IP addresses and DNS records (A, MX, NS): [add examples]
- Subdomains and public email addresses (theHarvester): [add counts, not personal data]

## Example Commands
```bash
whois example.com
dig example.com A MX NS TXT
nslookup example.com
theHarvester -d example.com -b duckduckgo
```

## Key Learnings
- Reconnaissance shapes every later testing phase.
- Passive collection avoids touching the target and reduces detection.
- Collected data should be handled responsibly and kept out of public repos.

## Disclaimer
Performed only on targets I own or am authorized to assess, for educational purposes.
