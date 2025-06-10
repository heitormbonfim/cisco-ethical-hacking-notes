# Notes

## Introduction

This document outlines key details for my fictional company and its current client.

1.  **Fictional Company:**

    - Protego Security Solutions

2.  **Client(s):**

    - Pixel Paradise

3.  **Objective of this module**

    - Explain the importance of Ethical Hacking
    - Build your own Hakcing Lab

4.  **Most Common Certifications**
    Answers will vary. The ISACA Certified Information Systems Auditor (CISA) and Certified Information Security Manager (CISM) certifications are often mentioned. The (ISC)2 Certified Information Systems Security Professional CISSP exam is also mentioned frequently. (Note that the (ISC)2 also offers Certified in Cybersecurity (CC) certification for entry-level job candidates). The GIAC Security Essentials (GSEC) certification is also suitable for entry-level positions. Furthermore, the CompTIA PenTest+ and Security+ exams are mentioned. Also relevant are the Cisco CCNP and CCIE Security certfications. Finally, the EC-Council offers the Certified Ethical Hacker (CEH).

## Network Infrastructure Tests

This often includes the switches, routers, firewalls, and supporting resources, such as authentication, authorization, and accounting (AAA) servers and IPSs. A penetration test on wireless infrastructure may sometimes be included in the scope of a network infrastructure test. However, additional types of tests beyond a wired network assessment would be performed. For instance, a wireless security tester would attempt to break into a network via the wireless network either by bypassing security mechanisms or breaking the cryptographic methods used to secure the traffic. Testing the wireless infrastructure helps an organization to determine weaknesses in the wireless deployment as well as the exposure. It often includes a detailed heat map of the signal disbursement.

## Application-Based Tests

This type of pen testing focuses on testing for security weaknesses in enterprise applications. These weaknesses can include but are not limited to misconfigurations, input validation issues, injection issues, and logic flaws. Because a web application is typically built on a web server with a back-end database, the testing scope normally includes the database as well. However, it focuses on gaining access to that supporting database through the web application compromise. A great resource is the Open Web Application Security Project (OWASP).

## Penetration Testing in the Cloud

