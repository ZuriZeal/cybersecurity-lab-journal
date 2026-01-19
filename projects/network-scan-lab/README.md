## Network Scan Lab

Initial state: Ubuntu VM on bridged network with no services exposed.

Action:
- Installed and started OpenSSH server.

Validation:
- Nmap scan from host shows:
  - 22/tcp open (ssh)
  - All other ports closed or filtered

Conclusion:
- System exposes only required service, reducing attack surface and limiting lateral attack options.
