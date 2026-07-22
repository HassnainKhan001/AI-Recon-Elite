# AI Infrastructure Blueprint Exposure (Supply Chain & Architecture Leak)

**Severity:** 🔵 Informational (High Intelligence Value)  
**CVSS Score:** 3.5 (Low, but critical for targeted attacks)  
**Status:** 🔵 Informational (Documented)

---

## 1. Target & Source

| Attribute | Details |
| :--- | :--- |
| **Platform** | GitHub |
| **Repository** | `jbilcke-hf/ai-clip-factory` |
| **Exposed File** | `/.env` |
| **File URL** | `https://github.com/jbilcke-hf/ai-clip-factory/blob/main/.env` |
| **Direct Raw Link** | `https://raw.githubusercontent.com/jbilcke-hf/ai-clip-factory/main/.env` |

---

## 2. Discovery Method (Direct Repository Scan)

**Exact Manual Steps used to find this:**
1. Searched GitHub for AI video generation projects using keywords: `"video" "huggingface" "replicate" -example`.
2. Identified the `jbilcke-hf/ai-clip-factory` repository.
3. Navigated to the root directory and observed the `/.env` file publicly exposed.

---

## 3. Reproducible Proof (Live Verification)

> *"Proof is not what I say. Proof is what the server returns."*

**Step 1:** Access the raw file directly using `curl` (or browser):

```bash
curl https://raw.githubusercontent.com/jbilcke-hf/ai-clip-factory/main/.env
