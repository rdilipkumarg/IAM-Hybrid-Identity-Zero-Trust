
# Scaling Secure Access: Implementing Phish-Resistant MFA & Conditional Access Pipelines

Unified hybrid identity infrastructure: integrated on-premises Active Directory with Azure AD (via AD Connect), enabling seamless SSO for legacy and cloud apps and centralizing access control.

Enforced least privilege for admins: deployed Azure AD Privileged Identity Management (PIM) for all high-privilege roles, eliminating permanent admin accounts and enforcing just-in-time elevation with full audit logging.

Secured external access: enabled Azure AD B2B collaboration for partners/contractors and implemented Conditional Access policies (MFA, network location, device compliance), enforcing zero-trust controls across the hybrid environment.

# IAM-Hybrid-Identity-Zero-Trust
This project demonstrates the design and implementation of a hybrid Identity and Access Management (IAM) architecture integrating on-premises Active Directory with Azure Active Directory (Microsoft Entra ID).

The goal of this project is to build a centralized identity platform that supports secure authentication, role-based authorization, and Zero Trust access policies across both cloud and on-premise environments.

The architecture simulates how enterprises transition from traditional perimeter-based security to a modern Zero Trust identity model.


## Problem Statement

Many organizations operate in hybrid environments, where both on-premise infrastructure and cloud services must coexist. Managing identities across these environments introduces several security and operational challenges:

Fragmented identity management systems

Inconsistent authentication policies

Privileged accounts with excessive permissions

Lack of centralized identity governance

This project addresses these challenges by designing a hybrid identity architecture that:

Synchronizes on-premises identities with Azure AD

Enables Single Sign-On across cloud and legacy applications

Enforces Zero Trust Conditional Access policies

Secures privileged accounts using Just-in-Time access


##  Industry Use Case

Hybrid identity architectures are widely used in large enterprises such as:

Financial institutions

Government organizations

Healthcare providers

Large enterprise IT environments

These organizations typically operate with legacy infrastructure while gradually migrating to cloud platforms, requiring a secure bridge between on-premise identity systems and cloud identity providers.
## Architecture
The architecture centers around Azure Active Directory as the central Identity Provider integrated with on-premises Active Directory using directory synchronization.

Hybrid Identity Architecture Diagram.png

Key Components

On-Premises Active Directory

Azure Active Directory (Microsoft Entra ID)

Azure AD Connect (Directory Synchronization)

Conditional Access Policy Engine

Privileged Identity Management (PIM)

Enterprise Applications


## System Design
The system design defines how authentication requests flow between users, applications, and identity providers in a hybrid environment.

Hybrid Identity System Design Diagram.png

Authentication Flow

User attempts to access an enterprise application.

Application redirects authentication request to Azure Active Directory.

Azure AD validates the user identity (synchronized from on-prem AD).

Conditional Access policies evaluate security signals.

If policies are satisfied, Azure AD issues authentication tokens.

Application validates the token and grants access.

This system design ensures centralized identity verification while supporting hybrid infrastructure.
## Implementation
This section describes the technical implementation of the hybrid identity architecture.

Hybrid Identity Implementation Diagram.png

Key Implementation Components

Active Directory Domain Environment

Azure Active Directory Tenant

Azure AD Connect Configuration

Conditional Access Policy Configuration

Privileged Identity Management Setup

Enterprise Application Integration

Implementation Activities

The following tasks were completed as part of the project implementation:

Configured Azure AD Connect for identity synchronization

Integrated on-premises Active Directory with Azure AD

Implemented Single Sign-On across enterprise applications

Configured Conditional Access policies for Zero Trust enforcement

Enabled Privileged Identity Management (PIM) for administrative roles

Applied Role-Based Access Control (RBAC) to restrict privileges
## Security Controls Implemented
The following security controls were implemented to secure the hybrid identity environment:

Multi-Factor Authentication (MFA)

Conditional Access Policies

Privileged Identity Management (PIM)

Role-Based Access Control (RBAC)

Just-in-Time Privileged Access

Zero Trust Access Enforcement
## Tools and Technologies

Azure Active Directory (Microsoft Entra ID)

Active Directory Domain Services

Azure AD Connect

Azure Conditional Access

Azure Privileged Identity Management

Role-Based Access Control

OAuth 2.0 / OpenID Connect

Hybrid Identity Architecture
## Key IAM Concepts Demonstrated

Hybrid Identity Architecture

Single Sign-On (SSO)

Conditional Access Policies

Zero Trust Security Model

Privileged Access Management

Role-Based Access Control (RBAC)
## Future Improvements

Future improvements for this architecture could include:

Integrating identity monitoring with a SIEM platform

Implementing passwordless authentication

Adding identity governance automation

Integrating external identity federation
