WatchGuard Technologies Endpoint Security Endpoint Security Prime
AI-Powered Endpoint Detection and Response (EDR) User Manual ---
Compiled from Official WatchGuard Documentation July 2026

1.  Product Overview WatchGuard Endpoint Security Prime is an AI-powered
    endpoint protection and detection and response (EDR) solution. It
    combines proactive threat detection with automated, guided response
    actions, and is designed to deliver strong protection outcomes with
    reduced alert noise and manual effort. Prime sits in the middle of
    WatchGuard's Endpoint Security product line, which also includes
    Basic (foundational protection), 360 (adds Zero-Trust Application
    Service and lateral movement detection), and Elite (adds advanced
    investigation tools). All editions are deployed and managed with the
    same WatchGuard Agent and WatchGuard Cloud console. Prime is well
    suited to IT teams and MSP-managed environments that want automated
    detection and response along with clear incident visibility, without
    needing to run constant manual investigation.
2.  Key Features AI-powered EDR that continuously monitors endpoint
    activity to detect suspicious behavior and emerging threats. Clear
    incident visibility through intuitive dashboards and detailed
    timelines of what happened on an endpoint and why. Low-noise
    alerting that reduces false positives so security teams can focus on
    meaningful events. Root cause analysis with MITRE ATT&CK-mapped
    detections, indicator-of-compromise (IoC) correlation, and attack
    lifecycle visualization. Centralized endpoint management: deploy and
    manage protection across all endpoints from a single WatchGuard
    Cloud console. Guided response actions and built-in workflows to
    help contain and remediate threats without deep security expertise.
    Attack surface reduction tools, including vulnerability assessment,
    discovery of unmanaged endpoints, firewall, device control, and web
    filtering. Endpoint isolation and response, anti-exploit detections,
    and ThreatSync XDR remediations. Compatible with WatchGuard's
    Managed Detection and Response (MDR) service for organizations that
    want a fully managed option. Endpoint Security Edition Comparison
3.  Hardware and Software Components WatchGuard Agent --- the single
    agent used to deploy Endpoint Security, FireCloud, SSL VPN clients,
    and ThreatSync+ NDR collectors; it handles communication between the
    endpoint and WatchGuard Cloud and keeps installed software up to
    date. Endpoint Security protection module --- installed by the
    WatchGuard Agent; provides antivirus, EDR, and the other protection
    capabilities included in the Prime license. WatchGuard Cloud console
    --- used to license, deploy, configure groups and settings profiles,
    and monitor endpoints. Endpoint Security management UI (Configure \>
    Endpoint Security) --- used for computer/device groups, settings
    profiles, and installer downloads. Supported endpoint platforms ---
    Windows (x86 and ARM), macOS, Linux, Android, and iOS (the latter
    typically through the WatchGuard mobile device management
    integration).
4.  System Requirements
5.  Installation 5.1 Planning Log in to WatchGuard Cloud and allocate
    Endpoint Security Prime licenses to the managed account. Identify
    the physical and virtual Windows, macOS, Linux, Android, and iOS
    devices to protect, and confirm enough licenses are purchased. Plan
    endpoint groups and settings profiles before deployment, since the
    security policy applied to a computer depends on its group. If using
    third-party antivirus, decide whether to remove it automatically or
    configure exclusions so both products coexist. 5.2 Download and Run
    the Installer
6.  In WatchGuard Cloud, select Configure \> Endpoint Security, then
    select Computers and click Add Computers.
7.  Select the target platform (Windows, macOS, Linux, Android, or iOS).
8.  Select the endpoint group to add the computer to; the assigned
    security policy depends on this group.
9.  Optionally set an expiration date for the Windows installer link.
10. Click Download Installer, then run the installer on the target
    computer (double-click the file on Windows and macOS, or use a
    terminal on Linux). 5.3 Alternative Deployment Methods Remote
    installation with discovery and deployment (Windows computers only).
    Command-line installation through Active Directory Group Policy
    Objects (GPO), using the WatchGuard Endpoint Security .msi package.
    A shareable download link that can be sent to users so they can
    self-install the agent. Automated deployment through a template or
    gold image for new computer provisioning. Note: The computer used to
    define a GPO for deployment cannot have the WatchGuard Agent
    installed; uninstall the agent first, then reinstall it after adding
    the GPO.
