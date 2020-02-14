


#### Lab Topology 

See lab topology diagram


#### Lab Objectives

* Configure multiple-area OSPF on a router
* Verify multiple-area OSPF behavior
* Configure OSPF stub, totally stubby, and no-so-stubby areas
* Configure OSPF authentication


#### Required Resources

* EVE-NG Pro
* Cisco IOL "i86bi-linux-adventerprisek9-ms.155-2.Tbin" image


#### Lab Requirements

1 Configure Addressing and Loopbacks
  * Using the addressing scheme in the diagram, configure the serial interfaces on R1, R2, and R3
    * One end of the serial link needs to be configured as the DCE
    * Clock rate for the DCE needs to 64000
  * As per the topology diagram, configure the loopback interfaces on R1, R2, and R3

2 Add Interfaces to OSPF
  * Configure the OSPF process on routers R1 and R2 (use router number for OSPF process)
  * Configure the subnet of the serial link between R1 and R2 to be in OSPF area 0 using the **network** command
  * Add loopback 1 on R1 and loopback 2 on R2 into OSPF area 0
  * Change the network type on the loopback intrfaces so that they are advertised with the correct subnet
  * Verify that both routers have OSPF neighbors
  * Verify that the routers can see each other's loopback interfaces
  * Add the subnet between R2 and R3 into OSPF area 23 using the **network** command
  * Add loopback 3 on R3 into OSPF area 23
  * Change the network type on R3's loopback 3 intrface so that it is advertised with the correct subnet
  * Verify that the neighbor relationship between R2 and R3 comes up
  * Output of the **show ip route** command on R1 identifies a route to the R3 loopback as an inter-area route
  * Output of the **show ip route** command on R2 displays no inter-area routes becuase R2 is in both areas (it is an ABR)
  * Use a Tcl script to verify connectivity to all interfaces from any router, with the exception of loopback 20 on R3

3 Configure a Stub Area
  * Under the OSPF process on R2 and R3, make area 23 the stub area
  * Confirm that the adjacency comes up between R2 and R3 (it may go down during the transition period)
  * Output of the **show ip route** command on R3 identifies a default inter-area route pointing toward R2
  
4 Configure a Totally Stubby Area
  * 


#### Additional Information

* 
