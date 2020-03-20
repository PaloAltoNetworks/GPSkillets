# 9.0 Remote Access VPN with Pre-Logon Quick Config

## Overview

GlobalProtect configured per the Remote Access VPN with Pre-Logon [Quick Config](https://docs.paloaltonetworks.com/globalprotect/9-0/globalprotect-admin/globalprotect-quick-configs/remote-access-vpn-with-pre-logon.html),
with the following changes:

- A root CA is generated on the firewall, and is used to generate a self-signed cert for the GlobalProtect portal and a
  shared machine certificate that needs to be distributed to clients.
- Client connection method has been changed from *on-demand* to *always-on*.
- Local user database has been configured with the username and password gpuser1/gpuser1 for quick testing, and is
  used for authenticaiton.
- LDAP config has been configured like the guide, but is only used as an example.

This skillet assumes no config exists on the firewall.

## Usage

1. Run the skillet.
2. Download/activate the desired GlobalProtect client on the gateway.
3. Export the generated machine certificate, and distribute it to clients.  Install the certifcate in the personal
   certificate store on the endpoints per the [documentation](https://docs.paloaltonetworks.com/globalprotect/9-0/globalprotect-admin/authentication/set-up-client-certificate-authentication/deploy-machine-certificates-for-authentication.html#id80c6dea9-335f-4f4b-9309-77b3c11cb5f8_id2e243b63-a20c-48eb-b745-f7b98cce59db) (local computer store on Windows, System Keychain on macOS).