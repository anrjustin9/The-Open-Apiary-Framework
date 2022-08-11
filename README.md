
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
### Level 4 Apiary
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



