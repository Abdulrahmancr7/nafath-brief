Version: NAFATH-V1
Track: Cybersecurity

## Overview
The government SSO service allows citizens to access multiple government services using one account. Software development and AI work together to identify suspicious login activities by analyzing login times, locations, devices, and failed attempts. However, AI needs limits on the citizens’ data it can use to protect privacy and comply with data protection laws. Mobile development also depends on a stable network connection to send login requests and receive authentication responses without delays or interruptions. Networking provides secure communication, but this alone cannot protect accounts if passwords are stolen. Therefore, cybersecurity adds multi-factor authentication, account monitoring, and phishing-resistant login methods to prevent unauthorized access. Data Management ensures citizens’ information is collected lawfully, stored securely, and shared only when necessary. Together, these fields help deliver a reliable, secure, and user-friendly government service

## Software
OAuth 2.0 is designed for delegated access to resources, while OpenID Connect (OIDC) is designed for user login. OAuth 2.0 allows applications to access resources with a user's permission without sharing their password. OpenID Connect extends OAuth 2.0 by adding an identity layer to verify who the user is. For example, citizens can use one account to log in to multiple government websites. Both are used in single sign-on systems to support secure login and controlled access to services.
Resource: The OAuth 2.0 Authorization Framework (RFC 6749) - https://www.rfc-editor.org/rfc/rfc6749

## AI
The authority can use the NIST AI Risk Management Framework (AI RMF 1.0) to manage risks before launch. Govern establishes responsibilities, Map identifies risks, Measure evaluates performance and fairness, and Manage prioritises risks and responses. The authority must address privacy and security risks, including falsely flagging innocent citizens and locking them out. It should also ensure human oversight and ongoing monitoring.
Resource: Artificial Intelligence Risk Management Framework (AI RMF 1.0) - https://www.nist.gov/itl/ai-risk-management-framework

## Mobile
Android’s runtime permission model limits the SSO app’s access to sensitive features such as the camera, microphone, and location. Permissions are declared in the app’s manifest, and dangerous permissions must be requested at runtime when users first use the relevant feature. Users can deny permission, so the app should offer alternatives, such as manual document entry. If the authority offers ID scanning, the app must request camera permission.
Resource: Permissions overview - Android Developers - https://developer.android.com/guide/topics/permissions/overview

## Networking

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
