## Firewall Service Exposure Lab

Initial state: Ubuntu VM on bridged network with multiple services reachable.

Action:

* Installed UFW firewall.
* Installed and started Nginx web server.

Control Test:

* SSH accessible on port 2222.
* Web service accessible on port 80.

Exposure Test:

* Nmap detected multiple open ports before firewall rules.
* SSH and HTTP reachable from host.

Mitigation Test:

* Set UFW default deny incoming.
* Allowed only:

  * 2222/tcp (SSH)
  * 80/tcp (HTTP)
* Enabled firewall.

Validation:

* Nmap scan shows only:

  * 2222/tcp open (SSH)
  * 80/tcp open (HTTP)
* All other common ports closed or filtered.

Conclusion:

* Firewall directly controls attack surface.
* Exposing only required services reduces risk.
* Scanning validates firewall effectiveness.
* Secure defaults prevent accidental exposure.

