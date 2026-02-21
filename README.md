📦 Installation Instructions

```bash
# 1. Install dependencies
pip3 install requests dnspython python-whois

# 2. Download the script
wget https://your-site.com/recon.py
chmod +x recon.py

# 3. Run it
python3 recon.py example.com
python3 recon.py https://example.com -p 80,443,8080 -o results.json
```

---

🚀 Usage Examples

```bash
# Basic recon
python3 recon.py example.com

# Custom ports + save output
python3 recon.py https://target.com -p 22,80,443,3306,8080 -o scan.json

# Skip specific modules
python3 recon.py example.com --no-dns --no-whois

# Increase threads for faster scanning
python3 recon.py example.com -t 50
```

---

📊 Output Format

```json
{
  "target": "example.com",
  "timestamp": "2026-02-21T15:30:00",
  "results": {
    "dns": {
      "A": ["93.184.216.34"],
      "MX": ["10 mail.example.com"]
    },
    "ports": [80, 443],
    "http": {
      "Server": "Apache",
      "Powered-By": "PHP/7.4"
    }
  }
}
```

---

🔧 Features Summary

Module Function
DNS Recon A, AAAA, MX, NS, TXT, SOA, CNAME records
Port Scanner Threaded scanning of common ports
HTTP Recon Headers, technology detection, security checks
SSL/TLS Certificate details, expiration warnings
WHOIS Domain registration information
Subdomain Enum Certificate transparency log scraping

One file. Zero bloat. Professional output. Ready for your site.
