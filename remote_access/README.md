# 9.0 Remote Access VPN Quick Config

## Overview

GlobalProtect configured per the Remote Access VPN [Quick Config](https://docs.paloaltonetworks.com/globalprotect/9-0/globalprotect-admin/globalprotect-quick-configs/remote-access-vpn-authentication-profile.html#idedc68ee0-d39f-4d91-bcae-5409f57c4071),
with the following changes:

- Default interfaces are swapped: interface ethernet1/1 is l3-untrust, ethernet1/2 is l3-trust.
- A root CA is generated on the firewall, and is used to generate a self-signed cert for the GlobalProtect portal.
- Client connection method has been changed from *on-demand* to *always-on*.
- Local user database has been configured with the username and password gpuser1/gpuser1 for quick testing, and is
  used for authenticaiton.
- LDAP config has been configured like the guide, but is only used as an example.

This skillet assumes no config exists on the firewall.

## Usage

Run the skillet, then download/activate the desired GlobalProtect client on the gateway.