# Security Concepts

## CIA Triad

The confidentiality, Integrity, and Availability (CIA) model is the opposite of Disclosure, Alternation, and Destruction (DAD). This model should help determine the value of data that it applies to, and in turn, the attention it needs from the business.

While the three elements of the CIA triad may overlap, if even one element is not met, then the other two are useless.

## Confidentiality [detailed](https://github.com/LogicBypass/ISC2-CC-Study-Material/blob/main/Notes/Security%20Concepts/Security%20Principles.md#confidentiality)
- Confidentiality - Permitting authorized access to information, while at the same time protecting information from improper disclosure

**Topics related to confidentiality:**
- **Sensitivity** - Importance assigned to information by the owner.
- ***Sensitive information** - is information that if improperly disclosed (**confidentiality**) or modified (**integrity**) would harm an organization or individual*.
 

Data that needs protection:

- **PII “*Personally Identifiable Information*”** - Any data that could be used to trace or identify an individual identity.
- **PHI “*Protected Health Information*”** - Information about one's health status, health provisioning, or healthcare payment.
- **Classified** or **Sensitive information** - includes trade secrets, research, business plans, and intellectual property.

#### Confidentiality Concerns
1. Snooping
	- Gathering information that is left out in the open online/offline.
	- "Clean desk policies" protect against snooping.
2. Dumpster Diving
	- Going through a person/organization's trash to obtain information.
	- "Shedding" protects against dumpster diving.
3. Eavesdropping
	- Listing sensitive information conversation.
	- "Rules about sensitive conversations" prevent eavesdropping
4. Wiretapping
	- Electronic eavesdropping - listing through wire(internet)
	- "Encryption" protects against Wiretapping
5. Social Engineering
	- Using psychological manipulation to convince an employee to give them sensitive information or access to internal systems.
	- Best defence is to "Educating users"


## Integrity
- Integrity is the condition where information is kept **accurate and consistent during storage, transmission, and usage** from errors in the information system or unauthorized access unless authorized changes are made.

**The concept of integrity applies to:**

- Information or Data
    - **Data integrity** is the assurance that data has not been changed in an unauthorized way. This involves protecting data during processing and storage to prevent errors, loss, or unauthorized modifications. Data integrity applies to data in storage, during processing, and while in transit.
    - **Consistency**, as part of data integrity, requires that all instances of the data be identical in form, content, and meaning on all related systems so that it is displayed and stored.
- Systems and processes for business operations
    - **System Integrity** refers to the maintenance of a known good configuration and expected operational function as the system processes the information.
        
        Ensuring integrity begins with an ability to document and understand the state of data or a system at a certain point creating a **baseline**
        
    - **A baseline** is a documented, lowest level of security configuration allowed by a standard or organization.
    From that baseline, the integrity of the data or the system can always be established by comparing the baseline with the current state
- Organizations
- People and their actions

#### Integrity_Concerns
1. Unauthorized modification
	- Attacks make changes without permission.
	- "Least priviege" protects against integrity attacks
2. Impersonation
	- Attacks pretend to be someone else
	- "User education" protects against attacks
3. Man-in-the-middle (MITM)
	- Attacks place the attacker in the middle of a communications session.
	- "Encryption" protects against MITM attacks
4. Replay
	- Attacks eavesdrop on logins and reuse the captured credentials.
	- "Encryption" protects against Replay attacks

**Access control** and **rigorous authentication** can help prevent authorized users from making unauthorized changes. 

**Hash verifications** and **digital signatures** can help ensure that transactions are authentic and that files have not been modified or corrupted.

## Availability
- Availability can be defined as timely and reliable access for authorized users to data and information services and the ability to use them.

- **Criticality** - a measure of the degree to which an organization depends on Information or Information systems in performing its operations.

Some systems and data are far more critical than others, so the security professional **must ensure that the appropriate levels of availability are provided**. 
This requires ensuring that **critical systems are identified and available.**

#### Availability_Concerns
1. Denial of service (DoS)
	- Unlimited request to a server
	- "Block unauthorized connections" to protect against denial of service attacks.
2. Power outages
	- Naturally or Man-made
	- "Redundant power and generators" protect against power outages.
3. Hardware failures
	- any component failures
	- "Redundant components" protect against hardware failure
4. Destruction
	- Naturally or Man-made
	- "Backup data centers" protect against destruction.
5. Service outages
	- Programing error and the failure of underlying equipment.
	- Building systems that are resilient in the face of errors and hardware failures.
	- Implementing well-versed security protocols


## Authentication and authorization
The access control process consists of three steps that you must understand. These steps are identification, authentication and authorization.

1. Identification incolves making a claim of identity.
	- Electronic identification commonly uses usernames
2. Authentication requires proving a claim of identity.
	- Electronic autherntication commonly uses passwords.
3. Authorization ensures that an action is allowed.
	- Electronic authorization commonly uses access control lists.

Authentication and authorization process, access control systems also provide "Accounting" functionality that allows administrators to track user activity and reconstruct that activity from logs. This may include tracking user activity on systems and even logging user web browsing history.


## Password security
Password mechanisms
	- Password length requirements set a minimum number of characters. 
	- Password complexity requirements describe the types of characters that must be included.
	- Password expiration requirements force password changes.
	- Password requirements prevent password reuse.


## Multifactor authentication
Multifactor authentication combines two different authentication factors.

Three different authentication factors. Something you know, something you are and something you have.

#### something you know
- Passwords, PIN's, Security questions.
#### something you are
- Biometric security mechanisms.
#### something you have
- Software and hardware tokens.

#### single sign-On (SSO)
Shares authentiacated sessions across systems
	- In a single sign on approach, users log on to the first SSO enabled system that they encounter. And then that login session persists across other systems until it expires. If the organization sets the expiration period to be the length of a business day, that means that users will only need to log in once a day and their single sign on is then going to last the entire day.


## Non-repudiation
Non-repudiation prevents someone from denying the truth.

Solved the issue with
	1. Signed contracts
	2. Digital signatures
	3. Video surveillance


## Privacy
Privacy Concerns
1. Protecting our own data.
2. Educating our users.
3. Protecing data collected by our organizations.

Private information may come in many forms. Two of the most common elements of private information are "Personally identifiable information" and "Protected health information".
1. Personally identifiable information, or PII, includes all information that can be tied back to a specific individual. 
2. Protected health information, or PHI, includes healthcare records that are regulated under the Health Insurance Portability and Accountability Act. Otherwise known as HIPAA.
