# Introduction #

## Upon completing this module, you’ll be able to:
>Describe directory services in Azure, including Azure Active Directory (AD) and Azure AD DS.
>Describe authentication methods in Azure, including single sign-on (SSO), multifactor authentication (MFA), and passwordless.
>Describe external identities and guest access in Azure.
>Describe Azure AD Conditional Access.
>Describe Azure Role Based Access Control (RBAC).
>Describe the concept of Zero Trust.
>Describe the purpose of the defense in depth model.
>Describe the purpose of Microsoft Defender for Cloud.

# Describe Azure directory services #

* Azure Active Directory (Azure AD) is a directory service that enables you to sign in and access both Microsoft cloud applications and cloud applications that you develop
* Azure AD can also help you maintain your on-premises Active Directory deployment
* IT administrators, App developers, Users, Online service subscribers use Azure AD
* Azure AD provides services such as Authentication, Single Sign-on, Application management, Device management
* You can connect your on-premises AD with Azure AD using Azure AD Connect
* Azure Active Directory Domain Services (Azure AD DS) is a service that provides managed domain services such as domain join, group policy, lightweight directory access protocol (LDAP), and Kerberos/NTLM authentication
* Azure AD DS integrates with your existing Azure AD tenant and allows users to sign in using existing credentials
* You can lift and shift legacy applications from your on-premises environment into a managed domain without managing AD DS environment in the cloud
* Azure AD DS creates a replica set of 2 Windows Server Domain Controllers in the selected Azure region
* Azure platform handles the DCs as part of the managed domain, including backups and encryption at rest using Azure Disk Encryption
* A managed domain is configured to perform a one-way synchronization from Azure AD to Azure AD DS.

# Describe Azure authentication methods #

* Authentication is the process of establishing the identity of a person, service, or device, which requires the user to provide some type of credential to prove who they are.
* Azure supports multiple authentication methods, including standard passwords, single sign-on (SSO), multifactor authentication (MFA), and passwordless.
* Single sign-on (SSO) enables a user to sign in one time and use that credential to access multiple resources and applications from different providers. SSO simplifies the security model and makes it easier for users to manage their identities and for IT to manage users.
* Multifactor authentication is the process of prompting a user for an extra form of identification during the sign-in process. MFA helps protect against a password compromise in situations where the password was compromised but the second factor wasn't.
* Azure AD Multi-Factor Authentication is a Microsoft service that provides multifactor authentication capabilities, enabling users to choose an additional form of authentication during sign-in.
* Passwordless authentication methods are more convenient because the password is removed and replaced with something you have, something you are, or something you know. Microsoft global Azure and Azure Government offer passwordless authentication options that integrate with Azure Active Directory (Azure AD) such as Windows Hello for Business, Microsoft Authenticator app, and FIDO2 security keys.
* Passwordless authentication is a method of secure access that removes the need for a password and replaces it with something the user has, something the user is, or something the user knows.
* To set up passwordless authentication, a device needs to be registered or enrolled with Azure so that it can be associated with the user.
* Azure Active Directory (Azure AD) offers three passwordless authentication options: Windows Hello for Business, Microsoft Authenticator app, and FIDO2 security keys.
* Windows Hello for Business is ideal for users with their own designated Windows PC, providing a convenient method for accessing corporate resources on-premises and in the cloud.
* Microsoft Authenticator app turns any iOS or Android phone into a strong, passwordless credential.
* FIDO2 security keys are an unphishable standards-based passwordless authentication method that can come in any form factor, typically USB devices, but could also use Bluetooth or NFC.

# Describe Azure external identities #

* External identities refer to individuals, devices, and services outside of an organization that need access to resources within the organization.
* Azure AD External Identities allows for secure collaboration with partners, vendors, suppliers, etc. and manage customer identity experiences.
External identities can use their own credentials to sign in, with their identity provider managing their identity and Azure AD or Azure AD B2C managing access to resources.
External Identities capabilities include:
Business to business (B2B) collaboration: allowing external users to use their preferred identity to access enterprise apps.
B2B Direct Connect: establishing mutual trust with another Azure AD organization for seamless collaboration.
Azure AD Business to Customer (B2C): publishing apps to consumers while using Azure AD B2C for identity and access management.
Azure AD B2B feature allows for easy collaboration across organizational boundaries by inviting guest users from other tenants and ensuring appropriate access through access reviews and recertification.

# Describe Azure conditional access #

