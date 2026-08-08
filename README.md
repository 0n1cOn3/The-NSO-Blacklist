<h1 align="center">🔍 How to catch NSO Group's Pegasus</h1>


### Introduction

NSO Group claims that its Pegasus spyware is only used to "investigate terrorism and crime" and "leaves no traces whatsoever". 
This Forensic Methodology Report shows that neither of these statements are true. This report accompanies the release of the Pegasus Project,        
a collaborative investigation that involves more than 80 journalists from 17 media organizations 
in 10 countries coordinated by Forbidden Stories with technical support of "Amnesty International's Security Lab"*.

### Why?

However, on further analysis we* also noticed suspicious redirects and we can at least from the forensic work, use the information to prevent certain Domains and DNS's. It should make it harder for Pegasus, to communicate with the C&C's from the NSO Group.

### Purpose?

This is a list of domains and DNSs which has been collected from Amnesty International's Security Lab.

🔗 Original forensic methodology report (2021):

    https://www.amnesty.org/en/latest/research/2021/07/forensic-methodology-report-how-to-catch-nso-groups-pegasus/

🔗 **NEW (July 2026)** — Inside Pegasus: The evolution of the world's most notorious spyware:

    https://securitylab.amnesty.org/latest/2026/07/inside-pegasus-the-evolution-of-the-worlds-most-notorious-spyware/

This 2026 Amnesty report draws on **leaked NSO Group internal documents** from the WhatsApp v. NSO Group court case, revealing:
- Pegasus internal architecture ("White Services" department, anonymization network)
- Infection vector names: **Heaven**, **Erised**, **Eden**, **Hummingbird** (WhatsApp 0-click family)
- Customer-specific infrastructure fingerprinting methodology (validated)
- "Abuse Prevention" system, "Sales 3"/"Sales 6" test deployments
- Dashboard roles, credential theft capabilities, cloud data extraction

See `pegasus-architecture.txt` for the full technical breakdown.

### What's Inside

| File | Description |
|------|-------------|
| `hosts.txt` | Pegasus-related domains and IPs (Pi-hole / AdGuard format) |
| `C2-hosts.txt` | Known C2 IP:port pairs |
| `pegasus-architecture.txt` | Internal architecture, vector names, White Services methodology (from 2026 court document analysis) |
| `pegasus-architecture.svg` | Visual architecture diagram (SVG) — delivery vectors, exploitation chain, C2 infrastructure |

### Pi-hole / AdGuard Home

The list can be added to Pi-hole and gives a layer of protection against Pegasus C2 communication.

```
https://raw.githubusercontent.com/0n1cOn3/The-NSO-Blacklist/main/hosts.txt
https://raw.githubusercontent.com/0n1cOn3/The-NSO-Blacklist/main/C2-hosts.txt
```

### ⚠️ Limitations

- This is **not** a complete list of all NSO Group infrastructure
- Some customers prevent Internet scanning exposure
- IPs rotate; domains may be decommissioned or repurposed
- False positives are possible — investigate before taking action
- NSO Group actively evolves its infrastructure TTPs

## Other Sources / Forks

🔗 https://github.com/Red-Laboratory/NSO-hosts

🔗 https://github.com/jjjxu/NSO_Pegasus_Blocklist

🔗 https://github.com/AmnestyTech/investigations

🔗 **Amnesty Security Lab — full research archive:**
    https://securitylab.amnesty.org/search/

🔗 https://securitylab.amnesty.org/latest/2026/07/inside-pegasus-the-evolution-of-the-worlds-most-notorious-spyware/

🔗 **Pegasus Project Case Study (Amnesty):**
    https://securitylab.amnesty.org/case-study-the-pegasus-project/

---

### Sister Projects

🔗 **The Paragon Blacklist** (Graphite IOCs): https://github.com/0n1cOn3/The-Paragon-Blacklist

🔗 **The Intellexa Blocklist** (Predator IOCs): https://github.com/0n1cOn3/The-Intellexa-Blocklist
