# wealthmatica.com DNS manifest (pre-Cloudflare snapshot, 2026-09-03)

Every record that must exist in Cloudflare after import. Verify each one before switching nameservers.

| Type | Name | Value | Notes |
|------|------|-------|-------|
| A | @ | 185.199.108.153 | GitHub Pages |
| A | @ | 185.199.109.153 | GitHub Pages |
| A | @ | 185.199.110.153 | GitHub Pages |
| A | @ | 185.199.111.153 | GitHub Pages |
| CNAME | www | nick-wealthmatica.github.io | GitHub Pages |
| MX | @ | smtp.google.com (priority 1) | Google Workspace email - CRITICAL |
| TXT | @ | v=spf1 include:_spf.google.com ~all | Email anti-spoofing - CRITICAL |
| TXT | google._domainkey | v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8A... (long key) | Email signing - CRITICAL |

No AAAA, no CAA, no _dmarc records existed at snapshot time.

Cloudflare settings after import:
- A @ records and CNAME www: proxy ON (orange cloud)
- MX and TXT records: DNS only (no proxy option anyway)
- SSL/TLS mode: Full (NOT Full-strict, and NOT Flexible)
- Always Use HTTPS: ON
