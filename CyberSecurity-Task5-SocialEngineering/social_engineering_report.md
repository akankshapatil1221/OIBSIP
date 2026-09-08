# Social Engineering Attacks Report

## Introduction

Social engineering is a type of cyber attack in which an attacker manipulates people into sharing confidential information, performing unsafe actions, or giving access to systems. Instead of directly attacking software, the attacker targets human behaviour such as trust, fear, urgency, curiosity, or helpfulness.

Social engineering is considered highly effective because even strong technical security controls can fail when a user is deceived into revealing a password, opening a malicious attachment, or approving an unauthorised request.
## 1. Phishing

Phishing is a social engineering attack in which an attacker sends a fake email, message, website link, or phone call to trick a victim into sharing sensitive information. The attacker may try to steal usernames, passwords, banking details, OTPs, or company data.

### Types of Phishing

- **Spear phishing:** A targeted phishing attack aimed at a specific person or organisation.
- **Whaling:** A phishing attack that targets senior leaders, executives, or high-value employees.
- **Vishing:** Voice phishing, where attackers use phone calls to trick victims.
- **Smishing:** SMS phishing, where attackers send fraudulent text messages.

### Real-World Case Study

In 2011, RSA Security experienced a spear-phishing attack. Employees received emails with a malicious attachment. After an employee opened the attachment, attackers gained access to internal systems and stole information related to RSA's SecurID authentication products.

### Prevention Recommendations

1. Check the sender's email address and avoid clicking suspicious links or attachments.
2. Verify urgent payment, password-reset, or account-related requests through another trusted channel.
3. Use multi-factor authentication so that a stolen password alone cannot give access.
4. Provide regular phishing-awareness training and phishing simulations for employees.
## 2. Pretexting

Pretexting is a social engineering attack in which an attacker creates a believable false story, called a pretext, to gain a victim's trust. The attacker may pretend to be an IT support employee, bank officer, police officer, HR representative, or vendor.

The attacker uses this false identity to request confidential information, passwords, OTPs, employee records, or access to a system.

### Real-World Case Study

In 2020, attackers used social engineering to target Twitter employees. They contacted employees and convinced them to provide access to internal tools. The attackers then used the tools to take control of high-profile accounts and post cryptocurrency scam messages.

### Prevention Measures

1. Independently verify a caller's or sender's identity before sharing confidential information.
2. Follow a clear approval process for password resets, account changes, and sensitive data requests.
3. Train employees to recognise suspicious requests that create urgency, fear, or pressure.
   
## 3. Baiting

Baiting is a social engineering attack in which an attacker offers something attractive to encourage a victim to take an unsafe action. The bait may be a free download, prize, discount, movie file, job offer, or infected USB drive.

In physical baiting, an attacker may leave an infected USB drive in a public place. A curious person may connect it to a computer, allowing malware to install. In digital baiting, attackers may use fake software downloads, pirated files, or malicious advertisements.

### Real-World Case Study

Security researchers have demonstrated USB-drop attacks by leaving infected USB drives in public locations. Many people connect unknown USB devices to their computers out of curiosity, which can allow malware to spread into an organisation's network.

### Prevention Measures

1. Never connect an unknown USB device to a personal or workplace computer.
2. Download software only from official and trusted websites.
3. Disable automatic USB execution and use endpoint-security software to scan removable media.
## 4. Quid Pro Quo

Quid pro quo means “something for something.” In this attack, an attacker offers a benefit or service in exchange for confidential information or access. For example, an attacker may pretend to be an IT support person and offer to fix a computer problem. In return, they may ask the victim for login credentials or ask them to install remote-access software.

### Prevention Measures

1. Contact the organisation's official IT support team using verified contact details.
2. Never share passwords, OTPs, or multi-factor authentication codes with anyone.
3. Require approval before installing remote-access software or providing system access.
   
   ## Comparison of Social Engineering Attacks

| Attack Type | Primary Target | Psychological Lever Used | Best Countermeasure |
|---|---|---|---|
| Phishing | Email, SMS, and online users | Urgency, fear, and trust | Verify links and use multi-factor authentication |
| Pretexting | Employees and customers | Authority and trust | Verify identity through an independent channel |
| Baiting | Curious users | Curiosity and reward | Do not use unknown USB devices or untrusted downloads |
| Quid Pro Quo | Employees needing help | Helpfulness and exchange | Use only authorised support channels |

## Organisational Recommendations: Employee Security Awareness Checklist

1. Train employees regularly to identify phishing emails, fake links, suspicious attachments, and impersonation attempts.
2. Require employees to verify sensitive requests through a separate trusted channel, such as an official phone number.
3. Enable multi-factor authentication for email, cloud accounts, and important business systems.
4. Create a clear process for reporting suspicious emails, messages, calls, and USB devices to the IT or security team.
5. Conduct safe phishing simulations and use the results to improve employee awareness training.

## Conclusion

Social engineering attacks succeed by exploiting human behaviour rather than only technical weaknesses. Phishing, pretexting, baiting, and quid pro quo attacks can lead to stolen credentials, malware infections, financial loss, and unauthorised access to company systems.

The best defence is a combination of employee awareness, strong authentication, verification procedures, and clear incident-reporting processes.

## References

1. National Institute of Standards and Technology (NIST). *Multi-Factor Authentication.*  
   https://www.nist.gov/itl/smallbusinesscyber/guidance-topic/multi-factor-authentication

2. National Institute of Standards and Technology (NIST). *Cybersecurity Awareness Month: Enabling Multi-Factor Authentication.*  
   https://www.nist.gov/blogs/cybersecurity-insights/cybersecurity-awareness-month-2022-enabling-multi-factor-authentication

3. National Institute of Standards and Technology (NIST). *SP 1800-13: Mobile Application Single Sign-On.*  
   https://www.nccoe.nist.gov/publication/1800-13/VolB/index.html

4. Cybersecurity and Infrastructure Security Agency (CISA). *How to Protect the Data that is Stored on Your Devices.*  
   https://www.cisa.gov/resources-tools/training/how-protect-data-stored-your-devices
