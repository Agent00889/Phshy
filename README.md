# 🛡️ Phishing URL Detector

A lightweight, blazing-fast, client-side threat intelligence tool that analyzes URLs for common phishing indicators, brand spoofing attempts, and structural anomalies. Built entirely with standard modern web technologies, it runs 20 heuristic detection rules instantly in the browser without relying on external APIs.

![Phishing Detector Interface](https://img.shields.io/badge/Security-Heuristic_Analysis-00e5a0?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-HTML5_/_CSS3_/_JS-00b37d?style=for-the-badge)

---

## 🚀 Features

* **20 Automated Security Checks:** Evaluates URLs against heuristic vectors including protocol validity, domain reputation, TLD risk profiles, character encoding, and entropy metrics.
* **Brand Spoofing Detection:** Catches sophisticated lookalike domains targeting popular tech giants and financial institutions (e.g., `paypal-secure-login.tk`).
* **Shannon Entropy Calculation:** Computes the random distribution of strings in the domain name to detect dynamically generated or algorithmic (DGA) malicious landing pages.
* **Visual Risk Stratification:** Dynamically calculates a quantitative risk score and categorizes results into real-time tiers: `LIKELY SAFE`, `LOW RISK`, `SUSPICIOUS`, `HIGH RISK`, or `LIKELY PHISHING`.
* **Session History Persistence:** Remembers your last 5 scanned inputs for easy switching and comprehensive tracking during rapid assessments.
* **Zero External Dependencies:** Built with pure vanilla HTML5, CSS3, and modern JavaScript. Zero risk of tracking or data exposure—your scanned URLs never leave your browser.

---

## 🛠️ Heuristic Analysis Engine Breakdown

The detector uses a weight-based scoring framework ($+X$ or $-X$ risk points) across multiple vectors:

### 1. Structure & Identity
* **Deep Subdomain Nesting:** Flags URLs utilizing excessively deep nesting layers (e.g., `a.b.c.evil.com`) designed to hide the actual domain suffix on mobile browsers.
* **IP Address Hostnames:** Detects raw IPv4 addressing used bypass standard domain name blacklists.
* **Excessive Hyphenation:** Flags multiple consecutive or scattered hyphens, typically associated with fake service mimicking (e.g., `secure-update-alert`).

### 2. Content & Obfuscation
* **Shannon Entropy Check:** High string unpredictability scores ($> 3.8$) indicate high likelihood of automated gibberish names.
* **Percent Encoding:** Analyzes heavy usage of hex-encoded parameters (`%20`, `%F3`) used to conceal payloads from plain sight.
* **Suspicious Keyword Matching:** Scans paths and strings for high-frequency social engineering targets like `login`, `otp`, `verify`, and `credential`.

---

## 💻 Tech Stack

* **Markup:** HTML5 semantic layout.
* **Styling:** Responsive CSS3 featuring custom properties (variables), Flexbox, CSS Grid layouts, and custom animations optimized for smooth 60fps renders.
* **Fonts:** Interfaced via Google Fonts (`Space Mono` and `DM Sans`).
* **Logic Engine:** Pure Vanilla JavaScript (ECMAScript 6+ structures like `Set`, mapping arrays, string metrics, and simulated async UI loaders).

---

## 📂 Quick Start & Installation

Because the application runs entirely client-side, setup takes under 10 seconds:

1. Clone or download this repository to your machine:
   ```bash
   git clone [https://github.com/yourusername/phishing-url-detector.git](https://github.com/yourusername/phishing-url-detector.git)
