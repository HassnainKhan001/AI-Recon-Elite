# Unauthenticated Ollama / vLLM Inference Server Exposure (Oracle Cloud)

**Report ID:** `AI-RECON-2026-007`  
**Severity:** 🔴 Critical (CVSS v3.1: 7.5)  
**Date of Discovery:** July 22, 2026  
**Researcher:** Muhammad Hasnain

---

## 1. Executive Summary

An unauthenticated Ollama (vLLM compatible) inference server was discovered on Oracle Cloud infrastructure (`ai.531049.xyz` / `79.72.87.190`). The server is fully exposed to the public internet and allows arbitrary AI model execution without any API key, authentication, or rate limiting. 

**Impact:** This vulnerability enables **unlimited financial theft** (GPU billing abuse), **Denial of Service (DoS)**, and **potential model exfiltration**.

**Status:** Actively exploitable at the time of discovery. Reported to Oracle Abuse Team (`abuse@oracleemaildelivery.com`) on July 22, 2026.

---

## 2. Target Profile

| Field | Details |
| :--- | :--- |
| **Hostname** | `ai.531049.xyz` |
| **IP Address** | `79.72.87.190` |
| **Hosting Provider** | Oracle Svenska AB |
| **Technology** | Ollama / vLLM (OpenAI-compatible API) |
| **Exposed Model** | `qwen2.5-coder:1.5b` |
| **Ports** | 443 (HTTPS - Exposed) |

---

## 3. Discovery Methodology

- **Initial Discovery:** Shodan search using query `port:443 "Ollama"` identified the host.
- **Service Fingerprinting:** Manual probing of standard endpoints (`/v1/models`, `/api/tags`) confirmed the presence of an OpenAI-compatible inference engine.
- **Authentication Check:** All endpoints returned `200 OK` without requiring any `Authorization` header, confirming zero authentication.

---

## 4. Forensic Proof of Concept (Live Verification)

All commands listed below were executed against the live target and verified.

### A. Model Enumeration (Identifying Exploitable Assets)

The server exposed its available machine learning models without any credential check.

**Request:**
```bash
curl -v -X GET https://ai.531049.xyz/v1/models
