Task 2: Phishing Email Analysis

Objective
Analyze a real-world phishing email to identify suspicious indicators and assess the potential threat.

---

Tools Used

Text Editor: To open `.eml` file

MxToolbox Email Header Analyzer – https://mxtoolbox.com/EmailHeaders.aspx  

IP Lookup Tools: https://ipinfo.io, https://whois.domaintools.com/  

Manual inspection of phishing traits

---

Email Summary

The email appears to be from `shore@suksapan.or.th` offering financial loan services. It requests contact via a Gmail address and includes vague, overly general promises with no personal reference or verification.

---

Phishing Indicators Found

1. Spoofed Sender

- Display name is from an official-sounding domain (`suksapan.or.th`)

- Reply-to is a Gmail address: `globalmeritexperts@gmail.com`

2. Header Failures

- SPF: softfail

- DKIM: none

- DMARC: none

- Origin IP doesn't match sender domain

3. Suspicious Content

- Pushes loan offers

- Unsolicited

- Generic greeting and no customization

- No links, but asks for reply via suspicious email

---

Header Summary

- From: shore@suksapan.or.th  

- Reply-To: globalmeritexperts@gmail.com  

- SPF: softfail  

- DKIM: none  

- DMARC: none  

- X-Originating-IP: 102.69.139.111  

- Email Server: host4.ns.co.th (outside of expected sender range)  

See `header_results.txt` for details.

---

Conclusion

This email clearly demonstrates phishing behavior: a spoofed sender, reply-to redirection, failed SPF/DKIM/DMARC checks, and suspicious content designed to lure victims into a financial scam.

---

Files Included

- `phishing_email.txt` – Extracted email body  

- `header_results.txt` – Summary of technical email headers  

- `README.md` – Task summary and phishing analysis
