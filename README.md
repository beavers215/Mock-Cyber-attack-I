# Mock-Cyber-attack-I
WebServer-SYN-Flood-Incident-Response


# Web Server SYN Flood Incident Response

## Overview
This repository documents a security incident involving a SYN flood attack targeting the web server of a travel agency. The incident was detected when an automated alert indicated a problem with the web server, leading to a connection timeout error message when attempting to access the company's website. This README provides a detailed account of the incident, including the observed symptoms, analysis process, mitigation measures, and lessons learned.

## Incident Details
- **Affected System**: Web Server
- **Attack Type**: SYN Flood Attack
- **Attacker IP Address**: 203.0.113.0

## Symptoms
- Connection timeout error message when accessing the company's website.
- Abnormal volume of TCP SYN requests observed in Wireshark TCP log.
- Inability to establish or maintain connections to the web server.

## Analysis Process
1. Received user alert indicating a problem with the web server.
2. Attempted to access the company's website, resulting in a connection timeout error message.
3. Utilized Wireshark packet sniffer to capture and analyze data packets in transit to and from the web server.
4. Identified a large number of TCP SYN requests originating from the attacker's IP address (203.0.113.0).
5. Recognized the attack as a SYN flood attack, overwhelming the server's resources and disrupting normal operations.
6. Implemented mitigation measures, including temporarily taking the server offline and configuring the firewall to block the attacker's IP address.

## Mitigation Measures
- Temporarily took the web server offline to allow it to recover and return to normal operating status.
- Configured the company's firewall to block the attacker's IP address (203.0.113.0) to prevent further malicious traffic.
- Recognized the limitations of IP blocking as attackers can easily spoof IP addresses, necessitating additional security measures.

## Lessons Learned
- Importance of proactive monitoring and detection mechanisms to identify security incidents promptly.
- Need for robust security measures, including firewalls and intrusion detection systems, to defend against network attacks.
- Continuous evaluation and improvement of security protocols and incident response procedures to mitigate risks effectively.

## Repository Contents
- Wireshark TCP log files capturing network traffic during the incident.
- Screenshots of error messages and other relevant documentation.
- Analysis reports detailing the incident timeline, findings, and mitigation efforts.

## Recommendations
- Consider implementing rate-limiting measures to mitigate the impact of SYN flood attacks.
- Explore the use of anomaly detection systems to identify and respond to abnormal network behavior.
- Conduct regular security audits and penetration testing to identify and address potential vulnerabilities in the network infrastructure.

