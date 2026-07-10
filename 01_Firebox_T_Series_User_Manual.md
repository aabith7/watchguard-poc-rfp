WatchGuard Technologies Network Security Firebox T Series Tabletop
Network Security Appliances for Small and Mid-Size Offices User Manual
--- Compiled from Official WatchGuard Documentation July 2026

1.  Product Overview The WatchGuard Firebox T Series is a family of
    compact, tabletop Unified Threat Management (UTM) firewall
    appliances designed for small offices, home offices, branch
    locations, and distributed mid-market networks. The T Series is
    built and supported by WatchGuard for managed service providers
    (MSPs) and IT teams, and it delivers fast deployment, strong
    performance, and AI-driven threat detection in a small physical
    footprint. The current tabletop line-up includes the T115-W, T125,
    T145, and T185 models, alongside earlier tabletop models still sold
    and supported, such as the T45-CW, NV5, and Wi-Fi variants (T115-W,
    T125-W, T145-W). Models are differentiated primarily by throughput,
    port count, memory, and wireless capability, allowing organizations
    to choose the right size of appliance for their network. Every
    Firebox T Series appliance can be managed locally through Fireware
    Web UI/WatchGuard System Manager, or centrally through WatchGuard
    Cloud, which provides a single hub for policy configuration,
    monitoring, and reporting across many devices.
2.  Key Features AI-powered threat detection integrated with WatchGuard
    ThreatSync (XDR), combining Firebox telemetry with endpoint and
    identity data. Unified Threat Management: firewall, VPN (Branch
    Office VPN, IPSec, SSL), gateway antivirus, intrusion prevention,
    and application control in one appliance. Integrated SD-WAN for
    optimizing and load-balancing multiple WAN connections and reducing
    reliance on costly MPLS or 4G/LTE links. High-speed Gigabit Ethernet
    ports; select models add Wi-Fi 6 or Wi-Fi 7 wireless and PoE for
    access points and IoT devices. Zero-touch, cloud-managed deployment
    through WatchGuard Cloud, plus locally-managed options through
    Fireware Web UI and WatchGuard System Manager (WSM). Built-in
    logging and reporting with 100+ dashboards and reports, including
    PCI and HIPAA compliance report templates. Transparent, bundled
    licensing (Basic Security Suite / Total Security Suite) with no
    hidden feature-based licensing traps. Energy-efficient, fanless or
    ultra-quiet metal chassis designs across the current generation.
    Optional WatchGuard NDR add-on that analyzes NetFlow data with
    machine learning to detect lateral movement, command-and-control
    traffic, and other hidden internal threats.
3.  Hardware and Software Components 3.1 Hardware 3.2 Software Fireware
    OS --- the operating system that runs on the Firebox and enforces
    firewall policy. Fireware Web UI --- browser-based interface for
    local device configuration. WatchGuard System Manager (WSM) ---
    Windows application for local management, including Policy Manager
    and the Quick Setup Wizard. WatchGuard Cloud --- cloud-based
    management console for cloud-managed devices, licensing, and
    reporting.
4.  System Requirements Note: Requirements vary slightly by model and
    Fireware version. Always confirm current minimum Fireware and
    browser requirements in the WatchGuard Help Center before
    deployment.
5.  Installation 5.1 Before You Begin Decide on a physical location for
    the appliance, near power and network cabling. Record your existing
    network IP address scheme (external, trusted, and any optional
    interfaces). Activate the Firebox: go to
    https://myproducts.watchguard.com/activate, log in to your
    WatchGuard account, and enter the appliance serial number to
    generate a feature key. 5.2 Physical Setup Connect Firebox interface
    0 (external) to a network or modem with internet access. Power on
    the Firebox with factory-default settings. Connect Firebox interface
    1 to your administration computer (or connect over Wi-Fi where
    supported), using a computer configured for DHCP. 5.3 Choosing a
    Management Method Cloud-Managed (recommended) --- the Firebox is
    added to WatchGuard Cloud first; it then downloads its configuration
    automatically once connected. Locally-Managed --- a new
    configuration is created directly on the device using the Web Setup
    Wizard or the WSM Quick Setup Wizard.
6.  Initial Setup 6.1 Cloud-Managed Quick Start
7.  In WatchGuard Cloud, add a new Firebox as a cloud-managed device and
    complete the Add Device wizard (device name, time zone, and network
    settings).
8.  Start the Firebox with factory-default settings and connect
    interface 0 to a network with internet access.
