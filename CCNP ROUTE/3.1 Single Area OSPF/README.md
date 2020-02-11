

#### Lab Topology

See lab topology diagram


#### Lab Objectives

* Configure single-area OSPF
* Advertise liopback interfaces into OSPF
* Verify OSPF adjacencies
* Verify OSPF routing information exchange
* Modify OSPF link costs
* Change interface priorities
* Utilise debugging commands for troubleshooting OSPF

#### Required Resources

* EVE-NG Pro
* Cisco IOL "i86bi-linux-adventerprisek9-ms.155-2.Tbin" image


#### Lab Requirements

1 Configure Addressing and Loopbacks
  * As per the topology diagram, apply IP address to the FastEthernet interfaces on R1, R2, and R3
  * As per the topology diagram, create a Loopback interface on R1, R2, and R3
  * Configure the serial interfaces on R1 and R2 as per the topology diagram
    * One end of the serial link needs to be configured as the DCE
    * Clock rate for the DCE needs to 64000
    * Bandwidth for both serial interfaces needs to be configured to match actual bandwidth of the links
  * Verify that the appropriate physical interfaces are up and that you can ping across each link

2 Add physical interfaces to OSPF
  * Configure the OSPF process on all routers (use router number for OSPF process)
  * Add the interfaces on R1 and R3 to OSPF using the network command
  * Add the interfaces on R2 to OSPF directly on the interface
  * All interface need to be in OSPF are 0
  * Using debug commands, observe OSPF by shutting down and bringing up physical links

3 Add Loopback Interfaces to OSPF
  * On each router, add the Loopback interfaces into the routing process using the network command
  * Verify these networks have been added to the routing table
  * Change the default network type to ensure that OSPF is advertising the actual network of the Loopbacks and not the host routes
  * Use a Tcl script to verify connectivity to all addresses in the topology

4 Modify OSPF Link Costs
  *


#### Additional Information
