
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


