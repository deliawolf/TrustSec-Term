# TrustSec-Term

Cisco TrustSec simplifies the provisioning and management of secure access to network services and applications. Compared to access control mechanisms that are based on network topology, Cisco TrustSec defines policies using logical policy groupings, so secure access is consistently maintained even as resources are moved in mobile and virtualized networks. Decoupling access entitlements from IP addresses and VLANs simplifies security policy maintenance tasks, lowers operational costs, and allows common access policies to be consistently applied to the wired, wireless, and VPN access.

Cisco TrustSec encompasses security group tags (SGTs) and IEEE MAC Security (MACsec) standard.

1. The frames that enter the Cisco TrustSec domain are marked using an SGT. This is a unique 16-bit tag that represents the unique role of the traffic source in the network. The tag can be thought of as a privilege identifier of the source user, device, or entity. The tagging decisions can either be dynamic, that is, obtained from the Cisco ISE for each client that attempts to access the network, or static.

2. MACsec is an IEEE 802.1AE standards-based Layer 2 hop-by-hop encryption that provides data confidentiality and integrity for media access independent protocols.

he features that are associated with SGTs on the network devices can be broken into three categories: classification, transport, and enforcement.

1. Classification: Classification is the assignment of an SGT to an IP address. This can be accomplished either dynamically or statically. Generally, dynamic classification is done at the access layer and static classification is done in the data center. Dynamic classification utilizes the rich context data available to Cisco ISE for making policy decisions. Dynamic classification can be done using IEEE 802.1X, MAC authentication bypass, or web authentication. Static classification is generally configured on the switch to which servers are attached. Static options and configuration syntax vary by switching platforms and operating system version. Options for static classification include the mapping of IP address, VLAN, or port, to an SGT. Also, Cisco ISE can centrally store a database of IP addresses and their corresponding SGTs. Compatible devices may download the centrally managed mappings from Cisco ISE.

2. Transport: Security group mappings follow the traffic through the network. This can be accomplished either through inline tagging or the SGT Exchange Protocol (SXP). With inline tagging, the SGT is embedded in the Ethernet frame header. Not all network devices support inline tagging. SXP is used to transport SGT mappings across devices that do not support inline tagging.

3. Enforcement: Enforcement is implementing permit or deny policy decisions based on the source and destination SGTs. This can be accomplished with security group access control lists (SGACLs) on switching platforms and security group firewalls (SGFWs) on routing and firewall platforms.

