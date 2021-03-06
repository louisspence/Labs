
#### Lab Topology

See lab topology diagram


#### Lab Objectives

* Setup a VTP Domain
* Create and maintain VLANs
* Configure ISL and 802.1Q Trunking

#### Required Resources

* EVE-NG Pro
* Cisco IOL "i86bi-linux-l2-adventerprisek9-15.bin" image


#### Lab Requirements

1 Basic Switch Parameters
  * Each switch should be assigned a hostname as per the topology diagram
  * Each switch should be configured an IP address on the management VLAN as per the topology diagram
  * Each switch should be configured with an enable secret
  * VTY lines on all switches should be configured to allow remote access from other network devices using password of 'cisco'
  * Add a meaningful descriptive name for all switch interfaces in use as per the topology diagram
  * All other interfaces should be administratively disabled with a meaningful description

2 VTP Configuration
  * The distribution layer switches should be configured as the VTP servers
  * The access layer switches should be VTP clients
  * All switches should be in the VTP domain "SWLAB"
  * All switches should be running VTP version 2
  * To restrict flooded traffic on the trunk links, VLAN traffic should be limited between switches in the VTP domain for any VLANs that are not defined

3 Trunking Configuration
  * ISL and 802.1Q trunking should be configured on switches as per the topology diagram
  * All trunk links should be configured statically
  * To prevent possible security issues, DTP should be disable on all trunk links on all switches
  * Although, by default, all VLANs are allowed on all trunks, all VLANs should be explicitly defined to help reduce the possibility of VLAN attacks
    * VLAN 1 should be the native VLAN on all trunk links

4 VLAN configuration
  * As per the topology diagram, VLANs 100, 110, and 120 are required
  * The VLANs should be named as:
     * VLAN 100 = Server-Farm-1
     * VLAN 110 = Server-Farm-2
     * VLAN 120 = Net-Eng
  * The switch connected to the hosts as per the topology diagram should be configured as static access ports


#### Additional Information