11. Initial Setup After installation, the WatchGuard Agent performs
    agent integration, downloads the protection module and the latest
    malware signature file, and applies default or administrator-created
    settings. The endpoint appears on the Endpoints page (Monitor \>
    Endpoints) and in the Endpoint Security Computers list once
    installation completes. If a connectivity check fails, the agent
    reports which required URLs it could not reach, visible in the Agent
    Installation Console, Windows Event Viewer, or the Web Console.
    Confirm the endpoint is protected by checking its status and
    assigned license in the Endpoint Security management UI. Note:
    Endpoints added without an available license still show hardware and
    software inventory information but remain unprotected until a
    license is assigned.
12. Basic Configuration Groups: organize computers into groups
    (Configure \> Endpoint Security \> Computers \> My Organization \>
    Add Group) so the correct settings profile and policies apply
    automatically. Settings profiles: create and assign settings
    profiles to control protection behavior for each group. Agent
    Deployment page: for accounts with multiple WatchGuard products
    (e.g., Endpoint Security and FireCloud), use Configure \> Agent
    Deployment to control which software the WatchGuard Agent installs
    at the group, sub-group, or endpoint level (Install or Do Not
    Install). Exclusions: if running alongside third-party antivirus,
    configure matching exclusions in both products to avoid conflicting
    detections. Proxy configuration: add a corporate proxy for Windows
    computers if endpoints reach the internet through a proxy server.
    MITRE ATT&CK mapping and IoC correlation: review how detections map
    to the attack lifecycle to prioritize investigation.
13. Common Use Cases
14. Daily Operations Monitor endpoint status, last agent connection, and
    installed products from the Endpoints page in WatchGuard Cloud.
    Review new detections and alerts in the Endpoint Security dashboard,
    prioritizing incidents by MITRE ATT&CK context. Use guided response
    actions to isolate, contain, or remediate affected endpoints. Check
    that endpoints continue to receive the latest signature files and
    protection module updates. Review and adjust group settings profiles
    as new device types or use cases are added. Export endpoint lists to
    CSV for reporting or license auditing as needed.
15. Troubleshooting
16. Best Practices Plan endpoint groups and settings profiles before
    mass deployment to ensure the right policies apply automatically.
    Use the Agent Deployment page to control product installation
    centrally when an account has more than one WatchGuard product
    license. Configure exclusions carefully when running alongside
    third-party antivirus to avoid false detections. Regularly review
    low-noise alerts and MITRE ATT&CK-mapped incidents rather than
    relying solely on automated remediation. Keep enough licenses
    purchased for all devices you intend to protect, and monitor for
    unlicensed endpoints. Consider WatchGuard's MDR service if the
    organization needs 24x7 monitoring beyond what internal teams can
    provide. Test deployment methods (local installer, GPO, remote
    discovery) in a pilot group before an organization-wide rollout.
17. Frequently Asked Questions Q: What is the difference between
    Endpoint Security Prime and 360 or Elite? Prime adds anti-exploit
    detection, endpoint isolation and response, MITRE ATT&CK-mapped
    alerts, and ThreatSync XDR remediations on top of Basic. The 360
    edition adds Zero-Trust Application Service and lateral movement
    detection and containment, while Elite adds advanced investigation
    tools on top of 360. Q: Can Endpoint Security Prime run alongside
    another antivirus product? Yes. You can either remove the existing
    antivirus automatically (for supported products) or configure
    exclusions in both products so they coexist without conflicting. Q:
    Does the WatchGuard Agent need to be reinstalled for every
    WatchGuard product? No. There is a single WatchGuard Agent for
    Endpoint Security products, FireCloud, SSL VPN clients, and
    ThreatSync+ NDR collectors; the Agent Deployment page controls which
    software it installs on each endpoint. Q: What happens if I don't
    have enough licenses for all my devices? You can still install the
    WatchGuard Agent on unlicensed computers. They display hardware and
    software inventory information but are not actively protected until
    a license is assigned. Q: Is Endpoint Security Prime compatible with
    a managed detection and response service? Yes. Endpoint Security
    Prime (along with 360 and Elite) is compatible with WatchGuard's
    Managed Detection and Response (MDR) service.
