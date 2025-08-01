# Cloud Security Posture Management (CSPM) in Depth

## Introduction

Cloud security posture management (CSPM) is an umbrella term for the practices and tools available to strengthen and enforce strong security management in an organization. There are several mitigating strategies a cybersecurity analyst can take to protect company assets.

This reading continues the conversation on the implementation of CSPM, expanding on additional considerations like risk detection, the mitigation of shadow IT, and the role of technical policy in averting security lapses.

---

## Discover Risks

An IT cyber specialist’s role involves knowing if the company's intellectual property has been compromised. This can be observed in many areas, like automatically scanning YouTube videos for copyright infringement or scanning the dark web for data breaches.

One aspect of this role involves the creation of banned password lists. Additionally, it encompasses the surveillance of Shadow IT, which refers to the use of devices or applications that have not been sanctioned or approved by the IT department.

For example, consider a scenario where a coder employs a public linting service—a tool designed to enhance the quality of code by automatically checking for potential errors, coding style violations, and other issues. In this case, the company's code is submitted to a third-party service for thorough analysis and optimization. Another instance arises when developers collaborate on company code using a public GitHub repository.

Discovering risks involves identifying the intentional and unintentional threats that may arise due to the actions of an uninformed or careless employee.

---

## Technical Policy

Technical policy relates to the standards and best practices the company has enacted. It plays a crucial role in addressing issues like Shadow IT, which involves the use of unauthorized devices and applications inappropriate for handling company data.

For employees to know what is permissible, there needs to be a centralized document outlining company best practices and standards. This includes implementing guardrails that prevent an employee from performing certain behaviors. For example, a policy might be enacted to prevent the copying or deleting of sensitive information. It could also include scanning employee devices and preventing access to devices considered unhealthy for the system.

An integral part of this concept is the practice of constantly auditing and reviewing company standards, employee actions, the current state of cybersecurity, and the degree to which company information has been protected to date.

---

## Minimizing Risks: A Holistic Security Posture

In understanding the principles of a robust security posture, the primary goal is to minimize risks to the system. This involves mitigating the potential harm a breach can cause and reducing the return on investment for a hacker attempting unauthorized access.

Consider the lesson on encryption: by storing an encrypted version of the hash of a password, any hacker who breaches the system only receives a minimum return on the effort taken if they cannot decrypt the passwords. This can act as a deterrent to prevent any attempt at a breach. For more sensitive information, Azure services can encrypt the data further—encrypting it while it is in transit, and even as the operating system processes it.

---

## CSPM in Different Departments

It is worth noting that cloud security posture management is not confined to the cybersecurity department. It should be a holistic approach embraced universally in the organization.

- **Threat Intelligence Team:** Uses CSPM to continuously assess the security posture of cloud environments and identify potential misconfigurations or vulnerabilities that attackers might exploit.
- **Information Technology (IT):** Leverages CSPM to automate security checks, ensuring that cloud resources are properly configured and compliant with security policies.
- **Compliance and Risk Management Teams:** Use CSPM to monitor and enforce cloud security controls, ensuring adherence to regulatory requirements and reducing the risk of data breaches.
- **Business Leaders and SMEs (Subject Matter Experts):** Utilize CSPM to gain visibility into the security status of their cloud assets, enabling informed decision-making and risk mitigation.
- **Security Architecture and Operations:** Deploy CSPM to detect security issues in real-time, enabling proactive responses to potential threats and ensuring a well-protected cloud environment.
- **Audit Team:** Employs CSPM as an assessment tool to evaluate the security posture of cloud resources and track compliance with security policies and best practices.

---

## Security Tools

Now, let's explore the tools employed to ensure security:

- **Microsoft Defender:** Provides governance features, regulatory compliance verification, and cloud security explorer. Manages permissions and provides attack analysis.
- **Azure Security Center:** Employee monitoring, threat assessment, and security recommendations.
- **Microsoft Sentinel:** Collects security data, collates them to identify potential attack patterns, and provides forensics in the aftermath of a breach.
- **Azure Monitor:** Presents and projects telemetry data from other services, allowing greater insight into the actions happening in your cloud environment.
- **Azure Bastion:** Wraps your SSH (Secure Shell) and RDP (Remote Desktop Protocol) ports behind a security buffer to minimize the attack surface available to hackers.

---

## Conclusion

CSPM is a dynamic and collaborative approach that involves every facet of an organization, from technical specialists to business leaders. By integrating these practices and tools, organizations can fortify their security posture and effectively mitigate emerging threats.