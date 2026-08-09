# Enterprise Linux Identity and Access Management

## Overview

This document covers enterprise Linux identity, authentication, authorization and access control management.

## Identity Management Scope

- User Management
- Group Management
- Password Management
- Sudo Access
- SSH Access
- PAM
- File Permissions
- ACL
- Account Locking
- Account Expiration
- Privilege Management
- Authentication
- Authorization
- Access Auditing

## User Management

Common operations:

- Create user
- Modify user
- Delete user
- Lock user
- Unlock user
- Set password
- Configure account expiration
- Configure login shell
- Configure home directory

Useful commands:

- useradd
- usermod
- userdel
- passwd
- chage
- id
- getent

## Group Management

Group operations:

- Create group
- Modify group
- Delete group
- Add user to group
- Remove user from group
- Validate group membership

Useful commands:

- groupadd
- groupmod
- groupdel
- gpasswd
- id
- groups

## Sudo Management

Sudo configuration covers:

- Administrative privileges
- Least privilege
- Command-specific access
- Sudoers configuration
- Sudo groups
- Sudo validation

Important files:

```text
/etc/sudoers
/etc/sudoers.d/
