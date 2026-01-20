# SSH Hardening and Secure Access Lab

## Goal
Secure remote access by hardening SSH and validating controls.

## Environment
- Ubuntu 22.04 VM (VirtualBox)
- Host: macOS
- Network modes: NAT and Bridged

## Tools
- OpenSSH
- VirtualBox
- Linux CLI

## Baseline
- Port 22
- Root login allowed
- Password authentication enabled

## Hardening Steps
- Changed SSH port to 2222
- Disabled root login
- Disabled password authentication
- Enabled key-based authentication
- Limited trusted devices

## Issues Encountered
- Lost access due to NAT routing
- Permission denied due to missing public key

## Fixes
- Switched VM to Bridged Adapter
- Added Mac public key to authorized_keys
- Fixed permissions on ~/.ssh

## Validation
- Successful login on port 2222
- Root login blocked
- Password login blocked
- External access verified

## Lessons Learned
- Hardening can break access if not planned
- Networking matters as much as security config
- Key management is critical for secure access
