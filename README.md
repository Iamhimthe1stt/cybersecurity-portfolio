# Cybersecurity Portfolio

Hi, I'm Victor, an MSc Cybersecurity Technology student at Northumbria University (London Campus). This repo collects my hands-on security work: audits, incident analysis and home lab projects.

**Skills:** Network traffic analysis (Wireshark), vulnerability scanning (Nessus), cloud lab environments (AWS EC2), networking (Cisco Packet Tracer), Python, SQL

## Projects

| Project | What I did | Tools |
|---|---|---|
| [Botium Toys Security Audit](./botium-toys-security-audit) | Reviewed the company's security posture and wrote a recommendation document | Security audit, risk assessment |
| [Network Attack Analysis](./network-attack-analysis) | Analysed a TCP/HTTP capture, identified a SYN flood (DoS) attack and explained its impact on the web server | Wireshark logs, TCP analysis |
| [Home Lab](./home-lab) | Built a lab to scan vulnerable machines and practise networking | Nessus, AWS EC2, Metasploitable, Packet Tracer |

## Highlight: Network Attack Analysis

- **Scenario:** a travel agency's website was timing out for customers.
- **Finding:** the log showed one IP flooding the server with SYN packets and never completing the handshake, exhausting the connection queue.
- **Conclusion:** a TCP SYN flood, a type of DoS attack.
- **Recommendations:** SYN cookies, per-IP rate limiting, IDS/IPS, firewall SYN-flood protection, CDN/DDoS mitigation.

## Contact

- LinkedIn: [victor-okere](https://www.linkedin.com/in/victor-okere-b322b6366)
- Email: okechukwuvictor652@yahoo.com
