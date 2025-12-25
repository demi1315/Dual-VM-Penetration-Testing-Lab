# Screenshot Reference Guide

All screenshots in this directory were captured during a controlled lab-based penetration test and are provided strictly for documentation and learning purposes.

They demonstrate evidence supporting the findings described in the report.

---

## Windows Target (192.168.2.100)

- **nmap-scan-windows.png**  
  Port and service discovery output identifying SMB and RPC services.

- **ms17-010-success.png**  
  Successful exploitation confirmation of MS17-010 vulnerability.

- **meterpreter-session.png**  
  Meterpreter session established with SYSTEM-level privileges.

- **hashdump-output.png**  
  Extracted NTLM password hashes for analysis.

- **john-cracking.png**  
  Password cracking results using wordlist-based analysis.

- **smb-signing-disabled.png**  
  Evidence of SMB message signing disabled.

- **anonymous-smb.png**  
  Confirmation of anonymous SMB session access.

---

## Linux Target (192.168.2.101)

- **nmap-linux-scan.png**  
  Service enumeration revealing outdated Apache, PHP, and SMB.

- **smb-anon-access.png**  
  Anonymous SMB share access validation.

- **directory-listing.png**  
  Directory indexing enabled on web server.

- **username-disclosure.png**  
  Hardcoded usernames exposed via web source.

- **hydra-bruteforce.png**  
  Password brute-force result for web authentication.

- **authenticated-access.png**  
  Successful authenticated access to protected content.

---

## Notes

- All screenshots were captured from an isolated lab environment.
- No real systems or production data were involved.
- Credentials shown belong to intentionally vulnerable test machines.