Conditional Access is a tool in Azure Active Directory used to allow or deny access to resources based on identity signals, including who the user is, where the user is, and what device the user is requesting access from.
Conditional Access helps IT administrators empower users to be productive and protect the organization's assets.
Conditional Access also provides a more granular multifactor authentication experience for users, where they may or may not be challenged for a second authentication factor based on certain signals.
Conditional Access collects signals from the user during sign-in, makes decisions based on those signals, and enforces the decision by allowing or denying access or challenging for a multifactor authentication response.
Use cases for Conditional Access include requiring multifactor authentication for certain roles or locations, limiting access to services through approved client applications, requiring access to applications only from managed devices, and blocking access from untrusted sources.

# Describe Azure role-based access control #

Azure Role-based Access Control (RBAC) is a way to control access to resources in a cloud environment by assigning roles to individuals or groups, with each role having a specific set of access permissions.
RBAC roles can be built-in or custom-defined, and access is applied to a scope, which can be a management group, subscription, resource group, or individual resource.
RBAC is hierarchical, with permissions granted at a parent scope inherited by all child scopes.
RBAC is enforced through Azure Resource Manager, a management service that provides a way to organize and secure cloud resources.
RBAC uses an allow model, meaning that when a role is assigned, the user is allowed to perform actions within the scope of that role.
RBAC does not enforce access permissions at the application or data level, so application security must be handled by the application.

# Describe zero trust model #

Zero Trust is a security model that assumes the worst case scenario and protects resources with that expectation.
Zero Trust assumes breach at the outset, and verifies each request as though it originated from an uncontrolled network.
Guiding principles include: verifying explicitly, using least privilege access, assuming breach, and minimizing the blast radius and segmenting access.
In Zero Trust, everyone is required to authenticate and access is granted based on authentication rather than location.
The Zero Trust model is a recommended approach by Microsoft to adapt to the complexity and mobility of modern environments and protect people, devices, applications, and data.
The Zero Trust model is a contrast to traditional corporate networks which assumed safety and restricted access based on location.

# Describe defense-in-depth #

Defense-in-depth is a strategy that uses multiple layers to protect data and prevent unauthorized access.
Layers of defense-in-depth include physical security, identity and access, perimeter, network, compute, application, and data.
Each layer provides protection and slows down an attack, allowing security teams to act.
Azure provides security tools and features at each layer of defense-in-depth.
Physical security layer focuses on physically securing access to buildings and controlling access to computing hardware.
Identity and access layer ensures identities are secure, access is granted only to what's needed, and sign-in events and changes are logged.
Perimeter layer uses DDoS protection and firewalls to protect from network-based attacks.
Network layer limits communication between resources to reduce risk of attack spreading.
Compute layer focuses on securing virtual machines and implementing endpoint protection.
Application layer integrates security into development lifecycle to reduce vulnerabilities.
Data layer controls access to business and customer data and ensures regulatory requirements are met.

# Describe Microsoft Defender for Cloud #
* Defender for Cloud is a security posture management and threat protection tool that monitors your cloud, on-premises, hybrid, and multicloud environments
* Already natively integrated to Azure, deployment is easy, automatic Log Analytics agent deployment available for non-Azure environments
* Monitors and protects Azure PaaS services (e.g Azure App Service, Azure SQL, Azure Storage Account), Azure data services, and networks
* Can defend hybrid cloud environment by deploying Azure Arc and enabling Defender for Cloud features
* Can also protect resources running in other clouds (e.g AWS and GCP)
* Focuses on three main functions: continuously assess, secure, and defend
* Continuously assess: regular vulnerability scans for compute, data, and infrastructure with integrated vulnerability findings from Microsoft threat and vulnerability management
* Secure: builds policies based on Azure Policy controls, runs on management groups, subscriptions, and tenant-wide
* Defend: detects and resolves threats to resources, workloads, and services

# Knowledge Check #

1. Which Azure Active Directory tool can vary the credentials needed to log in based on signals, such as where the user is located?
>Conditional Access is a tool that Azure Active Directory uses to allow (or deny) access to resources based on identity signals. Conditional Access might challenge you for a second authentication factor if your sign-in signals are unusual or from an unexpected location.

2. Which security model assumes the worst-case security scenario, and protects resources accordingly?
>Zero Trust is a security model that assumes the worst case scenario and protects resources with that expectation.

3. A user is simultaneously assigned multiple roles that use role-based access control. What are their actual permissions? The role permissions are: Role 1 - read || Role 2 - write || Role 3 - read and write.
> Read and write: Role-based access control, using an allow model, grants all of the permissions assigned in all of the assigned roles.


