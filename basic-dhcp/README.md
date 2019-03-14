# Basic GlobalProtect Configuration

This skillet configures the GlobalProtect portal and gateway using a
local database for user authentication.


### Highlights of this templates

* GP mobile user connection using a local user database

* Tunnel termination into a GP security zone

* Gateway and Portal configuration


### Prerequisites

* A self-signed certificate local to the firewall
    * Generate a local Certificate Authority (CA) root
    * Generate a certificate signed by the local CA root

* Public facing interface with IP address (eg. ethernet1/1)

* Private facing interface with IP address (eg. ethernet1/2)

* Trust (ethernet1/2) and Untrust (ethernet1/2) zones for tunnel security policy

* Virtual router configuration used for tunnel association



### Next steps after skillet configuration

* Install and configuration mobile devices using the portal IP address

* Add additional users to the local DB as required
