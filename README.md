===== CAP 5150 – Network Protocol Analysis Artifacts =====

This repository contains all packet captures and configuration files used in the CAP 5150 Final Project titled **“Network Security Protocols in Government Testing Environments.”** These artifacts correspond directly to the experiments described in the report, including TLS certificate expiration, SSH authentication testing, IPsec tunnel setup, and rekey behavior.

===== Repository Structure =====

configs/

mgmt/

sshd_config.mgmt # SSH server config used during misconfiguration test
default-ssl.conf # Apache TLS vhost using the expired certificate
ipsec.conf.mgmt # StrongSwan IPsec configuration for mgmt-node
ipsec.secrets.mgmt # Pre-shared key used for IPsec testing

gateway/

ipsec.conf.gateway # StrongSwan IPsec configuration for gateway-node
ipsec.secrets.gateway # Pre-shared key for gateway-node

pcaps/

expired_tls/ # TLS handshake showing expired certificate behavior
ssh_misconfig/ # SSH password-authentication session packets
ipsec_rekey/ # IKE/ESP packets during IPsec rekey event
internal_traffic/ # Baseline enclave traffic used for verification
second_test/ # Additional captures taken during evaluations

screenshots/

All screenshots used in the final report, included for clarity and accessibility.

===== Purpose =====

These artifacts support the evaluation of:

- TLS certificate validation and expiration behavior  
- SSH authentication policy (key vs password)  
- IPsec tunnel establishment and rekeying  
- Monitoring visibility using tcpdump and Wireshark  
- Zero Trust alignment and NIST SP 800-53 control mappings  

Each file in this repository is referenced in the final report’s **Methodology** and **Evaluation & Results** sections.

===== Usage =====

1. Clone the repository

2. Open any `.pcap` file in Wireshark.

3. Review configuration files to understand protocol behavior, policy changes, and rekey events.

===== Author =====

Mariano Ortiz  
University of Central Florida  
CAP 5150 – Fall 2025
