# Nexa Bug Bounty Framework

AI-powered reconnaissance and pattern-based vulnerability scanner for authorized bug bounty programs.

## Features

- **Recon Engine**: Subdomain enumeration, live host detection, port scanning, URL collection
- **Pattern Engine**: 330+ vulnerability patterns (IDOR, SQLi, XSS, SSRF, LFI, etc.)
- **AI Analysis**: DeepSeek-powered finding verification and severity classification
- **Report Generator**: Markdown + JSON reports with reproduction steps
- **Human-in-the-Loop**: AI assists, human verifies

## What Nexa Does

- Subdomain enumeration (subfinder, amass, assetfinder)
- Live host detection (httpx)
- Port scanning (nmap, naabu)
- URL collection (katana, waybackurls, gau)
- Pattern-based testing (IDOR, SQLi, XSS, SSRF, LFI, etc.)
- AI-powered analysis (DeepSeek)
- Automated report generation

## What Nexa Does NOT Do

- Does NOT find bugs autonomously
- Does NOT create exploits
- Does NOT submit reports
- Does NOT replace human creativity
- Does NOT work without authorization

## Legal Warning

**This tool is for AUTHORIZED bug bounty programs ONLY.**

- Only test on programs you have permission for (HackerOne, Bugcrowd, YesWeHack)
- Never test on random websites
- Respect scope and rate limits
- Follow responsible disclosure

Unauthorized use is illegal under IT Act 2000 (India) and similar laws worldwide.

## Installation

### Prerequisites

- Kali Linux (or any Debian-based distro)
- Python 3.10+
- Go 1.20+ (for tools)

### Step 1: Install System Tools

```bash
sudo apt update
sudo apt install -y python3 python3-pip nmap nikto ffuf

# Install Go tools
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
go install -v github.com/projectdiscovery/katana/cmd/katana@latest
go install -v github.com/projectdiscovery/naabu/v2/cmd/naabu@latest
go install -v github.com/tomnomnom/assetfinder@latest
go install -v github.com/tomnomnom/waybackurls@latest
go install -v github.com/lc/gau/v2/cmd/gau@latest
