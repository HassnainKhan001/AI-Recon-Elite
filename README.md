<p align="center">
  <img src="https://img.shields.io/badge/Status-Elite_Recon-purple?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Version-Static_1.0-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/2026-Updated-brightgreen?style=for-the-badge" />
</p>

# 🛡️ AI Recon Elite

> **Professional Offensive Reconnaissance Framework for AI & Cloud Infrastructure (2026)**

**Mission:** Provide a structured, repeatable, and elite-level methodology for discovering exposed assets and secrets in AI ecosystems.  
**Scope:** Pure OSINT, Subdomain Enumeration, Secret Hunting, and Attack Surface Mapping.  
**Rule:** `No Exploitation. No Jailbreaks. Pure Recon.`  
**Commitment:** This README is a **static template**. It will **never** be edited again. All future findings go into their respective pillar folders.

---

## 📚 The 13 Pillars of Recon (2026)

| # | Category | Primary Tools | Objective |
| :---: | :--- | :--- | :--- |
| 01 | **Subdomain Enumeration** | HaXder, BBOT, Amass, Subfinder | Discover all live subdomains and hidden entry points. |
| 02 | **Cloud Bucket Hunting** | s3dns, cloud.sh, Gobuster | Identify public S3, GCS, and Azure storage leaks. |
| 03 | **Service Fingerprinting** | AIMap, httpx, KBF | Fingerprint AI endpoints (vLLM, MCP, Ollama). |
| 04 | **Container Registry** | layerleak, skopeo, grep | Scrape Docker/OCI images for hardcoded secrets. |
| 05 | **Metadata SSRF** | Python Scripts, Metasploit | Exploit IMDS (169.254.169.254) for IAM credentials. |
| 06 | **Google Dorks** | GhostLink, AtDork | Hunt for exposed `.env`, API keys, and configs. |
| 07 | **Shodan / Censys** | OSINT MCP Server, Barz Cve Hunter | Scan internet-facing devices and vulnerable services. |
| 08 | **GitHub OSINT** | Keychase, pleno-dlp, Gitleaks | Source code secrets (tokens, keys, passwords). |
| 09 | **Deep Web OSINT** | IntelX, Fivecast ONYX | Access unindexed academic, paywalled, and archived data. |
| 10 | **Dark Web OSINT** | Robin, OnionClaw, OpenTor | Monitor Tor hidden services, forums, and ransomware leaks. |
| 11 | **Dark Web Search** | Ahmia, Torch, Haystak | Query .onion sites and dark web marketplaces. |
| 12 | **Leak & Breach Intel** | HIBP, DeHashed, LeakOSINT | Verify credential exposures in public breaches. |
| 13 | **Specialized Engines** | crt.sh, uncover, SecurityTrails | Passive DNS, CT logs, and historical internet data. |

---

## 🧠 The Dynamic Findings Structure (Consistency Rule)

To keep this README **permanently static**:

1.  **Never hardcode findings here.** This is a template, not a log.
2.  All findings go into **`/findings/master-log.md`**.
3.  Each pillar folder contains its own `tools.md` and `findings.md` for granular tracking.
4.  When you discover a new secret, you update the specific `findings.md` file inside that pillar folder. The master index updates automatically via the structure.

---

## 🛠️ Tool Stack (2026 Updates)

| Tool | Version/Note | Primary Use |
| :--- | :--- | :--- |
| **HaXder** | Async Recon | Subdomains + Cloud Storage in one sweep. |
| **BBOT** | Recursive Scanner | 20-50% more subdomains. |
| **AIMap** | AI Infrastructure | Fingerprints MCP, vLLM, Ollama, LangServe. |
| **layerleak** | OCI Registry | Scans any Docker Hub, GHCR, Quay, ECR, GCR. |
| **OSINT MCP Server** | Unified 37-in-1 | Shodan + Censys + VirusTotal + SecurityTrails. |
| **Robin** | AI OSINT | LLM-powered dark web query refinement. |
| **Keychase** | 78 Detectors | Zero-config GitHub secret scanning. |

---

## 📝 Professional Usage Disclaimer

> **This repository is strictly for educational purposes and authorized bug bounty/reconnaissance engagements.**  
> *Do not scan, probe, or test systems you do not own or lack explicit written permission to test. Unauthorized access is illegal.*

---

## 🔗 Quick Links

- **GitHub Home:** [https://github.com/HassnainKhan001]
-  **Linkdln Home:** [https://www.linkedin.com/in/muhammad-hasnain-28840b382/]
- **Last Updated:** July 2026

---

*"Recon isn't about finding everything. It's about finding the *right* thing that everyone else missed."*
