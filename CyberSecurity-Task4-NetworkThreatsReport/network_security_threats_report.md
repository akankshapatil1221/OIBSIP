# Common Network Security Threats

## Introduction

Network security threats are attacks that target computers, devices, servers, and data connected through a network. These threats can cause data theft, service disruption, financial loss, and damage to an organisation’s reputation. As businesses increasingly depend on online systems, understanding common threats and applying proper security controls has become essential for every network administrator.

## 1. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) Attacks

A Denial-of-Service (DoS) attack attempts to make a website, server, or network unavailable to genuine users. The attacker sends an extremely high number of requests or uses malicious traffic to consume the target’s bandwidth, processing power, or memory.

A Distributed Denial-of-Service (DDoS) attack is more powerful because it uses many compromised devices, called a botnet, to send traffic to one target at the same time. This makes the attack harder to stop because the traffic comes from many different IP addresses.

### Real-World Example

In 2016, the Mirai botnet launched a large DDoS attack against Dyn, a DNS service provider. This disrupted access to popular websites and online services. The attack showed how insecure IoT devices, such as cameras and routers, can be used to create a botnet.

### Impact

- Websites and online services may become unavailable.
- Businesses can lose customers, revenue, and user trust.
- Security teams may spend significant time and money restoring services.

### Mitigation Strategies

1. Use DDoS protection services and Content Delivery Networks (CDNs) to absorb malicious traffic.
2. Apply rate limiting and firewall rules to block unusual or excessive requests.
3. Monitor network traffic continuously and maintain an incident response plan.

## 2. Man-in-the-Middle (MITM) Attacks

A Man-in-the-Middle (MITM) attack happens when an attacker secretly intercepts communication between two parties, such as a user and a website. The attacker may read, change, or steal the information being exchanged without either party knowing.

MITM attacks are common on insecure public Wi-Fi networks. For example, an attacker may create a fake Wi-Fi hotspot with a name similar to a café or airport network. When a user connects, the attacker can try to capture unencrypted traffic.

### Real-World Example

In 2015, Lenovo’s pre-installed Superfish software created a serious security risk. It installed a weak certificate on users’ computers, which could allow attackers to intercept encrypted HTTPS communication. This demonstrated how poor certificate handling can enable MITM-style attacks.

### Impact

- Usernames, passwords, banking details, and personal data can be stolen.
- Attackers can modify information sent between a user and a website.
- Organisations can suffer privacy breaches and reputational damage.

### Mitigation Strategies

1. Use HTTPS websites and verify that browser certificate warnings are never ignored.
2. Avoid entering sensitive information on public Wi-Fi; use a trusted VPN when necessary.
3. Use secure Wi-Fi encryption, strong passwords, and certificate validation.

## 3. IP Spoofing

IP spoofing is an attack in which an attacker changes the source IP address in network packets so that the packets appear to come from a trusted device or network. The attacker uses this technique to hide their identity, bypass basic IP-based trust rules, or support other attacks such as DDoS attacks.

IP spoofing does not always allow an attacker to receive responses because the reply normally goes to the real IP address. However, it can still be dangerous when systems trust traffic only because it appears to come from an internal or approved IP address.

### Real-World Example

In the 1990s, an attacker named Kevin Mitnick used IP spoofing techniques to exploit trust relationships between computer systems. This case showed that relying only on IP addresses for authentication is not secure.

### Impact

- Attackers can hide the true origin of malicious traffic.
- Networks that trust specific IP addresses can be accessed or attacked.
- IP spoofing can be used in DDoS attacks to make filtering more difficult.

### Mitigation Strategies

1. Configure ingress and egress filtering so that routers block packets with fake source addresses.
2. Do not rely only on IP addresses for authentication; use multi-factor authentication and secure credentials.
3. Monitor network logs and use intrusion detection systems to identify unusual or spoofed traffic.

## 4. DNS Poisoning and DNS Spoofing

DNS stands for Domain Name System. It converts a website name, such as `example.com`, into an IP address that computers use to connect. DNS poisoning or DNS spoofing happens when an attacker gives a victim a false DNS response and redirects them to a malicious IP address or fake website.

For example, a user may type the correct banking website address but be sent to a fake page that looks real. The attacker can then steal login credentials or financial information.

### Real-World Example

In 2008, security researcher Dan Kaminsky discovered a major DNS cache poisoning vulnerability. The weakness could allow attackers to send fake DNS records and redirect users to malicious websites. Many organisations released emergency patches to reduce the risk.

### Impact

- Users can be redirected to fake websites without noticing.
- Login credentials, payment information, and personal data can be stolen.
- Organisations may lose customer trust if their domain is abused.

### Mitigation Strategies

1. Use DNSSEC to validate DNS responses and reduce the risk of forged records.
2. Keep DNS servers updated and apply security patches quickly.
3. Monitor DNS records and use trusted DNS resolvers with security protections.

## Comparison of Common Network Security Threats

| Threat | Attack Vector | Who Is at Risk? | Difficulty to Execute | Ease of Mitigation |
|---|---|---|---|---|
| DoS/DDoS | Excessive malicious traffic sent to a server or network | Websites, online services, and businesses | Medium to High | Medium |
| MITM | Intercepting communication between a user and a service | Users on insecure networks and organisations | Medium | Medium |
| IP Spoofing | Sending packets with a forged source IP address | Networks using IP-based trust rules | Medium | Medium |
| DNS Poisoning | Sending fake DNS responses or changing DNS records | Internet users, organisations, and domain owners | High | Medium |


## Conclusion

Network security threats can affect every organisation that uses computers, websites, cloud services, or online communication. DoS/DDoS attacks can stop services, MITM attacks can steal or change data, IP spoofing can hide malicious traffic, and DNS poisoning can redirect users to fake websites.

Three important takeaways for a network administrator are:

1. Monitor network traffic regularly to detect unusual activity early.
2. Keep systems, firewalls, DNS servers, and security tools properly configured and updated.
3. Use layered security controls, including HTTPS, strong authentication, traffic filtering, and an incident response plan.

## References

1. National Institute of Standards and Technology (NIST). *Resilient Interdomain Traffic Exchange: BGP Security and DDoS Mitigation (SP 800-189).*  
   https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-189.pdf

2. National Institute of Standards and Technology (NIST). *Advanced DDoS Mitigation Techniques.*  
   https://www.nist.gov/programs-projects/advanced-ddos-mitigation-techniques

3. Cybersecurity and Infrastructure Security Agency (CISA). *Best Practices for Using Public Wi-Fi.*  
   https://www.cisa.gov/sites/default/files/publications/Best%20Practices%20for%20Using%20Public%20WiFi.pdf

4. National Institute of Standards and Technology (NIST). *Secure Domain Name System (DNS) Deployment Guide, SP 800-81 Rev. 3.*  
   https://csrc.nist.gov/pubs/sp/800/81/r3/final

