# AI Recon Elite

## Mission
A professional, structured reconnaissance framework for AI infrastructure (OpenAI, Anthropic, Hugging Face, Google, Groq). This repository follows the **13 Pillars of Recon 2026** and contains **only OSINT, secret hunting, and external attack surface mapping**. No exploitation, no jailbreaks—pure reconnaissance.

## The 13 Pillars

| #  | Category | Tools | Status |
|----|----------|-------|--------|
| 1  | Subdomain Enumeration | HaXder, BBOT, Scion, Subfinder, Amass | Active |
| 2  | Cloud Bucket Hunting | s3dns, cloud.sh, S3Scanner, Gobuster | Active |
| 3  | Service Fingerprinting | AIMap, KBF, httpx, curl, Burp | Active |
| 4  | Container Registry | layerleak, skopeo, docker pull, grep | Active |
| 5  | Metadata SSRF | Custom Python, Azure-Metadata-Enumerator | Active |
| 6  | Google Dorks | GhostLink, DorkGPT, AtDork | Active |
| 7  | Shodan / Censys | Shodan, Censys, OSINT MCP Server | Active |
| 8  | GitHub OSINT | Keychase, pleno-dlp, Gitleaks | Active |
| 9  | Deep Web OSINT | IntelX, Fivecast ONYX | Active |
| 10 | Dark Web OSINT | Robin, OnionClaw, OpenTor | Active |
| 11 | Dark Web Search | Ahmia, Torch, Haystak | Active |
| 12 | Leak & Breach Intel | HIBP, DeHashed, LeakOSINT | Active |
| 13 | Specialized Engines | crt.sh, SecurityTrails, uncover | Active |

## Findings (Real-World Discoveries)

| Target | Secret Found | Status |
|--------|-------------|--------|
| OpenAI (Janhvi-Gangurde) | `sk-proj-...` API Key | Reported |
| Anthropic (raya-ac) | `sk-ant-...` API Key | Acknowledged |
| Groq (Hugging Face Space) | `gsk_...` API Key | Active |
| PostgreSQL (lingxi-core) | `postgres://...` Creds | Pending |
| AI Infrastructure | Blueprint Exposure | Informational |

## Tools & Scripts
- `scripts/dork_runner.py` — CLI utility to generate and open Google Dorks.

## Methodology
- **Passive:** Google Dorks, GitHub OSINT, crt.sh, SecurityTrails.
- **Active:** Shodan, Censys, cloud.sh, layerleak.
- **Elite:** AIMap, OSINT MCP Server, OnionClaw.

## Next Steps
- [ ] Complete all 13 pillars.
- [ ] Automate daily reconnaissance.
- [ ] Integrate with AI agents for continuous monitoring.
