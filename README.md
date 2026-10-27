# Hi, I'm Wojciech Kołłątaj 👋

**Linux · Networking · IT Infrastructure · Security**

I build and document hands-on infrastructure projects focused on **reliable operations, network troubleshooting, least privilege, automation, and recovery**. My work combines a real ASUS-based home-lab gateway, a Fedora workstation, and isolated network/security experiments.

I value **reproducible procedures and verifiable results**: configuration and code are version-controlled, changes are tested against explicit criteria, and production observations are kept separate from simulated or experimental results.

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

- **Accepted reproducible baseline:** Fedora 44 / GNOME Shell 50.5 / Wayland, with automated desired-state and physical-host checks.
- **Current desktop experimentation:** Fedora 44 / **KDE Plasma 6.7.5** / Wayland on the physical laptop; KDE is in use but has **not** replaced the accepted GNOME restore baseline.
- **Security and administration:** SELinux, Secure Boot, signed NVIDIA modules, firewalld, systemd, Btrfs, and controlled Tailscale exposure.
- **Restore and maintenance:** clean-room VM recovery tests, integrity checks, documented update/rollback procedures, and separate encrypted backup/isolated restore work.
- **Localization engineering:** version-aware Polish translations, source/resource auditing, and runtime UI verification.

**Explore:** [Workstation README](https://github.com/wojko6/fedora-workstation-setup) · [Recovery documentation](https://github.com/wojko6/fedora-workstation-setup/blob/main/docs/DISASTER-RECOVERY.md)

### [OPNsense + MikroTik Segmentation Lab](https://github.com/wojko6/OPNsense-MikroTik-Segmentation-Lab)

**Completed and validated GNS3 lab** combining an OPNsense perimeter firewall with MikroTik RouterOS CHR. It demonstrates routed network segments, stateful firewall rules, NAT, DHCP, restricted administration, and evidence-backed isolation of a downstream network from the trusted LAN.

## Current engineering labs

These projects are **experimental, not production-deployed services**.

### [Homelab Control Center — Fedora V0.3](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/tree/main/experiments/fedora/homelab-control-center-v0.1)

A manually launched, loopback-only dashboard with **read-only, fixed-query telemetry** from VictoriaMetrics and DNS Guard. Real measurements are distinguished from synthetic demonstrations, which require explicit opt-in. Source and tests are merged; persistent startup and remote access are **not** approved.

### [Local AI coding-agent security lab](https://github.com/wojko6/Advanced-ASUS-Edge-Gateway-ZTNA-Infrastructure/blob/main/docs/worklog/2026-10-26.md)

Testing **Ollama + Qwen3.5 4B + OpenCode** on Fedora with narrowly allowlisted reads/edits, host-controlled tools, rootless network-disabled Podman, SELinux, and independent semantic test gates. A bounded control run and one injected-input test each passed **16/16 semantic checks**; other trials exposed reliability failures. This is evidence from specific tests, **not** a claim of general prompt-injection resistance or autonomous production access.

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
