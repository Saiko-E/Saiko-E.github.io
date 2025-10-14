comandos:

STP

Switch(config)# spanning-tree vlan <ID de la VLAN>
Switch(config)# spanning-tree mode <pvst | rapid-pvst | mst>
Switch# show spanning-tree


EtherChannel

S1(config)# interface range f0/21 – 22
S1(config-if-range)# shutdown
S1(config-if-range)# channel-group 1 mode desirable
S1 (config-if-range) # no shutdow

S3(config)# interface range f0/21 - 22
S3(config-if-range)# shutdown
S3(config-if-range)# channel-group 1 mode desirable
S3 (config-if-range) #no shutdown

S1(config)# interface port-channel 1
S1(config-if)# switchport mode trunk
S3(config)# interface port-channel 1
S3(config-if)# switchport mode trunk

S1# show etherchannel summary
Flags: D - down P - in port-channel
I - stand-alone s - suspended
H - Hot-standby (LACP only)
R - Layer3 S - Layer2
U - in use f - failed to allocate aggregator
u - unsuitable for bundling
w - waiting to be aggregated
d - default port
Number of channel-groups in use: 1
Number of aggregators: 1
Group Port-channel Protocol Ports

dtp:
interface <nombreInterface>
switchport nonegotiate
switchport mode dynamic auto (para habilitar)