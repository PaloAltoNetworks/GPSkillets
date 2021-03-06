# GlobalProtect Quick Configs

Implementations of the 
[GlobalProtect Quick Configs](https://docs.paloaltonetworks.com/globalprotect/9-0/globalprotect-admin/globalprotect-quick-configs.html), made into skillets for easy import into Palo Alto Networks firewalls.

## Deployment Note

These configs create security rules that **do not** contain any sort of security profile or logging configuration.
Please utilize the best practice security profiles from the
[iron-skillet](https://github.com/PaloAltoNetworks/iron-skillet) repository on the rules that get created and read the
[Best Practices documentation](https://docs.paloaltonetworks.com/best-practices) before deploying.

## Configurations

There are some small differences between the quick config and what has been implemented here.  See the `README.md` file
in each directory for any changes.

* `remote_access` - Remote Access VPN (Always On)
* `pre_logon` - Remote Access VPN (Always On) with Pre-Logon Machine Certificate

## Authors

* Michael Richardson ([@mrichardson03](https://github.com/mrichardson03/))
* Scott Shoaf ([@scotchoaf](https://github.com/scotchoaf))

## Support Policy

The code and templates in the repo are released under an as-is, best effort,
support policy. These scripts should be seen as community supported and
Palo Alto Networks will contribute our expertise as and when possible.
We do not provide technical support or help in using or troubleshooting the
components of the project through our normal support options such as
Palo Alto Networks support teams, or ASC (Authorized Support Centers)
partners and backline support options. The underlying product used
(the VM-Series firewall) by the scripts or templates are still supported,
but the support is only for the product functionality and not for help in
deploying or using the template or script itself. Unless explicitly tagged,
all projects or work posted in our GitHub repository
(at https://github.com/PaloAltoNetworks) or sites other than our official
Downloads page on https://support.paloaltonetworks.com are provided under
the best effort policy.
