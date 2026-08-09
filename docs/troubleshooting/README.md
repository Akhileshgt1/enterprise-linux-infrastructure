# Enterprise Linux Troubleshooting Guide

## Overview

This document covers real-world enterprise Linux troubleshooting methodology from basic system issues to complex production incidents.

## Troubleshooting Methodology

The standard troubleshooting approach:

1. Identify the problem
2. Collect system information
3. Check recent changes
4. Check logs
5. Check system resources
6. Isolate the affected component
7. Apply corrective action
8. Validate the fix
9. Monitor the system
10. Document the incident

## System Information

Important commands:

- hostnamectl
- uname -a
- uptime
- timedatectl
- who
- w
- last
- dmesg
- journalctl

## CPU Troubleshooting

Common scenarios:

- High CPU utilization
- Single process consuming CPU
- High thread CPU utilization
- CPU load imbalance
- High load average

Useful commands:

- top
- top -H
- ps
- pidstat
- mpstat
- uptime

## Memory Troubleshooting

Common scenarios:

- High memory utilization
- Swap utilization
- Memory leak
- OOM condition
- Out of memory killer

Useful commands:

- free -h
- vmstat
- top
- ps
- /proc/meminfo
- dmesg

## Disk Troubleshooting

Common scenarios:

- Filesystem 100% full
- Inode exhaustion
- Disk I/O high
- Large files
- Deleted files still consuming space

Useful commands:

- df -h
- df -i
- du -sh
- lsblk
- iostat
- lsof

## Filesystem Troubleshooting

Common scenarios:

- Filesystem read-only
- Mount failure
- /etc/fstab issue
- Filesystem corruption
- Mount point unavailable

Validation:

- findmnt
- mount
- df -h
- lsblk
- cat /etc/fstab
- journalctl

## Network Troubleshooting

Common scenarios:

- Server unreachable
- DNS failure
- Port unavailable
- Routing issue
- Packet loss
- Interface down

Useful commands:

- ip addr
- ip route
- ping
- ss
- curl
- dig
- traceroute
- tcpdump
- nmcli

## Service Troubleshooting

Common scenarios:

- Service stopped
- Service failed to start
- Service repeatedly restarting
- Port not listening
- Configuration error

Useful commands:

- systemctl status
- systemctl restart
- systemctl is-active
- journalctl -u
- ss -lntp

## Boot Troubleshooting

Common scenarios:

- GRUB failure
- Kernel panic
- initramfs issue
- Emergency mode
- Rescue mode
- /etc/fstab failure
- Boot filesystem issue

Troubleshooting flow:

BIOS/UEFI
→ GRUB
→ Kernel
→ initramfs
→ systemd
→ Services

## Security Troubleshooting

Common scenarios:

- SSH login failure
- Permission denied
- SELinux denial
- Firewall blocking connection
- User authentication failure

Useful commands:

- ssh
- id
- getent
- chmod
- chown
- ausearch
- ausearch -m AVC
- firewall-cmd
- journalctl

## Log Analysis

Important logs:

- journalctl
- /var/log/messages
- /var/log/secure
- /var/log/audit/audit.log
- /var/log/dmesg

## Production Incident Workflow

### P1 / Critical

1. Confirm impact
2. Identify affected servers/services
3. Check recent changes
4. Collect logs
5. Stabilize service
6. Restore availability
7. Identify root cause
8. Document RCA

### P2 / High

1. Identify affected component
2. Analyze logs
3. Check resource utilization
4. Apply corrective action
5. Validate service
6. Monitor

## Root Cause Analysis

Every major incident should document:

- Incident summary
- Impact
- Timeline
- Detection
- Root cause
- Contributing factors
- Resolution
- Validation
- Preventive action

## Validation Checklist

After troubleshooting:

- Service status
- Process status
- CPU
- Memory
- Disk
- Network
- Logs
- Application connectivity
- User connectivity
- Monitoring status

## Status

🚧 Documentation in progress
