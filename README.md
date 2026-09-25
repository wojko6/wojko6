# Hi, I'm Wojciech Kołłątaj 👋

I build practical infrastructure, Linux, networking and security projects with a strong focus on **reproducibility, hardening, recovery and evidence-based validation**.

My work spans Fedora Workstation engineering, network segmentation, Tailscale/ZTNA, DNS/DNSSEC, firewall policy, packet analysis, disaster recovery and real-time network troubleshooting.

## Featured projects

### [Advanced ASUS Edge Gateway & Zero-Trust Lab](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure)

A reproducible Home/SMB security-edge lab built on an ASUS TUF-AX5400 with Asuswrt-Merlin.

Highlights:

- Tailscale-based remote access and exit-node capability with project-owned least-privilege firewall chains
- dnsmasq + Unbound integration with DNSSEC validation
- LAN classic-DNS enforcement and direct DNS-over-TLS / TCP 853 blocking
- SSD-backed Entware deployment, swap-backed service startup and recovery workflows
- backup, restore, rollback, health-check and sanitized evidence tooling
- GitHub Actions validation and mock/static regression tests
- live validation of management authorization, DNS paths and exit-node routing
- GeForce NOW Ethernet/Wi-Fi stability analysis
- Xbox Cloud Gaming WebRTC analysis using RTP, ICE, jitter, RTT, bitrate and decoder telemetry

Latest documented live checkpoint: project health check completed with **0 failures and 0 warnings**.

---

### [Fedora Workstation Setup](https://github.com/wojko6/fedora-workstation-setup)

A reproducible Fedora Workstation desired-state, hardening, localization and disaster-recovery project.

Highlights:

- Fedora 44 / GNOME Shell 50.5 / Wayland reference baseline
- reproducible package, Flatpak, GNOME extension and dconf state
- security controls covering SELinux, Secure Boot, signed NVIDIA modules, firewalld and network exposure
- version-aware GNOME extension restore and exact-state validation
- extensive Polish localization engineering for GNOME extensions and desktop applications
- controlled Helium/Chromium DataPack localization with strict producer/version validation
- clean-room disaster-recovery validation in a separate VM
- upgrade and total-failure recovery runbooks
- physical-host verification integrated into the repository

Current accepted physical verifier:

```text
PASS=256 WARN=0 FAIL=0 SKIP=0
VERIFY_RC=0
```

---

### [OPNsense + MikroTik Segmentation Lab](https://github.com/wojko6/OPNsense-MikroTik-Segmentation-Lab)

A completed GNS3 network-security lab combining OPNsense with MikroTik RouterOS CHR.

Highlights:

- multi-segment routing
- stateful firewall policy
- trusted-LAN isolation
- controlled Internet access
- NAT and DHCP
- RouterOS management hardening
- firewall logging and validation evidence
- restricted SSH / WinBox administration

**Status:** Completed and validated ✅

## Selected engineering work

### Disaster recovery and reproducibility

I treat recovery as part of the design rather than an afterthought. My Fedora project includes clean-room restore validation, integrity-checked recovery sets, fail-closed restore helpers, SELinux recovery steps and explicit acceptance criteria.

### Network security and DNS

My router work covers Tailscale/ZTNA, project-owned firewall policy, DNS interception, DNSSEC-validating Unbound, direct DoT controls, logging, backup/recovery and controlled packet-level validation.

### Real-time network diagnostics

I have used packet captures, interface counters, latency sampling and application telemetry to investigate latency-sensitive workloads including GeForce NOW and Xbox Cloud Gaming.

### Localization engineering

My Fedora work includes exact-version gettext and resource audits, GNOME extension localization, application resource validation, strict drift detection and physical UI acceptance checks instead of relying only on static translation files.

## Technologies

**Linux & Systems:** Fedora, GNOME, Wayland, systemd, SELinux, Secure Boot, Btrfs, Bash  
**Networking:** TCP/IP, routing, DNS, DNSSEC, DHCP, NAT, firewalls, OPNsense, MikroTik RouterOS, Tailscale  
**Security:** ZTNA, least privilege, hardening, threat modeling, recovery, evidence-based validation  
**Diagnostics:** Wireshark, tshark, tcpdump, iproute2, nftables/iptables, WebRTC Internals  
**Automation & DevOps:** Git, GitHub, GitHub Actions, shell scripting, validation and rollback workflows  
**Virtualization / Labs:** GNS3, VirtualBox, VMware, Windows, Active Directory

## Current focus

- strengthening the ASUS Edge Gateway validation and observability model
- maintaining a reproducible and recoverable Fedora Workstation baseline
- expanding network and real-time traffic analysis case studies
- developing practical portfolio projects for infrastructure, networking and security roles

## Roles I'm interested in

- IT Support / Help Desk
- Junior System Administrator
- Junior Network Administrator / Network Engineer
- Junior SOC / Cybersecurity
- Junior Infrastructure / Security Engineer

## Contact

- GitHub: [github.com/wojko6](https://github.com/wojko6)
- Email: wojtekkotaj6@gmail.com
