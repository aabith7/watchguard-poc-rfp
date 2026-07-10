WatchGuard Technologies Platform Security / Centralized Management
WatchGuard Cloud Centralized Management, Monitoring, and Reporting for
the WatchGuard Platform User Manual --- Compiled from Official
WatchGuard Documentation July 2026

1.  Product Overview WatchGuard Cloud is WatchGuard's centralized,
    cloud-based management console. It gives administrators and MSPs one
    place to deploy, configure, monitor, and report on Fireboxes, Wi-Fi
    6 access points, Endpoint Security, AuthPoint MFA, FireCloud, and
    other WatchGuard products across many customer accounts. WatchGuard
    Cloud uses a multi-tier account architecture. Service Provider
    accounts can manage many Subscriber accounts, allocate licensed
    devices and endpoints, and delegate access, while a Subscriber
    account configures and manages its own products directly. As the hub
    of WatchGuard's Unified Security Platform, WatchGuard Cloud also
    hosts ThreatSync XDR, which correlates activity across network,
    endpoint, and identity security layers to prioritize alerts and
    speed up detection and response.
2.  Key Features Unified security visibility across customers, sites,
    and services from a single dashboard. Precision policy management
    that helps prevent configuration drift and misconfigurations across
    many devices and accounts. ThreatSync XDR: correlates activity
    across WatchGuard security layers to reduce alert noise and
    prioritize what matters most. Centralized network security
    management for cloud-managed and locally-managed Fireboxes and
    FireClusters, including monitoring, reporting, and system actions
    such as upgrades and reboots. Centralized Wi-Fi management,
    including access point configuration, SSID and radio settings, and
    guest access and reporting tools. Centralized endpoint security
    management with a single WatchGuard Agent for deployment across
    Windows, macOS, Linux, Android, and iOS. Centralized identity
    security management for AuthPoint MFA, including user sync, policy
    configuration, and enforcement. Zero trust access management for
    FireCloud Total Access, so security policies follow users across
    remote, cloud, and on-premises environments. Scheduled and on-demand
    reporting, with reports emailed to specified recipients on a daily,
    weekly, monthly, or immediate basis. Role-based operator accounts
    and account groups for delegated, multi-tenant administration.
3.  Hardware and Software Components WatchGuard Cloud web console
    (cloud.watchguard.com) --- the primary interface for configuration,
    monitoring, and reporting. Managed devices --- Fireboxes,
    FireClusters, and Wi-Fi 6 access points added as cloud-managed or
    locally-managed devices. WatchGuard Agent --- the unified agent used
    to deploy Endpoint Security, FireCloud, SSL VPN, and ThreatSync+ NDR
    collector software to endpoints. AuthPoint --- identity security
    service managed from within WatchGuard Cloud. ThreatSync /
    ThreatSync XDR --- the correlation and detection engine built into
    WatchGuard Cloud. Operator accounts and account groups --- used to
    control who can view or manage which accounts and devices.
4.  System Requirements
5.  Installation WatchGuard Cloud itself is a cloud service with no
    local software to install; "installation" instead refers to setting
    up your account structure and connecting your devices and endpoints.
    5.1 Create Your Account Log in to your existing WatchGuard account,
    or create a new one, at cloud.watchguard.com. If you are a Service
    Provider, set up your top-level Service Provider account before
    creating Subscriber accounts for your customers. Every account must
    have at least one Owner or Administrator operator with full
    privileges. 5.2 Connect Your Products Activate each product
    (Firebox, access point, Endpoint Security license, AuthPoint
    license) in your WatchGuard account before adding it to WatchGuard
    Cloud. Add Fireboxes and FireClusters as cloud-managed or
    locally-managed devices. Add Wi-Fi 6 access points as cloud-managed
    devices, ensuring each has a current WatchGuard Standard or USP
    Wi-Fi license. Deploy the WatchGuard Agent to endpoints to connect
    them for Endpoint Security or FireCloud management. Configure
    AuthPoint users, groups, and resources within the same WatchGuard
    Cloud account.
6.  Initial Setup 6.1 Set Up Operators and Roles
7.  In WatchGuard Cloud, go to account or operator management to review
    the built-in roles: Administrator (full permissions), Helpdesk (full
    permissions to configure services, read-only elsewhere), and Auditor
    (read-only throughout the account).
