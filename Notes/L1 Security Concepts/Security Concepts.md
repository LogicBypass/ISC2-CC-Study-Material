# Security Concepts

## CIA Triad

The confidentiality, Integrity, and Availability (CIA) model is the opposite of Disclosure, Alternation, and Destruction (DAD). This model should help determine the value of data that it applies to, and in turn, the attention it needs from the business.

While the three elements of the CIA triad may overlap, if even one element is not met, then the other two are useless.

## Confidentiality [detailed](https://github.com/LogicBypass/ISC2-CC-Study-Material/blob/main/Notes/Security%20Concepts/Security%20Principles.md#confidentiality)
> Confidentiality - Permitting authorized access to information, while at the same time protecting information from improper disclosure
> 

**Topics related to confidentiality:**

- **Sensitivity** - Importance assigned to information by the owner.
    
    ***Sensitive information** - is information that if improperly disclosed (**confidentiality**) or modified (**integrity**) would harm an organization or individual*.
    

Data that needs protection:

- **PII “*Personally Identifiable Information*”** - Any data that could be used to trace or identify an individual identity.
- **PHI “*Protected Health Information*”** - Information about one's health status, health provisioning, or healthcare payment.
- **Classified** or **Sensitive information** - includes trade secrets, research, business plans, and intellectual property.

**Confidentiality threats:**

1. Snooping
    - Gathering information that is left out in the open online/offline.
    - "Clean desk policies" protect against snooping.
2. Dumpster Diving
    - Going through a person/organization's trash to obtain information
    - "Shedding" protects against dumpster diving.
3. Eavesdropping
    - Listing sensitive information conversation
    - "Rules about sensitive conversations" prevent eavesdropping
4. Wiretapping
    - Electronic eavesdropping - listing through wire(internet)
    - "Encryption" protects against Wiretapping
5. Social Engineering
    - Using psychological manipulation to convince an employee to give them sensitive information or access to internal systems.
    - The best defense is to "Educating users"

### **Integrity**

---

> Integrity is the condition where information is kept **accurate** and **consistent** during **storage**, **transmission**, and **usage** from **errors** in the information system or **unauthorized access** unless authorized changes are made.
> 

**The concept of integrity applies to:**

1. Information or Data
    - **Data integrity** is the assurance that data has not been changed in an unauthorized way. This involves protecting data during processing and storage to prevent errors, loss, or unauthorized modifications. Data integrity applies to data in storage, during processing, and while in transit.
    - **Consistency**, as part of data integrity, requires that all instances of the data be identical in form, content, and meaning on all related systems so that it is displayed and stored.
2. Systems and processes for business operations
    - **System Integrity** refers to the maintenance of a known good configuration and expected operational function as the system processes the information.
        
        Ensuring integrity begins with an ability to document and understand the state of data or a system at a certain point creating a **baseline**
        
    - **A baseline** is a documented, lowest level of security configuration allowed by a standard or organization.
    From that baseline, the integrity of the data or the system can always be established by comparing the baseline with the current state
3. Organizations
4. People and their actions

**Integrity threats:**

1. Unauthorized modification
    - Attacks make changes without permission.
    - "Least privilege" protects against integrity attacks
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

### Availability

---

> Availability can be defined as timely and reliable access for authorized users to data and information services and the ability to use them.
> 

********************************Criticality******************************** - a measure of the degree to which an organization depends on Information or Information systems in performing its operations.

*Some systems and data are far more critical than others, so the security professional must ensure that the appropriate levels of availability are provided. This requires ensuring that critical systems are identified and available.*

**Availability threats:**

1. Denial of service (DoS)
    - Unlimited requests to a server
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
    - Programming error and the failure of the underlying equipment.
    - building systems that are resilient in the face of errors and hardware failures.
    - Implementing well-versed security protocols
    

### ****Authentication****

---

> Consists of an **Access Control processes** validating the identity of a **user** or **entity** before granting access to a system or resource, by comparing one (Single-Factor SFA) or multiple (Multi-Factor MFA) factors of identification.
> 

**Access Control processes:**

1. **Identification**: The process of presenting an identity or claiming to be a specific user, without providing any evidence to support the claim.
    - Electronic identification commonly uses usernames, emails
2. **Authentication**: The process of verifying the claimed identity by providing evidence.
    - Electronic authentication commonly uses passwords.
3. **Authorization**: The process of granting or denying access to a resource or system based on a user's identity and permissions.
    - Electronic authorization commonly uses access control lists.

Access control systems not only perform **authentication** and **authorization** but also offer "**Accounting**" functionality to monitor and record user activity. 
This feature allows administrators to track user activity on the system, and access logs can be used to reconstruct user behavior. This includes logging user activity on systems and even monitoring web browsing history.

**Methods and types of authentication:**

**Methods** of authentication:

1. Something you **know** __“Knowledge-based”__: Password, Passphrase, ID
2. Something you **have** __"Token-based"__: Token, Memory cards, Smart Cards
3. Something you **are** __“Characteristic-based”__: Biometrics, Some measurable characteristics 
- **Password security requirements:**
    - **Password length requirements** set a minimum number of characters. 
    - **Password complexity requirements** describe the types of characters that must be included.
    - **Password expiration requirements** force password changes.
    - **Password history requirements** prevent password reuse.

**Types** of authentication:

- **Single-Factor Authentication (SFA)** - Using only one of the methods of authentication stated previously.
- **Multi-Factor Authentication (MFA)** - Using a combination of two or more methods of authentication stated previously
- **Single Sign-On (SSO):**
    
    In a single sign-on (SSO) approach, users only need to log in once to the first SSO-enabled system they encounter. This authenticated session is then shared across other systems until it expires. If the session expires at the end of the business day, users will only need to log in once a day to access all systems, making the sign-on process more convenient and efficient.
    

### Non-repudiation

---

> **Non-repudiation** is a security property that prevents an individual or entity from denying that they have performed a particular action or transaction.
> 

> Assurance that the sender of information is provided with proof of delivery and the recipient is provided with proof of the sender's identity, so neither can later deny having processed the information.
> 

Solved the issue with 1. Signed contracts 2. Digital signatures 3. Video surveillance****

## Privacy
Privacy Concerns
1. Protecting our own data.
2. Educating our users.
3. Protecing data collected by our organizations.

Private information may come in many forms. Two of the most common elements of private information are "Personally identifiable information" and "Protected health information".
1. Personally identifiable information, or PII, includes all information that can be tied back to a specific individual. 
2. Protected health information, or PHI, includes healthcare records that are regulated under the Health Insurance Portability and Accountability Act. Otherwise known as HIPAA.