9.  The Firebox automatically connects to WatchGuard Cloud and downloads
    the configuration created in the wizard.
10. If the device cannot obtain an address through DHCP, open
    https://10.0.1.1:8080, log in with the default user name admin and
    passphrase readwrite, and use the Web Setup Wizard to select
    Cloud-Managed and enter external network settings manually.
11. Confirm the deployment status changes from "Waiting for Initial
    Connection" to a successful, connected state on the Deployment
    History page. 6.2 Locally-Managed Quick Start Open a browser and go
    to https://10.0.1.1:8080 while connected to interface 1. Log in with
    user name admin and passphrase readwrite (the Web Setup Wizard
    starts automatically on a factory-default device). Select
    Locally-Managed (Create New Configuration), then follow the wizard
    to set external and trusted interface settings, device passphrases,
    and a time zone. Note: Change the default admin (readwrite) and
    status (readonly) passphrases immediately after setup, and use
    unique, strong passphrases for every Firebox.
12. Basic Configuration Network interfaces: configure mixed routing mode
    (each interface on its own subnet, using NAT) --- the default and
    most common mode --- or drop-in/bridge mode for specific network
    layouts. Firewall policies: the setup wizard automatically enables
    default, secure firewall policies; review and adjust policies for
    the applications and services your organization uses. Security
    subscriptions: enable licensed services such as Gateway AntiVirus,
    IntelligentAV, APT Blocker, Intrusion Prevention Service,
    spamBlocker, WebBlocker, and Application Control according to your
    Security Suite subscription. VPN configuration: set up Branch Office
    VPN (BOVPN) for site-to-site connectivity, and Mobile VPN (IPSec or
    SSL) for remote users. SD-WAN: configure multiple WAN interfaces or
    actions to load-balance or fail over traffic across available
    internet connections. Administrative accounts: create additional
    operator accounts with role-based permissions in WatchGuard Cloud
    for delegated administration.
13. Common Use Cases
14. Daily Operations Monitor device and network health from the
    WatchGuard Cloud Dashboard or locally through Fireware Web UI /
    Firebox System Manager. Review daily and historical traffic, threat,
    and VPN reports (100+ built-in dashboards and reports). Check
    Deployment History after any configuration change to confirm it was
    applied successfully. Review and respond to security event
    notifications generated by subscription services (e.g., IPS, Gateway
    AntiVirus, APT Blocker). Periodically verify that Fireware OS and
    signature updates are current. Rotate and manage administrator
    passphrases and operator roles as part of routine security hygiene.
15. Troubleshooting
16. Best Practices Always change the default admin and status
    passphrases before placing the Firebox into production. Keep
    Fireware OS up to date to maintain compatibility with WatchGuard
    Cloud and to receive the latest security fixes. Use WatchGuard Cloud
    centralized management for multi-site or MSP-managed deployments to
    maintain consistent policy templates. Record your network IP address
    plan before and after configuration for easier troubleshooting.
    Enable the full set of licensed security services (IPS, Gateway
    AntiVirus, APT Blocker, WebBlocker) rather than firewalling alone.
    Regularly review compliance and traffic reports to detect abnormal
    usage patterns. Back up your configuration before making major
    changes, and store backup images securely.
17. Frequently Asked Questions Q: What is the difference between
    cloud-managed and locally-managed Fireboxes? Cloud-managed Fireboxes
    are configured, monitored, and managed entirely from WatchGuard
    Cloud. Locally-managed Fireboxes are configured with Fireware Web UI
    or WatchGuard System Manager, and can optionally be added to
    WatchGuard Cloud for monitoring and reporting only. Q: Can I migrate
    a locally-managed Firebox to cloud management? Yes. WatchGuard
    provides a documented migration path, though a new configuration is
    created in WatchGuard Cloud rather than a direct import of the
    existing local configuration. Q: Do all T Series models support
    Wi-Fi? No. Wireless is available on "-W" model variants (for
    example, T115-W). Some higher-throughput models, such as the T185,
    are wired-only. Q: What is included in the Firebox license? Firebox
    appliances are sold with a Basic Security Suite or Total Security
    Suite subscription, which bundles core services such as Gateway
    AntiVirus and spamBlocker, along with standard or premium support
    (LiveSecurity). Q: Where can I get official Firebox documentation?
    The WatchGuard Help Center (watchguard.com/help/docs) hosts current
    Fireware and WatchGuard Cloud documentation, including setup guides,
    datasheets, and release notes.
