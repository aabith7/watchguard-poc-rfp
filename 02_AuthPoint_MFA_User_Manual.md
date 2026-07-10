WatchGuard Technologies Identity Security AuthPoint MFA Cloud-Based
Multi-Factor Authentication and Zero Trust Identity Verification User
Manual --- Compiled from Official WatchGuard Documentation July 2026

1.  Product Overview AuthPoint is WatchGuard's cloud-native multi-factor
    authentication (MFA) service. It verifies user identities with push
    notifications, one-time passcodes (OTP), QR codes, hardware tokens,
    and phishing-resistant passkeys, and it is managed entirely from
    WatchGuard Cloud. AuthPoint protects logins to Windows and macOS
    computers, VPNs, cloud applications (through SAML and OIDC), and
    Microsoft 365 and Azure through certified Microsoft Entra ID
    External MFA. It also provides an Identity Provider (IdP) portal for
    web single sign-on (SSO) to MFA-protected applications. AuthPoint is
    available as a standalone Multi-Factor Authentication (MFA) product,
    or as part of Total Identity Security, WatchGuard's broader identity
    security bundle that adds capabilities such as risk-based
    authentication and dark web monitoring.
2.  Key Features Phishing-resistant passkeys --- users authenticate with
    a fingerprint or face scan instead of a password or code. Zero Trust
    adaptive policies --- access decisions consider device, location,
    and behavior context at every login. Certified Microsoft Entra ID
    External MFA --- one MFA solution for Microsoft 365, Azure, and
    other applications, without requiring SAML. Unique Mobile Device DNA
    --- ties each authentication to a specific physical device, so a
    cloned phone cannot be used to authenticate. Cross-platform coverage
    --- a single mobile app protects Windows and macOS logins, VPN
    access, and cloud applications. Cloud multi-tenant management ---
    MSPs can deploy and manage identity security for many customer
    accounts from one WatchGuard Cloud console. Multiple authentication
    methods --- push notification, OTP, QR code, hardware token, and
    passkey, plus support for third-party tokens in the AuthPoint app.
    Identity Provider (IdP) portal --- gives users single sign-on access
    to a list of SAML resources they are authorized to use.
3.  Hardware and Software Components
4.  System Requirements
5.  Installation 5.1 Cloud Service Setup Log in to WatchGuard Cloud and
    confirm your account has an active AuthPoint license. Navigate to
    the AuthPoint section to begin adding users, groups, and resources.
    5.2 Install the AuthPoint Gateway (if using RADIUS or LDAP) Download
    the AuthPoint Gateway installer from WatchGuard Cloud. Install the
    Gateway on a server inside your network that can reach both your
    LDAP/Active Directory environment and the internet. Configure the
    Gateway to connect to your RADIUS clients and LDAP databases as
    required by your resources. 5.3 Install the Logon App (if enforcing
    MFA at device logon) Install the Logon App component on each Windows
    computer or server where MFA should be required at logon. Confirm
    the computer has internet access, since the Logon App must reach
    AuthPoint to check authentication policies before a user's first
    logon. Configure the corresponding Logon App resource in AuthPoint
    to link the installed component to an authentication policy.
6.  Initial Setup 6.1 Add Your First User
7.  In WatchGuard Cloud, go to the AuthPoint Users page and add a new
    user.
8.  Select MFA user (rather than Non-MFA user) so the account can
    authenticate with AuthPoint.
9.  Enter the user's first name, last name, a unique user name, and an
    email address.
10. Leave the default options selected so AuthPoint automatically
    creates a token for the user and emails them an activation link.
11. Click Save. AuthPoint sends the user two emails: one to set their
    AuthPoint password, and one to activate their token. 6.2 Activate
    the Mobile Token
12. Download and install the AuthPoint mobile app on your phone.
13. Open the Set Password email and follow the link to create your
    AuthPoint password.