Cloud service providers (CSPs) such as Azure, Amazon Web Services (AWS), and Google Cloud Platform (GCP) have no choice but to take their security and compliance responsibilities very seriously. For instance, Amazon created the Shared Responsibility Model to describe the AWS customers’ responsibilities and Amazon’s responsibilities in detail (see https://aws.amazon.com/compliance/shared-responsibility-model).

The responsibility for cloud security depends on the type of cloud model (software as a service [SaaS], platform as a service [PaaS], or infrastructure as a service [IaaS]). For example, with IaaS, the customer (cloud consumer) is responsible for data, applications, runtime, middleware, virtual machines (VMs), containers, and operating systems in VMs. Regardless of the model used, cloud security is the responsibility of both the client and the cloud provider. These details need to be worked out before a cloud computing contract is signed. These contracts vary depending on the security requirements of the client. Considerations include disaster recovery, service-level agreements (SLAs), data integrity, and encryption. For example, is encryption provided end to end or just at the cloud provider? Also, who manages the encryption keys–the CSP or the client?

Overall, you want to ensure that the CSP has the same layers of security (logical, physical, and administrative) in place that you would have for services you control. When performing penetration testing in the cloud, you must understand what you can do and what you cannot do. Most CSPs have detailed guidelines on how to perform security assessments and penetration testing in the cloud. Regardless, there are many potential threats when organizations move to a cloud model. For example, although your data is in the cloud, it must reside in a physical location somewhere. Your cloud provider should agree in writing to provide the level of security required for your customers. As an example, the following link includes the AWS Customer Support Policy for Penetration Testing: https://aws.amazon.com/security/penetration-testing.

### Note

Many penetration testers find the physical aspect of testing to be the most fun because they are essentially being paid to break into the facility of a target. This type of test can help expose any weaknesses in the physical perimeter as well as any security mechanisms that are in place, such as guards, gates, and fencing. The result should be an assessment of the external physical security controls. The majority of compromises today start with some kind of social engineering attack. This could be a phone call, an email, a website, an SMS message, and so on. It is important to test how your employees handle these types of situations. This type of test is often omitted from the scope of a penetration testing engagement mainly because it primarily involves testing people instead of the technology. In most cases, management does not agree with this type of approach. However, it is important to get a real-world view of the latest attack methods. The result of a social engineering test should be to assess the security awareness program so that you can enhance it. It should not be to identify individuals who fail the test. One of the tools that we talk about more in a later module is the Social-Engineer Toolkit (SET), created by Dave Kennedy. This is a great tool for performing social engineering testing campaigns.

#### TIP

Bug bounty programs enable security researchers and penetration testers to get recognition (and often monetary compensation) for finding vulnerabilities in websites, applications, or any other types of systems. Companies like Microsoft, Apple, and Cisco and even government institutions such as the U.S. Department of Defense (DoD) use bug bounty programs to reward security professionals when they find vulnerabilities in their systems. Many security companies, such as HackerOne, Bugcrowd, Intigriti, and SynAck, provide platforms for businesses and security professionals to participate in bug bounty programs. These programs are different from traditional penetration testing engagements but have a similar goal: finding security vulnerabilities to allow the organization to fix them before malicious attackers are able to exploit such vulnerabilities. I have included different bug bounty tips and resources in my GitHub repository at: https://github.com/The-Art-of-Hacking/h4cker/tree/master/bug-bounties.

## Surveying Different Standards and Methodologies

There are a number of penetration testing methodologies that have been around for a while and continue to be updated as new threats emerge.

The following is a list of some of the most common penetration testing methodologies and other standards:

- The MITRE ATT&CK framework (https://attack.mitre.org) is an amazing resource for learning about an adversary’s tactics, techniques, and procedures (TTPs). Both offensive security professionals (penetration testers, red teamers, bug hunters, and so on) and incident responders and threat hunting teams use the MITRE ATT&CK framework today. The MITRE ATT&CK framework is a collection of different matrices of tactics, techniques, and subtechniques. These matrices–including the Enterprise ATT&CK Matrix, Network, Cloud, ICS, and Mobile–list the tactics and techniques that adversaries use while preparing for an attack, including gathering of information (open-source intelligence [OSINT], technical and people weakness identification, and more) as well as different exploitation and post-exploitation techniques. You will learn more about MITRE ATT&CK throughout this course.

- The OWASP Web Security Testing Guide (WSTG) is a comprehensive guide focused on web application testing. It is a compilation of many years of work by OWASP members. OWASP WSTG covers the high-level phases of web application security testing and digs deeper into the testing methods used. For instance, it goes as far as providing attack vectors for testing cross-site scripting (XSS), XML external entity (XXE) attacks, cross-site request forgery (CSRF), and SQL injection attacks; as well as how to prevent and mitigate these attacks. You will learn more about these attacks in Module 6, “Exploiting Application-Based Vulnerabilities.” From a web application security testing perspective, OWASP WSTG is the most detailed and comprehensive guide available. You can find the OWASP WSTG and related project information at https://owasp.org/www-project-web-security-testing-guide/.

- Special Publication (SP) 800-115 is a document created by the National Institute of Standards and Technology (NIST), which is part of the U.S. Department of Commerce. NIST SP 800-115 provides organizations with guidelines on planning and conducting information security testing. It superseded the previous standard document, SP 800-42. SP 800-115 is considered an industry standard for penetration testing guidance and is called out in many other industry standards and documents. You can access NIST SP 800-115 at https://csrc.nist.gov/publications/detail/sp/800-115/final.

- The Open Source Security Testing Methodology Manual (OSSTMM), developed by Pete Herzog, has been around a long time. Distributed by the Institute for Security and Open Methodologies (ISECOM), the OSSTMM is a document that lays out repeatable and consistent security testing (https://www.isecom.org). It is currently in version 3, and version 4 is in draft status. The OSSTMM has the following key sections:

  - Operational Security Metrics
  - Trust Analysis
  - Work Flow
  - Human Security Testing
  - Physical Security Testing
  - Wireless Security Testing
  - Telecommunications Security Testing
  - Data Networks Security Testing
  - Compliance Regulations
  - Reporting with the Security Test Audit Report (STAR)

- The Penetration Testing Execution Standard (PTES) (http://www.pentest-standard.org) provides information about types of attacks and methods, and it provides information on the latest tools available to accomplish the testing methods outlined. PTES involves seven distinct phases:

  1. Pre-engagement interactions
  2. Intelligence gathering
  3. Threat modeling
  4. Vulnerability analysis
  5. Exploitation
  6. Post-exploitation
  7. Reporting

- The Information Systems Security Assessment Framework (ISSAF) is another penetration testing methodology similar to the others on this list with some additional phases. ISSAF covers the following phases:

  - Information gathering
  - Network mapping
  - Vulnerability identification
  - Penetration
  - Gaining access and privilege escalation
  - Enumerating further
  - Compromising remote users/sites
  - Maintaining access
  - Covering the tracks

--

## Active Recall

- What is an Ethical Hacker?
- .. NIST Computer Security Resource Center (CSRC)?
- .. Organization defines a hacker as a user that attempts or gains unauthorized
  acess to an information system?
- .. organization hackingisnotacrime.org is responsible for?
- .. organization is a good reference for cybersecurity job role is?
- .. NICCS Cyber Career Pathways Tool?i
- .. Hacktivist?
- .. Organized Crimes?
- .. State-Sponsered Attack?
- .. Insider threats?
- .. black-box, gray-box and white-box?
- .. unkown environment, partially known environment, known-environment?
- ..
