
![](https://github.com/anrjustin9/The-Open-Apiary-Framework/raw/main/Apiary%20Framework%20Logo2.png)

------------

# **The Open Apiary Framework v0.9**
The Apiary Framework aims to provide a structured approach to the deployment and management of honeypots on a network to achieve the overall goal of increasing the likelihood of detecting a threat. A structured approach is important as it provides organizations with a consistent way of implementing honeypots with clear detection benefits while not reducing the overall security of the environment.

The framework is divided into the following components:
1. **The HoneyPot Definition:** describes what a HoneyPot is and the characteristics of the same.
2. **The Apiary Maturity Model:** A descriptive model of the stages through which an organization progresses as they define, implement, evolve and improve their HoneyPot strategy.
3. **The HoneyPots:** this component of the framework describes the various types of Honeypots which can be deployed, the approach in which it can be deployed, the detection benefits, and the security considerations. 

## Defining the HoneyPot
There are several characteristics which can be attributed to the Honeypot:

1. **Enticement:** Enticement is the name of the game and one of the key characteristics of the Honeypot which makes it attractive to attackers. There is a delicate balance between being too enticing, which can inadvertently alert attackers to the presence of a honeypot, and being unenticing, which can lead attackers to not notice nor consider this system in their attack. In general, the Honeypot should “look” like a key critical asset, or the keys to one, while not serving any purpose to the business as to reduce the “noise” generated during its monitoring. While looking like an easy target, a balance must also be struck with being secure.
3. **Security:** While being enticing, a honeypot should not reduce the overall security of the environment. This means that the honeypot should be secured to a reasonable extent that compromise of it does not mean compromise of wider segments of the network nor the organization’s critical assets.
5. **Recoverable:** Honeypots are meant to be reusable and as such, being able to return the artifact or system to its original state is key for quick response and recovery times. 
7. **Not Resource Intensive:** Resources in many organizations are already limited and as such, honeypots should not consume an intensive amount of resources while in operation. Further to this, they should not require regular maintenance, and should be able to be left on the network unattended for long periods of time. 
9. **Monitored:** Special alarms and monitoring rules or tools should be configured to detect activity on this artifact or system. As mentioned above, noise from this system can be reduced by ensuring that it does not serve a business purpose thus reducing the likelihood of noise generated from day-to-day access. However, alarms and monitoring rules should generate high severity alerts based on activity on this machine to alert to a potential intruder. 

## The Apiary Maturity Model
The Apiary model defines six (6) levels of maturity of an organization’s honeypot deployment and management strategy. Each level of the maturity model is based on the following:
1. **Detection and Incident Response Capability and Maturity: **The current maturity of the organization’s incident detection and response capabilities, based on the people, processes and technology. The maturity of this capability is important as it influences the various HoneyPot technologies which will be most effective, and vice versa.
2. **HoneyPots:** The various HoneyPots deployed within the organization.

|   |  Level 0 | Level 1   | Level 2  | Level 3  |  Level 4 |  Level 5 |
| :------------ | :------------ | :------------ | :------------ | :------------ | :------------ | :------------ |
| Detection and Incident Response Capability and Maturity  |  Ad-hoc/ Repeatable | Ad-hoc/ Repeatable  | Repeatable / Defined  |  Repeatable / Defined |  Managed/Optimized |Managed/Optimized   |
|  Minimum Honeypot Requirements  |  
| **On-Premise**  |   |   |   |   |   |   |
|  Honey Systems | (1) External Honey System OR (1) Internal Honey System  |(1) External Honey System OR (1) Internal Honey System   |(1) External Honey System OR (1) Internal Honey System   |(1) External Honey System OR (1) Internal Honey System   | (1) External Honey System OR (1) Internal Honey System  | (1) External Honey System OR (1) Internal Honey System  |
|  Honey Web Applications |   |(1) Honey Web Application   | (1) Honey Web Application  |  (1) Honey Web Application | (1) Honey Web Application  | (1) Honey Web Application  |
| Honey Files  |   |   | (1) Honey File  |(1) Honey File   |(1) Honey File   |(1) Honey File   |
| Honey Repositories  |   |   |   |  (1) Honey Repository |  (1) Honey Repository |  (1) Honey Repository |
|  Honey Credentials |   |   |   |   (1) Honey Credential|   (1) Honey Credential|  (1) Honey Credential |
|  Honey User  Identities |   |   |   |   |   (1) Honey User Identities| (1) Honey User Identities  |
|  Honey Service Identities |   |   |   |   |   |  (1) Honey Service Identity |
| **Cloud (where applicable)**  |   |   |   |   |   |   |
| Honey Cloud Resources  |   |   | (1) Honey Cloud Resource: External   | (1) Honey Cloud Resource: External   | (1) Honey Cloud Resource: External AND (1) Honey Cloud Resource: Internal  | (1) Honey Cloud Resource: External AND (1) Honey Cloud Resource: Internal  |
| Honey Cloud User Identities  |   |   |   |   | (1) Honey Cloud User Identities  | (1) Honey Cloud User Identities  |
| Honey Cloud Service Identities  |   |   |   |   |   | (1) Honey Cloud Service Identity  |


------------


### Level 0 Apiary
Level zero apiary is the entry level tier which is designed to be easy to implement and cost effective with clear security benefits, and is not limited to organizations.

**a. Detection and Incident Response Capability and Maturity Prerequisites:** Initial to Ad-hoc/Repeatable detection and incident response capability and maturity is required to facilitate a Level 0 Apiary. This is characterized by processes which are not fully defined, technologies which are basic and minimal skilled resources. In particular, the following are required at a minimum:
- **Processes:** Basic processes for preparing, responding and following up on incidents or alerts on the network, or from the HoneyPot. These processes are ideally not documented nor is there a standard procedure to follow for triage. Technology is relied upon heavily.
- **People: **Dedicated, skilled human resources are not available to facilitate the incident response capabilities and personnel who facilitate the incident response processes share other responsibilities.  
- ** Technology:** Basic detection and incident response technologies are implemented in an unstructured manner to detect and respond to incidents. This may include but is not limited to technologies to support logging and alerting or incident management.

**b. HoneyPots:** The HoneyPots which can be implemented in this level are basic, and are applicable to the external and internal environments:

1. **On-Prem:** One or more of the following on-prem system honeypots can be implemented within this level. Enticement is limited to basic vulnerabilities and exposures to appear as the low hanging fruit on the network. These are selected as minimal additional logging and detection capabilities are required to be configured, other than that of the alerting mechanisms for malicious activity. In some instances, logging and detection capabilities are already built in thus reducing the resources required to implement:
	- Honey Systems:
	-- External Facing Honey Systems
	-- Internal Facing Honey Systems 

**c. Benefits:**
1. ** Basic and easy to implement HoneyPots: **This Apiary level is primarily geared towards HoneyPots which are easy to implement and monitor within an environment. HoneySystems often require minimal setup;
2. **Built-in monitoring and alerting:** This Apiary level leverages honeypots which have in-built monitoring capabilities, thus reducing setup and alerting requirements and further making it suitable for organizations with limited monitoring and incident response capabilities;
3. **Foundational:** This Apiary level builds a foundation for where other HoneyPots can be deployed upon, as Honey Systems can support various other types of Honey Pots e.g. Honey File.
4. **Designed to detect attacks early in the cyber kill chain:** being foundational, this level is designed to deploy HoneyPots which can detect attacks early in the cyber kill chain, allowing for early detection and remediation of breaches.


------------

### Level 1 Apiary
A Level one apiary maintains the detection and incident response capability of Level 0, while increasing the minimum Honeypot types. This level is designed to also be easy to implement, cost effective and provide clear security benefits.

**a. Detection and Incident Response Capability and Maturity Prerequisites:** Initial to Ad-hoc/Repeatable (same as Level 0)

**b. Honeypots: ** The Honeypots which can be implemented in this level are basic, build upon those which are detailed at a minimum in Level 0, and are applicable to external and internal:
1. On-Prem:  This level combines honey systems with honey web applications, where at minimum one honey system type and one web application is required. 
	2. **Honey Systems**:
		3. External Facing Honey Systems
		4. Internal Facing Honey Systems 
	5. **Honey Web Applications**
		6. External Facing
		7. Internal Facing

**c. Benefits:**
1. **Basic and easy to implement HoneyPots:** This Apiary level is primarily geared towards expanding upon the easy-to-implement Honey Pots by incorporating an additional attack vector, web applications, which can be easily deployed on Honey Systems.
2. ** Built-in monitoring and alerting:** This Apiary level leverages honeypots which have in-built monitoring capabilities, thus reducing setup and alerting requirements and further making it suitable for organizations with limited monitoring and incident response capabilities;
3. **Foundational:** This Apiary level builds a foundation for where other HoneyPots can be deployed upon, as Honey Systems or Honey Web Applications can support various other types of Honey Pots e.g. Honey File.
4. **Designed to detect attacks early in the cyber kill chain:** being foundational, this level is designed to deploy HoneyPots which can detect attacks early in the cyber kill chain, allowing for early detection and remediation of breaches.

------------
### Level 2 Apiary

A Level 2 apiary increases the detection and incident response requirements to support the minimum types of honeypots effectively. This level is designed to incorporate cloud systems as well as provide support to organizations which consider data loss prevention as a priority.

**a. Detection and Incident Response Capability and Maturity Prerequisites:** Defined detection and incident response capability and maturity is required to facilitate a Level 2 Apiary. This is characterized by processes which are defined, and strategically supported by technologies and skilled resources. In particular, the following are required at a minimum:
1. **Processes:** Defined processes for preparing, responding and following up on incidents or alerts on the network, or from the HoneyPot. These processes are ideally documented and is there a standard procedure to follow for triage.
2. **People:** Dedicated, skilled human resources are available to facilitate the incident response capabilities. Personnel who facilitate the incident response processes can share other responsibilities, however are dedicated to the organization’s incident response efforts.
3. **Technology:** Technologies which provide basic centralized logging and security event correlation are implemented, in addition to technologies to support incident handling. 

**b. Honeypots:** The honeypots which can be implemented at this level extend beyond the on-premise environment to the cloud, and integrate considerations for detecting data tampering at the file level.
1. On-Prem:  This level combines honey systems with honey web applications, where at minimum one honey system type, one web application and one  honey file is required. 
	2. Honey Systems:
		3. External Facing Honey Systems
		4. Internal Facing Honey Systems 
	5. Honey Web Applications
		6. External Facing
		7. Internal Facing
	8. Honey File
9. Cloud:  This level adds considerations for the cloud, where at minimum one honey system or web application is required for implementation. This implementation is not applicable if cloud technologies are not in use. 
	10. Honey Cloud Resource
		11. External Facing

**c. Benefits: **
1. **Data protection considerations: **This Apiary level incorporates considerations for data protection through the incorporation of HoneyFiles to detect data access, modification, transmission or destruction.
2. **Cloud detection considerations:** This Apiary level incorporates basic considerations for detecting cloud threats through the implementation of basic HoneyPots in the cloud. 
3. **Cloud foundations:** This Apiary level incorporates cloud honey systems and honey web applications, which set the foundation for other cloud based honeypots e.g. honey file.

------------
### Level 3 Apiary
A Level 3 apiary maintains the minimum detection and incident response capability of Level 2, however it is geared towards organizations at the higher end of the “Defined” capability. This level is designed to incorporate credentials and databases as part of the honeypot strategy to detect lateral movement as well as data loss at the data repository level.

**a. Detection and Incident Response Capability and Maturity Prerequisites: **Defined (same as level 2);

**b. Honeypots: **This level expands upon level 2 by adding honeypots designed to detect lateral movement and data loss at the database level.
1. On-Prem:  This level combines honey systems with honey web applications, where at minimum one honey system type, one web application and one  honey file is required. 
	2. Honey Systems:
		3. External Facing Honey Systems
		4. Internal Facing Honey Systems 
	5. Honey Web Applications
		6. External Facing
		7. Internal Facing
	8. Honey File
	9. Honey Credential
	10. Honey Repository
11. Cloud:  This level adds considerations for the cloud, where at minimum one honey system or web application is required for implementation. This implementation is not applicable if cloud technologies are not in use. 
	12. Honey Cloud Resource
		13. External Facing
		14. Honey Credential

**c. Benefits:**
1. **Additional data loss detection vectors:** This level expands upon the data protection considerations of the prior level by adding additional HoneyPots designed to detect data loss at the database level.
2. **Lateral movement:** Detecting lateral movement is a key concern and indicator of compromise within an organization. This level adds starting HoneyPots to detect basic credential usage within the environment in order to identify lateral movement. This is particularly beneficial as it adds considerations for detection of malicious activity at the middle of the attack chain to compensate for where initial access is not detected.

------------
### Level 4 Apiary
A Level 4 apiary increases the detection and incident response capability requirements to a minimum of management. This level is designed to incorporate user identities as part of the detection strategy and place additional reliance on technology and automation for incident response.

**a. Detection and Incident Response Capability and Maturity Prerequisites:** Managed/Optimizing: This Apiary level sets the minimum requirement of Managed where processes and procedures are defined, tested for effectiveness and skilled resources are dedicated to incident response efforts. 
1. Processes: Processes for preparing, responding and following up on incidents or alerts on the network, or from the HoneyPot are defined and regularly tested for effectiveness and improved upon.
2. People: Dedicated, skilled human resources are available to facilitate the incident response capabilities and effectiveness is measured and tracked.
3. Technology: Detection and incident response technologies are implemented in a structured manner to detect and respond to incidents. These technologies are regularly tested for effectiveness and improved upon.

**b. Honeypots:** This level expands upon Level 3 by adding additional honeypots designed to detect lateral movement.
1. On-Prem:  This level combines honey systems with honey web applications, where at minimum one honey system type, one web application and one  honey file is required. 
	2. Honey Systems:
		3. External Facing Honey Systems
		4. Internal Facing Honey Systems 
	5. Honey Web Applications
		6. External Facing
		7. Internal Facing
	8. Honey File
	9. Honey Credential
	10. Honey Repository
	11. Honey User Identity
12. Cloud:  This level adds considerations for the cloud, where at minimum one honey system or web application is required for implementation. This implementation is not applicable if cloud technologies are not in use. 
	13. Honey Cloud Resource
		14. External Facing
	15. Honey Cloud Credential
	16. Honey Cloud User Identity

**c. Benefits:**
1. **Additional lateral movement considerations: **This level focuses on expanding HoneyPots designed at detecting additional types of lateral movement in the environment.

------------
### Level 5 Apiary
A Level 5 apiary miantians the same level of detection and incident response capability requirement as level 4 (managed). This level is designed to incorporate minor expansions to the honeypot requirements over Level 4.

**a. Detection and Incident Response Capability and Maturity Prerequisites:** Managed/Optimizing: (same as Level 4)

**b. Honeypots:** This level expands upon Level 4 by adding additional honeypots designed to detect lateral movement.
1. On-Prem:  This level combines honey systems with honey web applications, where at minimum one honey system type, one web application and one  honey file is required. 
	2. Honey Systems:
		3. External Facing Honey Systems
		4. Internal Facing Honey Systems 
	5. Honey Web Applications
		6. External Facing
		7. Internal Facing
	8. Honey File
	9. Honey Credential
	10. Honey Repository
	11. Honey User Identity
	12. Honey Service Identity
13. Cloud:  This level adds considerations for the cloud, where at minimum one honey system or web application is required for implementation. This implementation is not applicable if cloud technologies are not in use. 
	14. Honey Cloud Resource
		15. External Facing
		16. Internal Facing
	17. Honey Cloud Credential
	18. Honey Cloud User Identity
	19. Honey Cloud Service Identity

**c. Benefits:**
1. **Additional lateral movement considerations:** This level focuses on expanding HoneyPots designed at detecting additional types of lateral movement in the environment.

## The HoneyPots 

#### 1.1 On-Premise | Honey Systems
Honey systems are operating systems (virtual or physical) which sit on either the boundary of a network (external facing) or within the network (internal facing). These systems are characterized by the following:
**General Descriptors: **
2. **Enticement: **These systems are enticing to attackers as they are easily detected on the network through port scans, IP directories or Active Directory. Enticement can be improved by performing the following:
	3. **Naming**: changing the name of the systems to one which mimics a critical asset e.g. file server, database server or domain controller within the organization. Enticements which rely on naming conventions should, to the maximum extent possible, leverage organizational information to increase enticement. 
	4. **IP Assignment**: assignment of IP addresses which are low in range (e.g. 10.10.10.5) to increase detectability and visibility at the network level to entice attackers.
	5. **Active Directory**: special assignments to groups (e.g. jump server group, IT workstations group) or attributes on the Active Directory to increase visibility. 
	6. **Vulnerabilities and Misconfigurations**: basic misconfigurations or vulnerabilities on the system which are easily detectable and exploitable by an attacker, but which the detection and exploitation is easily detectable by the defender. 
	7. **Network Services:** services installed on the system which expose unusual services running on usual port assignments.
8. **Security:** These systems, while enticing, are secured and compromise of the system would not compromise the confidentiality, integrity and availability of other systems on the network. The security of these systems can be maintained through the implementation of the organization’s security stack which should, at the minimum, include the following:
	9. Anti-malware
	10. System Hardening
	11. Changing default passwords
	12. Reducing connections to other systems on the network

14. **Recoverable:** Backup and recovery mechanisms do not necessarily need to follow the standard organizational backup and recovery procedures, however a backup of the initial state which includes setup and configuration should be retained and used to restore the systems to a honeypot state upon compromise. This can also be accomplished by snapshots on both Linux and Microsoft Windows systems.

16. **Not Resource Intensive:** Honey systems should not require exorbitant amounts of computing power to run and as such, these systems should be minimal and deployed only for purpose. Further to this, it should require low to medium interaction from the owner.

18. **Monitored: **These systems may have integrated logging and alerting capabilities which can be leveraged as a stand-alone solution or can feed into centralized event logging systems. Monitoring can include the following:
	19. **General - Operating System Event Logs:** event logs such as Windows Event Logs and Syslogs can be collected and analyzed. Alerts should be configured to trigger upon event logs which detect user activity such as sign on or launching of new applications/processes.
	20. **Specific - Network Connections: **monitoring of network connections to and from the machine can be implemented to detect potential malicious activity as well as command-and-control activity.
	21. **Specific - Operating System Integrity:** changes in operating system integrity such as changes to user accounts or operating system files can be implemented to detect malicious activity.

#### 1.2 On-Premise | Honey Web Applications
Honey web applications (external and internal) are web applications which are intentionally designed to be enticing to threat actors which target web applications. 
**General Descriptors:**
1. **Enticement:** These systems are enticing to attackers as, like with honey systems, are easily detected on networks through port scans or through Active Directory. 
	2. **IP Address:** assignment of IP addresses which are low in range (e.g. 10.10.10.5) to increase detectability and visibility at the network level to entice attackers.
	3. **Ports: **use of standard, commonly used web application ports increase the discoverability of the web application;
	4. **Web Application Design:** use of enticing web application designs such as those with login pages or those which allude to the storage of confidential information;
5. **Security: **These web applications should maintain a particular level of security not store information or be configured in such a way that it poses a risk to the rest of the environment. Security controls should at a minimum include:
	6. Web Application Request Filtering
7. **Recoverable: **Recovery mechanisms should be established to recover the web application source files, and databases where applicable.
8. **Not Resource Intensive:** The web application should not require substantive computing resources and should require low to medium interaction from the owner.
9. **Monitored: **Logging and monitoring can be implemented at the web server layer which serves the web application as these software often have integrated logging capabilities and can feed into centralized log collection systems. Monitoring can include the following:
	10. **General - Web Server Logs:** event logs such as Windows Event Logs and Syslogs can be collected and analyzed. Alerts should be configured to trigger upon event logs which detect user activity such as sign on or launching of new applications/processes.
	11. **Specific - Application Logs:** Logging at the web application layer can also be performed, however this may require the web application to be designed to support logging and monitoring. 

#### 1.3 On-Premise | Honey Files
Honey files are data files which are crafted to be enticing to attackers, however do not contain data which can harm the organization.
**General Descriptors:**
1. **Enticement: **These files are enticing to attackers who seek sensitive information which can be used to extort the organization, or further compromise the environment: 
	2. Location: placing the file on exposed locations such as shared drives or document management systems;
	3. Naming: use of naming schemes which allude to the presence of sensitive information such as PII or credentials;
	4. File Type: use of common file types which do not support encryption such as flat files or Office documents.
5. **Security:** These files should not contain sensitive information which can pose a security risk. 
6. **Recoverable:** Recovery mechanisms should be established to recover or restore the file to its original state.
7. **Not Resource Intensive: **The file and its monitoring process should not require extensive computing resources such as space or processing power.
8. **Monitored:** Logging and monitoring can be implemented through the use of File Integrity Monitoring (FIM) solutions to detect changes or file access where the objective is to determine whether the file was accessed. Where the objective is to detect data loss, FIM can be combined with network monitoring tools to detect file transfers, and can be enhanced through event correlation engines.

#### 1.4 On-Premise | Honey Credentials
Honey credentials are usernames and passwords/hashes which are intentionally left exposed for attackers to stumble upon and attempt to leverage to elevate access or move laterally on the network.

**General Descriptors:**
1. **Enticement:** These credentials are enticing to attackers who seek to elevate access or move laterally on the network. Enticements can be in the following categories: 
	2. **Naming:** using keywords which allude to elevated permissions e.g. admin, superuser on databases, the local system or the network;
	3. **Location:** the placement of these credentials in locations which are easily accessed or exposed e.g. shared drives, SYSVOL etc;
Enticements should be focused on crafting the credential to resemble either system, database or network credentials to reduce the 
5. **Security:** These credentials should not actually possess privileges, and instead should be either disabled or non-existent within the environment. This also aids in monitoring as often operating systems and databases can generate audit logs for denied logins natively.
6. **Recoverable:** Mechanisms should be put in place to restore the credential information to its original state where it to be tampered with.
7. ** Not Resource Intensive:** Maintaining the credential and monitoring its use should not consume extensive resources.
8. **Monitored:** Monitoring of the use of the credential can be implemented based on the enticement used and be done at the respective levels to detect denied logins.

#### 1.5 On-Premise | Honey Repositories
Honey Repositories are collections of data such as database instances, sharepoint instances or code repositories which are intentionally exposed for attackers to target.
**General Descriptors:**
1. **Enticement:** Repositories are appealing to attackers as they may contain sensitive information which can be exfiltrated. Enticements can be in the following categories: 
	2. **Naming:** utilizing keywords which allude to the storage of sensitive information;
	3. **Vulnerabilities and Misconfigurations: **common vulnerabilities and misconfigurations which are considered to be “low hanging fruit”;
4. **Security:** These repositories should not contain sensitive data and instead at a minimum contain test or dummy data. Further to this, the database instance should at minimum be hardened (with select misconfigurations for enticement e.g. default credentials) to reduce the risk of compromise of the underlying operating system;
5. **Recoverable:** Mechanisms should be put in place to restore the repository and its configuration to the original state were it to be changed by a threat actor.
6. **Not Resource Intensive:** The repository instance nor its monitoring mechanisms should not consume excessive compute resources.
7. **Monitored:** Repository software often supports auditing and logging and as such monitoring of the database logs for access can be implemented to detect malicious activity.

#### 1.6 On-Premise | Honey Repositories
Honey user identities are identities registered with identity and access management solutions (e.g Active Directory) and are designed to be enticing to attackers and detect attempts to abuse the identity. It is different from a Honey Credential which may not exist on any system.

**General Descriptors:**
1. **Enticement:** User identities appeal to attackers as they may have access to sensitive information on the network or can be abused as part of business email compromise attacks. 
	2.** User Naming:** Utilizing standard naming conventions;
	3. **User Groups: **Placing the user identities within groups which designate it as high value targets e.g. Finance, IT etc.
	4. **Security Exceptions: **Applying security exceptions to the identity which are visible on the identity and access management solution e.g.. DoNotRequirePreAuth on Active Directory;
	5. **Access Control Lists and Permissions:** Applying special access controls and permissions to the account which are visible on the identity and access management solution.
6. **Security:** These identities should have restrictions which prohibit its use to reduce the risk of abuse of the identity. Further to this, enticements should give the appearance of elevated or sensitive access, while not effectively giving access. 
7. **Recoverable:** Mechanisms should be established to restore the identity and its respective enticements to the original state were it to be modified by an attacker.
8. **Not Resource Intensive:** Maintaining the identity and its enticements should not consume excessive resources on the identity and access management solutions e.g  Office365.
9. **Monitored:** Identity and access management solutions often have native logging and auditing capabilities, which can be integrated with motoring and security event management solutions for monitoring of the use of the credential.

#### 1.7 On-Premise | Honey Service Identities
Honey service identities are identities which enable network services registered with identity and access management solutions (e.g Active Directory) and are designed to be enticing to attackers and detect attempts to abuse the identity. It is different from a Honey Credential which may not exist on any system and different from a user identity whereby enticements are crafted to give the appearance of a service account.
**General Descriptors:**
1. **Enticement:** Service identities appeal to attackers as they may have access to sensitive services on the network or can be abused as part of lateral movement attempts. To increase the enticement of these . 
	2. **Account Naming:** Utilizing standard naming conventions for service accounts;
	3. **Account Groups:** Placing the service identities within groups which designate it as high value targets e.g. Service Accounts.
	4. **Security Exceptions:** Applying security exceptions to the identity which are visible on the identity and access management solution e.g.. Configuring a Service Principal Name on Active Directory;
	5. **Access Control Lists and Permissions:** Applying special access controls and permissions to the account which are visible on the identity and access management solution.
6. **Security:** These identities should have restrictions which prohibit its use to reduce the risk of abuse of the identity. Further to this, enticements should give the appearance of elevated or sensitive access, while not effectively giving access. 
7. **Recoverable:** Mechanisms should be established to restore the identity and its respective enticements to the original state were it to be modified by an attacker.
8. **Not Resource Intensive:** Maintaining the identity and its enticements should not consume excessive resources on the identity and access management solutions e.g  Office365.
9. **Monitored:** Identity and access management solutions often have native logging and auditing capabilities, which can be integrated with motoring and security event management solutions for monitoring of the use of the credential.


#### 2.1 The Cloud | Honey Cloud Identities
Honey identities are identities registered with cloud identity and access management solutions (e.g Azure Active Directory) and are designed to be enticing to attackers and detect attempts to abuse the identity. Within cloud services, there are various classes of identities, which honeypots are described for in the preceding sections.

##### 2.1.1 The Cloud | Honey Cloud User Identities
Honey user identities are cloud identities related to a specific human user, and are designed to be enticing to attackers and detect attempts to abuse the human identity. 
**General Descriptors:**
1. **Enticement:** User identities appeal to attackers as they may have access to sensitive information on the network or can be abused as part of business email compromise attacks. 
	2. **User Naming**: Utilizing standard naming conventions;
	3. **User Groups**: Placing the user identities within groups which designate it as high value targets e.g. Finance, IT etc.
	4. **Security Exceptions**: Applying security exceptions to the identity which are visible on the identity and access management solution 
	5. **Access Control Lists and Permissions**: Applying special access controls and permissions to the account which are visible on the identity and access management solution.
6. **Security**: These identities should have restrictions which prohibit its use to reduce the risk of abuse of the identity. Further to this, enticements should give the appearance of elevated or sensitive access, while not effectively giving access. 
7. **Recoverable:** Mechanisms should be established to restore the identity and its respective enticements to the original state were it to be modified by an attacker.
8. **Not Resource Intensive**: Maintaining the identity and its enticements should not consume excessive resources on the identity and access management solutions e.g  Office365.
9. **Monitored: **Identity and access management solutions often have native logging and auditing capabilities, which can be integrated with motoring and security event management solutions for monitoring of the use of the credential.

##### 2.1.1 The Cloud | Honey Cloud Service Identities
Honey service identities are identities which enable network services registered with identity and access management solutions (e.g Azure Active Directory) and are designed to be enticing to attackers and detect attempts to abuse the identity. It is different from a Honey Cloud User identity as it is specifically registered as a cloud service account.
**General Descriptors:**
1. **Enticement:** Service identities appeal to attackers as they may have access to sensitive services on the network or can be abused as part of lateral movement attempts. To increase the enticement of these . 
	2. **Account Naming:** Utilizing standard naming conventions for service accounts;
	3. **Account Groups: **Placing the service identities within groups which designate it as high value targets e.g. Service Accounts.
	4. **Security Exceptions: **Applying security exceptions to the identity which are visible on the cloud identity and access management solution.
	5. **Access Control Lists and Permissions:** Applying special access controls and permissions to the account which are visible on the identity and access management solution.
6. **Security**: These identities should have restrictions which prohibit its use to reduce the risk of abuse of the identity. Further to this, enticements should give the appearance of elevated or sensitive access, while not effectively giving access. 
7. **Recoverable**: Mechanisms should be established to restore the identity and its respective enticements to the original state were it to be modified by an attacker.
8. **Not Resource Intensive: **Maintaining the identity and its enticements should not consume excessive resources on the identity and access management solutions e.g  Office365.
9. **Monitored:** Identity and access management solutions often have native logging and auditing capabilities, which can be integrated with motoring and security event management solutions for monitoring of the use of the credential.

#### 2.2 The Cloud | Honey Cloud Resources
Honey cloud resources are those cloud services which are designed to be enticing to attackers and detect attempts to utilize the resource in an unexpected or malicious way. Resources in this section are generalized to maximize compatibility across various cloud infrastructure providers.
**General Descriptors:**
1. **Enticement:** Cloud resources appeal to attackers as they may contain sensitive data, or be leveraged to pivot across the environment. To increase the enticement of these . 
	2. **Resource Naming: **Utilizing standard resource naming conventions for cloud resources;
	3. **Resource Type:** Resources such as key stores and data stores are more enticing to attackers. 
4. **Security**: These resources should not contain or store sensitive information, or be linked to other resources, as to reduce the likelihood of lateral movement across the cloud. Enticements should give the appearance of sensitivity, while not being sensitive.
5. **Recoverable**: Mechanisms should be established to restore the resource and its respective enticements to the original state were it to be modified by an attacker.
6. **Not Resource Intensive:** Maintaining the resource and its enticements should not consume excessive resources on the cloud platform.
7. **Monitored**: Cloud resources often have logging at both the management pane and at the data pane. The appropriate pane should be selected and monitored for unauthorized or unusual activity.



------------

## The HoneyPot Return-on-Investment Methodology
ROI is the ratio between the reduction in daily cost of an attacker dwelling on the network to the daily cost of an attacker dwelling prior to honeypots being implemented.

- Cost of Breach Before (CB1): The average cost of a breach prior to the honeypots being implemented. This includes remediation costs, litigation costs and regulatory costs
- Dwell Time Before (DT1): The average dwell time prior to honeypots being implemented.
- Daily Cost of an Attacker on the network before (CA1): 
- Cost of Implementation (COI): The cost to implement and maintain the honeypots on the network
- Dwell Time After (DT2): The average dwell time after the honeypots have been implemented or the target dwell time based on defined KPIs for the project.
- Delta Dwell Time (DT3): The difference in average dwell times.
- Cost of Breach After (CB2): The cost of breach after the implementation of Honeypots
- Daily Cost of an Attacker on the network after (CA2): the daily loss incurred when an attacker is on the network.

### Calculating Return on Investment
1. Calculate the cost of an attacker on the network before honeypots have been implemented
`	CA1 = CB1 DT1 `
3. Calculate the change in dwell time
`DT3 = DT1 - DT2 `
5. Calculate the cost of breach after honeypots have been implemented
`CB2 = COI +(DT3 CA1) `
7. Calculate the cost of an attacker on the network after honeypots have been implemented
`CA2 = CB2 / DT3 `
9. Calculate ROI:
`ROI = (CA1 - CA2) / CA1`

**Example:**
Assuming the following:
- CB1 = $50,000 
- DT1 = 30 days
- COI = $5,000
- DT2 = 10 days

1. Calculate the cost of an attacker on the network before honeypots have been implemented
`CA1 = CB1 / DT1 `
`CA1 = $50,00030`
`CA1 =  $1,667`
2. Calculate the change in dwell time
`DT3 = DT1 - DT2 `
`DT3 = 30- 10`
`DT3 = 20`
3. Calculate the cost of breach after honeypots have been implemented
`CB2 = COI +(DT3 CA1) `
`CB2 = $5000+(20 $1,667) `
`CB2 = $21,667`
4. Calculate the cost of an attacker on the network after honeypots have been implemented
`CA2 = CB2 / DT3` 
`CA2 = $21,667 / 20`
`CA2 =  $1,083 `
5. Calculate ROI:
`ROI = (CA1 - CA2) / CA1`
`ROI = ($1,667 - $1,083) / $1,667`
`ROI = 0.35	`


## References
Clarke, M. (2012). The Digital Revolution. In Academic and Professional Publishing (pp. 79-98). Chandos Publishing. https://doi.org/10.1016/B978-1-84334-669-2.50004-4
Nayyar, S. (2021, 4 3). Why The Dwell Time Of Cyberattacks Has Not Changed. Forbes. Retrieved 11 2, 2021, from https://www.forbes.com/sites/forbestechcouncil/2021/05/03/why-the-dwell-time-of-cyberattacks-has-not-changed/?sh=6f37b473457d

