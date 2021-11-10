# SLAX
A collection of SLAX scripts

### alarms.slax
* This script will populate the jnxUtil MIB, Juniper Utility MIB, with descript
ions of any chassis alarms that are present so it can be queried with a SNMP 
management tool.  Chassis alarms will show up in the mib with an ascii encoded i
ndex that will equate to chassis-alarm[index] where the index is the alarm numbe
r.

### dhcp-bindings-to-static.slax
* This script looks for dynamic DHCP security bindings and creates a static binding with the specified group name (default BYPASS) for a specif
ied VLAN (default Voice).  It will only create a static binding if the state is fully bound (BOUND), and the interface is defined as an access type, trunks are ig
nored.  If any bindings are found that can be converted to static, a configuration is created and commmited.

### persistent-macs-dot1x-static-bypass.slax
* This script adds all of the registered persisent MAC addresses to the dot1x static bypass configuration and commits the configuration.

### pkg.slax
* Attempts to removed old pkg files (Junos) by executing the shell command: "pkg setup rm previous"

### free_up_space.slax
* This script will free up as much space as possible on an EX VC stack. It merciliessly deletes probably unused files and software packages.  

### resv.slax
* Collects LSP and TED information and spits out the results in a parsable output suitable for feeding into graphviz

### spanning-tree.slax
* This script gathers information about the Ethernet Switching environment related to spanning tree for offline analysis

### special-voip.slax
* This script configures access interfaces to accept a tagged vlan with switch-option voip, and optionally a forwarding-class.  The voice vlan
 *   and fowarding class wil be advertised to an attached media device if LLDP-MED is configured on the port.

### disable-unused-trunks.slax
* This script will add a description and/or disable any unuused trunk ports




