# Enterprise Linux High Availability and Disaster Recovery

## Overview

This document covers high availability, failover, disaster recovery and business continuity concepts for enterprise Linux environments.

## High Availability

High Availability (HA) is designed to minimize service downtime by providing redundancy and automated or controlled failover.

## HA Components

Typical HA environments may include:

- Multiple Linux Nodes
- Shared or Replicated Storage
- Cluster Communication
- Resource Manager
- Service Resources
- Virtual IP
- Fencing
- Quorum
- Monitoring

## Active-Passive Architecture

```text
                Client
                  |
                  |
             Virtual IP
                  |
          +-------+-------+
          |               |
       Node-01          Node-02
       ACTIVE           STANDBY
          |               |
          +-------+-------+
                  |
            Shared Storage
