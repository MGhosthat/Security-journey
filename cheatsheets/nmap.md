# Nmap Master Cheat Sheet

## 1. Essential Flags & Discovery
* `-sV` — Service version detection (discovers exact software and version numbers running on ports).
* `-sC` — Runs default Nmap Scripting Engine (NSE) scripts for basic vulnerability and enumeration checks.
* `-p-` — Scans all 65,535 TCP ports (essential for catching non-standard ports like hidden administrative panels).
* `-oN <file>` — Outputs scan results in normal text format for evidence collection.
* `-Pn` — Disables host discovery (treats all targets as online; bypasses blocked ICMP ping rules).

## 2. Scan Types
* **TCP SYN Scan (`-sS`):** Default stealth/half-open scan. Requires root privileges.
* **TCP Connect Scan (`-sT`):** Completes the full 3-way handshake; used when root access isn't available.
* **UDP Scan (`-sU`):** Scans UDP services (DNS, DHCP, SNMP). Slower and more complex.

## 3. Timing Templates (`-T0` to `-T5`)
* `-T3` — Normal speed (default).
* `-T4` — Aggressive speed; recommended for fast, reliable local lab environments.
