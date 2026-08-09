# Enterprise Storage Guide

## Overview

This document covers enterprise Linux storage administration and storage connectivity.

## Storage Technologies

- SAN Storage
- iSCSI
- LVM
- Filesystem
- Mount Points
- Persistent Mount Configuration
- Storage Validation

## SAN

Storage Area Network (SAN) provides centralized block storage to enterprise servers.

## iSCSI

iSCSI provides block-level storage access over an IP network.

### iSCSI Components

- iSCSI Initiator
- iSCSI Target
- IQN
- Discovery
- Login
- Session Validation

## LVM

Logical Volume Manager provides flexible disk and filesystem management.

### LVM Components

- Physical Volume (PV)
- Volume Group (VG)
- Logical Volume (LV)
- Filesystem

## Storage Validation

The following areas will be validated:

- Disk visibility
- iSCSI session
- Multipath status
- PV/VG/LV status
- Filesystem
- Mount points
- Persistent `/etc/fstab` configuration
- Read/write validation

## Architecture

Detailed SAN → iSCSI → LVM architecture will be documented with diagrams.

## Status

🚧 Detailed storage implementation will be completed on Day 3.
