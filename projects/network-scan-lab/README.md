## Network Scan Lab

Initial state: Ubuntu VM on bridged network with no services exposed.

Action:
- Installed and started OpenSSH server.

Control Test:
- Started SSH service on Ubuntu VM.

Validation:
- Nmap scan shows 22/tcp open running OpenSSH 8.9p1.

Conclusion:
- Enabling services directly increases attack surface.
- Service detection reveals software versions that attackers could target.
