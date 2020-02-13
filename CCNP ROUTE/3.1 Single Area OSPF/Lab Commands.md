#### Configuration Commands

* **enable**
* **interface** *interface-id*
* **description** *text*
* **ip address** *ip-address*
* **[no] shutdown**
* **clockrate** *value*
* **bandwidth** *value*
* **router ospf** *process-id*
* **network** *address wildcard_mask* **area** *area*
* **ip ospf** *process-id* **area** *area-id*
* **ip ospf network point-to-point**
* **ip ospf cost** *cost*
* **auto-cost reference-bandwidth** *value*
* **ip ospf priority** *number*


#### EXEC Commands

* **show ip protocols**
* **show ip ospf**
* **show ip ospf neighbor [detail]**
* **show ip ospf interface** *interface-id*
* **show ip ospf interface brief**
* **show ip ospf database**
* **show ip route**
* **clear ip ospf process**
* **ping** *ip-address*
* **traceroute** *ip-address*


#### Debug Commands

* **debug ip ospf adj**
* **undebug all**


#### TCL Scripts


tclsh
 foreach address {
 10.1.1.1
 10.1.2.1
 10.1.3.1
 10.1.100.1
 10.1.100.2
 10.1.200.1
 10.1.200.2
 10.1.200.3
 } {
 ping $address }
