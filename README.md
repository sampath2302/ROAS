# ROAS
# Config ROAS with and without Subinterfaces on a Router

5 VLANS in this topology 192.168.10.0/24, 20.0/24......50.0/4

.1 is default g/w on router for each vlan (ex: 192.168.20.1/24 for vlan 20)

.10 as PC's IP in each VLAN.(Ex: VLAN20 - 192.168.20.10/24)

Configure PCs, Switch and the Router.

Conditions are:

PC1 should be in VLAN10

On Router, should not configure subinterface for VLAN10. Configure vlan10 g/w on main interface.

All PCs should ping each other







# Solution:

Config PC, Switch and Router as you normally would, everything pings except to and from VLAN 10. As there is no subinterface, VLAN 10 is not created on the router. Solution is to change the native VLAN to 10 in this context. On trunk interface use this command "switchport trunk native vlan 10" to modify native vlan.



 
