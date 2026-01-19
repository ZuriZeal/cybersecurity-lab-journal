## Network Scan Lab

Initial state: Ubuntu VM on bridged network with no services exposed.

Action:
- Installed and started OpenSSH server.

Control Test:
- Started SSH service on Ubuntu VM.

- Exposure Test:
- Started SSH service.
- Nmap detected 22/tcp open running SSH.

- Mitigation Test:
- Stopped SSH service.
- Nmap scan shows all 1000 common ports closed.

Validation:
- Nmap scan shows 22/tcp open running OpenSSH 8.9p1.

Conclusion:
- Services directly change attack surface.
- Reducing running services reduces exposure.
- Scanning validates security posture.
