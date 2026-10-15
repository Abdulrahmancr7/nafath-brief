Version: NAFATH-V1
Track: Cybersecurity

## Overview
The government SSO service allows citizens to access multiple government services using one account. Software development and AI work together to identify suspicious login activities by analyzing login times, locations, devices, and failed attempts. However, AI needs limits on the citizens’ data it can use to protect privacy and comply with data protection laws. Mobile development also depends on a stable network connection to send login requests and receive authentication responses without delays or interruptions. Networking provides secure communication, but this alone cannot protect accounts if passwords are stolen. Therefore, cybersecurity adds multi-factor authentication, account monitoring, and phishing-resistant login methods to prevent unauthorized access. Data Management ensures citizens’ information is collected legitimately, stored securely, and shared only when necessary. Together, these fields help deliver a reliable service, with cybersecurity protecting citizens’ accounts.

## Software
OAuth 2.0 is designed for delegated access to resources, while OpenID Connect (OIDC) is designed for user login. OAuth 2.0 allows applications to access resources with a user's permission without sharing their password. OpenID Connect extends OAuth 2.0 by adding an identity layer to verify who the user is. For example, citizens can use one account to log in to multiple government websites. Both are used in single sign-on systems to support secure login and controlled access to services.

Resource: The OAuth 2.0 Authorization Framework (RFC 6749) - https://www.rfc-editor.org/rfc/rfc6749

## AI
The authority can use the NIST AI Risk Management Framework (AI RMF 1.0) to manage risks before launch. Govern establishes responsibilities, Map identifies risks, Measure evaluates performance and fairness, and Manage prioritizes risks and responses. The authority must address privacy and security risks, including falsely flagging innocent citizens and locking them out. It should also ensure human oversight and ongoing monitoring.

Resource: Artificial Intelligence Risk Management Framework (AI RMF 1.0) - https://www.nist.gov/itl/ai-risk-management-framework

## Mobile
Android’s runtime permission model limits the SSO app’s access to sensitive features such as the camera, microphone, and location. Permissions are declared in the app’s manifest, and dangerous permissions must be requested at runtime when users first use the relevant feature. Users can deny permission, so the app should offer alternatives, such as manual document entry. If the authority offers ID scanning, the app must request camera permission.

Resource: Permissions overview - Android Developers - https://developer.android.com/guide/topics/permissions/overview

## Networking
DNS over HTTPS (DoH) sends DNS queries through an encrypted HTTPS connection. DNS translates domain names into IP addresses. DoH helps protect citizens’ privacy by making it harder for network eavesdroppers to read or modify DNS queries. However, it does not hide the user’s IP address, encrypt all browsing activity, or automatically block phishing and malicious websites. The DNS provider can still see the queries it processes. DoH should be combined with other cybersecurity controls.

Resource: DNS Queries over HTTPS (DoH) - RFC 8484 - https://www.rfc-editor.org/rfc/rfc8484

## Cybersecurity
Phishing-resistant authentication binds each login to the genuine website, so a credential captured on a fake site cannot be used on the real one. FIDO2/WebAuthn passkeys and security keys use cryptographic verification to check the website’s origin. SMS codes, email codes, and authenticator-app codes are generally not phishing-resistant because attackers can steal or relay them. The government SSO authority should prioritize passkeys or security keys where practical and provide secure account recovery procedures to protect citizens’ accounts.

Resource: NIST SP 800-63B, Digital Identity Guidelines: Authentication and Lifecycle Management - https://pages.nist.gov/800-63-4/sp800-63b.html

## Data
Oman’s Personal Data Protection Law (Royal Decree 6/2022) sets general rules for protecting personal data. Circular 6/2024 requires civil service units to use privacy notices, security measures, and protection against data breaches. For government SSO, citizens’ data must be collected by legitimate and fair means. Any leak, loss, or hacking must be reported to the Electronic Defense Center. Data may be transferred outside Oman only in permitted cases and with the Center’s approval.

Resource: Personal Data Protection Circular (No. 6/2024) - https://www.mtcit.gov.om/library-3/guidelines-documentation-7/circulars-66/personal-data-protection-circular-765

## Misconception in My Track
Many people believe that any multi-factor authentication code protects against phishing. However, attackers can steal or relay manually entered codes because they do not bind the authenticator output to the specific session. Passkeys and security keys provide stronger protection through cryptographic methods, such as verifier name binding, which ties credentials to the website’s origin. Channel binding is another mechanism recognized by NIST. NIST SP 800-63B-4, Section 3.2.5, “Phishing Resistance,” explains these protections and why manually entered codes are not phishing-resistant.

## Open Question
If a citizen loses the device holding their passkey, how can the authority recover their account without weakening phishing resistance?