14. Open the Activation email and click the activation link to reach the
    Welcome to AuthPoint page.
15. On a phone, tap Activate to open the app and activate the token
    directly; on a computer, open the AuthPoint app and tap Activate,
    then scan the QR code shown on screen.
16. Optionally set a custom name and image for the new token once
    activation completes. Note: Users synced from Active Directory or an
    LDAP database do not receive a Set Password email --- they
    authenticate with their existing directory password. 6.3 Sync Users
    from Active Directory or LDAP (Optional) Configure an external
    identity connection to your Active Directory or LDAP database in
    AuthPoint. Add a query or group sync to identify which users and
    groups to import. Choose whether AuthPoint should automatically
    assign a mobile token and send the activation email to synced users.
    AuthPoint creates a user account for each person identified by the
    sync at the configured synchronization interval.
17. Basic Configuration Groups: organize users into groups to apply
    authentication policies consistently. Resources: add the
    applications, VPNs, servers, or the IdP portal that AuthPoint should
    protect. Authentication policies: define which groups must use MFA
    for which resources, and which authentication methods are allowed.
    IdP portal: enable the portal so users can see and access their
    available SAML resources from a single page, and optionally activate
    their own tokens there. Hardware tokens: assign and, if the IdP
    portal is unavailable, manually activate hardware tokens for users
    who need them. Additional devices: users with more than one mobile
    device can activate a separate token (up to 20 WatchGuard tokens per
    user) for each device.
18. Common Use Cases
19. Daily Operations Monitor user and token status (Activated, Pending)
    on the Users page in WatchGuard Cloud. Add new users and resend Set
    Password or Activation emails as new employees join or reset their
    devices. Approve or review authentication activity and investigate
    unexpected push notification requests. Add or revoke tokens promptly
    when an employee's device is lost, replaced, or when the employee
    leaves the organization. Review and update authentication policies
    as new resources or groups are added. Check group sync status if
    using Active Directory/LDAP integration to confirm new employees are
    provisioned automatically.
20. Troubleshooting
21. Best Practices Enable Microsoft Entra ID External MFA for Microsoft
    365 and Azure rather than relying on Microsoft Authenticator alone,
    to centralize policy management. Use passkeys or push-based
    authentication where possible for phishing resistance, rather than
    OTP alone. Sync users from Active Directory or LDAP where feasible
    to reduce manual account management. Delete test or temporary
    AuthPoint users before syncing to a live authentication database.
    Promptly delete or reassign tokens for lost devices and departing
    employees. Use groups and authentication policies to apply the right
    level of MFA enforcement to the right resources. For MSPs, use
    WatchGuard Cloud's multi-tenant structure to standardize AuthPoint
    deployment across customer accounts.
22. Frequently Asked Questions Q: What is the difference between an MFA
    user and a Non-MFA user? MFA users authenticate with AuthPoint and
    consume an AuthPoint user license. Non-MFA users, such as service
    accounts, authenticate only with a password and cannot access
    resources that require MFA. Q: How is AuthPoint different from
    Microsoft Authenticator? Microsoft Authenticator focuses on
    Microsoft environments. AuthPoint additionally covers VPN access,
    Windows and macOS logon, remote desktop, and third-party
    applications from a single platform, and gives MSPs multi-tenant
    management across customer accounts. Q: How quickly can AuthPoint be
    deployed? For cloud-only environments there is nothing to install
    on-premises. Administrators can configure users in WatchGuard Cloud,
    assign tokens, and begin protecting logins the same day. Q: Can a
    user use more than one device for authentication? Yes. A user can
    activate a separate WatchGuard token for each additional device, up
    to 20 WatchGuard tokens per user, and can approve a push
    notification from any of their active devices. Q: What happens if a
    user's phone is lost or replaced? An administrator can create a new
    token for the user (if there is no token already pending), which the
    user then activates on their new device. To move an existing token
    to a new device rather than adding another one, use the token
    migration process.