8.  Add operators for each team member who needs access, and assign the
    role matching their responsibilities.
9.  For Service Providers, set up account groups to assign operator
    permissions and endpoint policies across multiple managed accounts
    at once.
10. Confirm that every account has at least one Owner or Administrator
    with full privileges. 6.2 Add Your First Devices Select Configure \>
    Devices to add Fireboxes, FireClusters, or access points to your
    account as cloud-managed or locally-managed devices. For Service
    Providers, allocate each device to the correct Subscriber account
    after activation. Verify connection status on the Devices or
    Deployment History page after each device is added. 6.3 Explore
    Reporting From the Administration menu, select Scheduled Reports to
    configure recurring reports (daily, weekly, monthly, or on demand)
    and specify email recipients. Review the built-in dashboards for
    network, endpoint, and identity security visibility.
11. Basic Configuration Account structure: organize Subscriber accounts
    logically (for example, by customer) if operating as a Service
    Provider or MSP. Operator roles: assign the least-privilege role
    needed for each person (Auditor for read-only oversight, Helpdesk
    for support staff, Administrator for full control). Device policies:
    configure Firebox firewall policies, access point SSIDs, and
    endpoint settings profiles consistently, ideally using shared
    templates or sites where available. ThreatSync XDR: review
    correlated detections across network, endpoint, and identity layers
    rather than triaging each product's alerts separately. Agent
    Deployment: for accounts with multiple products relying on the
    WatchGuard Agent (Endpoint Security, FireCloud), configure
    deployment behavior at the group, sub-group, or endpoint level. Beta
    features: Administrators or Owners can enable or disable beta
    features and applications from the Beta Features page to preview
    upcoming capabilities.
12. Common Use Cases
13. Daily Operations Review the WatchGuard Cloud dashboard for the
    current status of devices, endpoints, and identity security across
    all managed accounts. Triage ThreatSync XDR correlated alerts,
    prioritizing incidents with the highest confidence and severity.
    Check Deployment History after configuration changes to confirm
    updates were applied successfully to devices. Review scheduled
    reports and distribute them to stakeholders or customers as needed.
    Manage operator accounts, adding or removing access as staff
    responsibilities change. Monitor license allocation and renewal
    status across Subscriber accounts.
14. Troubleshooting
15. Best Practices Assign operator roles using least privilege: use
    Auditor or Helpdesk roles for staff who do not need full
    configuration access. Use account groups to manage permissions and
    policies consistently across many Subscriber accounts. Standardize
    configuration with templates, sites, or settings profiles rather
    than configuring each device manually. Regularly review ThreatSync
    XDR correlated alerts rather than monitoring each product's console
    separately. Set up scheduled reports early so compliance and
    management reporting is automatic rather than ad hoc. Keep device
    firmware and the WatchGuard Agent up to date to ensure compatibility
    with the latest WatchGuard Cloud features. Periodically audit
    operator accounts and remove access for staff who no longer need it.
16. Frequently Asked Questions Q: What is the difference between a
    Service Provider account and a Subscriber account? A Service
    Provider account can manage many Subscriber accounts, allocate
    licensed devices, and delegate access. A Subscriber account (My
    Account) is where an organization configures and manages its own
    products directly. Q: What are the built-in operator roles? The
    built-in Subscriber account roles are Administrator (full
    permissions), Helpdesk (full permissions to configure services,
    read-only elsewhere), and Auditor (read-only throughout the
    account). Every account must have at least one Owner or
    Administrator. Q: Can WatchGuard Cloud manage both cloud-managed and
    locally-managed Fireboxes? Yes. Both device types support
    monitoring, reporting, and system actions such as upgrades and
    reboots in WatchGuard Cloud, though only cloud-managed devices have
    their full configuration managed from the cloud. Q: What is
    ThreatSync XDR and how does it relate to WatchGuard Cloud?
    ThreatSync XDR is built into WatchGuard Cloud and correlates
    activity across network, endpoint, and identity security layers to
    reduce alert noise and prioritize the most important threats for
    investigation. Q: Can I preview upcoming WatchGuard Cloud features
    before general release? Operators with Administrator or Owner
    permissions can enable or disable features on the Beta Features page
    to preview and test upcoming capabilities, with some limitations for
    delegated accounts.
