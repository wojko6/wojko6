# Hi, I'm Wojciech Kołłątaj 👋

**Linux · Networking · IT Support · IT Infrastructure · Security**

I troubleshoot, maintain, and document Linux workstations and network infrastructure, with a practical focus on **network diagnostics, reliable operations, automation, access control, and recovery**. My projects combine a working ASUS-based home-lab gateway, a Fedora workstation, and isolated network/security experiments.

I value **reproducible procedures and verifiable results**: changes are tested against explicit criteria, recovery steps are documented, and real-system observations are kept separate from experiments.

**Hands-on skills demonstrated:** Linux troubleshooting and desktop support · TCP/IP, DNS and VPN diagnostics · Grafana/Loki monitoring and incident investigation · Bash/Python scripting · backup, restore and rollback procedures.

## Featured projects

### [Advanced ASUS Edge Gateway & Zero-Trust Lab](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure)

A working Home/SMB-style security-edge lab on an **ASUS TUF-AX5400** with Asuswrt-Merlin (GNUton). It is an engineering lab, not a high-availability or enterprise-certified appliance.

- **Networking and access control:** Tailscale remote access/exit node, restricted management paths, firewall policy, and controlled DNS routing.
- **DNS operations:** Pi-hole, dnsmasq, Unbound **1.26.2** with DNSSEC validation, and DNS Guard v3.2 with documented recovery behavior and limitations.
- **Monitoring and incident analysis:** syslog-ng, Alloy, Loki, Grafana, VictoriaMetrics, alerting, packet captures, and dated incident evidence on a separate Fedora host.
- **Self-hosted services:** RouterCloud, a LAN/Tailscale-scoped file service with authentication, WebDAV, and backup/recovery workflows.
- **Change safety:** shell/Python tooling, CI checks, isolated ARMv7/QEMU tests, reviewable deployments, backups, and rollback plans.

**Explore:** [Start here](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/blob/main/docs/START-HERE.md) · [Project status and limits](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/blob/main/PROJECT-STATUS.md) · [Unbound upgrade and incident report](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/blob/main/docs/case-studies/unbound-dnssec-autotrust-opkg-incident-2026-10-24.md)

### [Fedora Workstation Setup](https://github.com/wojko6/fedora-workstation-setup)

Reproducible workstation configuration, security hardening, localization, verification, and recovery engineering.

- **Running workstation (2026-11-11):** Fedora **45 / KDE Plasma 6.8.2 / Wayland**, NVIDIA **620.70.06 Open Kernel Module**, following a controlled Fedora 44 → 45 upgrade.
- **Last accepted reproducible restore baseline (historical):** Fedora **44 / GNOME Shell 50.5 / Wayland**, with clean-room and physical-host verification. Fedora 45/KDE clean-room restoration and full desired-state promotion remain **HOLD**.
- **Bounded post-upgrade checks:** boot and external display worked; a real S3 suspend/resume succeeded with one NVIDIA allocation warning. These observations do not establish long-term GPU/session stability or a validated bare-metal rollback.
- **Security and administration:** SELinux, Secure Boot state auditing, NVIDIA module management, firewalld, systemd, Btrfs, and controlled Tailscale exposure.
- **Restore and maintenance:** clean-room VM recovery tests, integrity checks, documented update/rollback procedures, and separate encrypted backup/isolated restore work.
- **Localization and desktop integration:** version-aware Polish translations, source/resource auditing, runtime UI verification, and a locally fixed native Plasma AppBay grid launched from the Krema dock via a registered D-Bus widget action. The panel applet ID is installation-specific; this setup is not yet a portable restore artifact.

**Explore:** [Workstation README](https://github.com/wojko6/fedora-workstation-setup) · [Current status and limits](https://github.com/wojko6/fedora-workstation-setup/blob/main/PROJECT-STATUS.md) · [AppBay + Krema technical record](https://github.com/wojko6/fedora-workstation-setup/blob/main/docs/kde-appbay-krema-launchpad-2026-11-11.md) · [Recovery documentation](https://github.com/wojko6/fedora-workstation-setup/blob/main/docs/DISASTER-RECOVERY.md)

### [OPNsense + MikroTik Segmentation Lab](https://github.com/wojko6/OPNsense-MikroTik-Segmentation-Lab)

**Completed and validated GNS3 lab** combining an OPNsense perimeter firewall with MikroTik RouterOS CHR. It demonstrates routed network segments, stateful firewall rules, NAT, DHCP, restricted administration, and evidence-backed isolation of a downstream network from the trusted LAN.

## Current engineering labs

These projects are **experimental, not production-deployed services**.

### [Homelab Control Center — published V0.3 and gated follow-up labs](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/tree/main/experiments/fedora/homelab-control-center-v0.1)

A manually launched, loopback-only dashboard with **read-only, fixed-query telemetry** from VictoriaMetrics and DNS Guard. V0.3 source is merged; later V0.14.x collection/history experiments remain in [separate Draft PRs](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/pull/338) and are **not** permanently deployed. Real measurements remain distinct from synthetic demonstrations.

### [Local AI coding-agent security lab](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/blob/main/docs/worklog/2026-10-26.md)

Testing **Ollama + Qwen3.5 4B + OpenCode** on Fedora with narrowly allowlisted reads/edits, host-controlled tools, rootless network-disabled Podman, SELinux, and independent semantic test gates. A bounded control run and one injected-input test each passed **16/16 semantic checks**; other trials exposed reliability failures. This is evidence from specific tests, **not** a claim of general prompt-injection resistance or autonomous production access. The separate [C.63 offline source modules were published](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/pull/347) with `MODEL_ACTION_AUTHORITY=NONE`; later C.64 proposals remain under separate Draft review.

**November 2026 documentation checkpoint:** a controlled physical [Fedora 45 upgrade](https://github.com/wojko6/fedora-workstation-setup/blob/main/docs/WORKLOG-2026-11-10.md) was completed and is documented alongside a [KDE localization audit](https://github.com/wojko6/fedora-workstation-setup/blob/main/docs/kde-localization-audit-2026-11-10.md) and the [AppBay/Krema integration](https://github.com/wojko6/fedora-workstation-setup/blob/main/docs/kde-appbay-krema-launchpad-2026-11-11.md). The accepted Fedora 44/GNOME restore evidence remains historical; **Fedora 45/KDE full reproducibility is not yet certified**.

## Technical toolkit

- **Systems:** Fedora Linux, GNOME, KDE Plasma, Wayland, systemd, SELinux, Secure Boot, Btrfs, Restic
- **Networking:** TCP/IP, routing, DNS/DNSSEC, DHCP, NAT, iptables/nftables, Tailscale, OPNsense, MikroTik
- **Observability and diagnostics:** Wireshark, tshark, tcpdump, syslog-ng, Grafana, Loki, Alloy, VictoriaMetrics, WebRTC telemetry
- **Automation and labs:** Bash, Python, Git, GitHub Actions, Podman, QEMU, GNS3, VirtualBox, VMware

## What I'm interested in

I'm particularly interested in **IT Support / Help Desk, junior system or network administration, infrastructure operations, and entry-level security roles**. My strongest portfolio examples are hands-on troubleshooting, documentation, controlled changes, and diagnosing real systems rather than just configuring them once.

## Contact

- **GitHub:** [github.com/wojko6](https://github.com/wojko6)
- **Email:** wojtekkotaj6@gmail.com

*Technical claims are scoped to the linked project documentation and dated validation results. Lab prototypes and proposed changes are not presented as production features.*
