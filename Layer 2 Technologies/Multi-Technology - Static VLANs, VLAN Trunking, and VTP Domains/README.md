
#### Lab Topology

See lab topology diagram

#### Lab Objectives

* Setup a VTP Domain
* Create and maintain VLANs
* Configure ISL and 802.1Q Trunking


#### Lab Requirements

1 Basic Switch Parameters
  * Each switch should be assigned a hostname as per the topology diagram
  * Each switch should be configured an IP address on the management VLAN as per the topology diagram
  * Each switch should be configured with an enable secret 
  * VTY lines on all switches should be configured to allow remote access from other network devices using password of 'cisco'

2 VTP Configuration
  * The distribution layer switches should be configured as the VTP servers
  * The access layer switches should be VTP clients
  * All switches should be in the VTP domain "SWLAB"
  * All switches shol dbe running VTP version 2
  * To restrict flooded traffic on the trunk links, VLAN traffic should be limited between switches in the VTP domain for any VLANs that are not defined 

3 VLAN configuration
  * As per the topology diagram, VLANs 100, 110, and 120 are required
  * The VLANs should be named as:
     * VLAN 100 = Server-Farm-1
     * VLAN 110 = Server-Farm-2
     * VLAN 120 = Net-Eng
  * The switch connected to the hosts as per the topology diagram shoul dbe configured as static access ports

4 Trunking Configuration
  * ISL and 802.1Q trunking should be configured on switches as per the topology diagram
  * All trunk links should be configured statically 
  * To prevent possible security issues, DTP should be disable on all trunk links on all switches
  * Although, by default, all VLANs are allowed on all trunks, all VLANs should be explicitly defined to help reduce the possibility of VLAN attacks
  * VLAN 1 should be the native VLAN on all trunk links


#### Commands Required for Lab

##### Configuration Commands

* enable
* configure terminal
* hostname *name*
* interface *vlan-id*
* ip address *ip-address*
* [no] shutdown
* enable secret *password*
* line *vty number*
* password *password*
* login
* vtp domain *domain-name*
* vtp version {1 | 2 | 3}
* vtp mode {server | client}
* switchport mode {trunk | access}
* switchport access *vlan-id*
* switchport trunk encapsulation {dot1q | isl}
* interface range *interfaces* 
* switchport nonnegotiate
* switchport trunk allowed vlan *vlan-id*
* switchport trunk native vlan *vlan-id*
* vtp pruning
* vlan *vlan-id*
* name *name*
* state {active | suspend

##### Verification Commands

* show vlan
* show vlan brief
* show vtp status
* show interfaces switchport
* show interfaces trunk
* show running-config 

#### Additional Information



