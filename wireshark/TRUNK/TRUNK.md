####
注：当使用Trunk使用IEEE 802.1Q封装时，将对除了Native VLAN之外的所
有VLAN打上标记，如果802.1Q收到一个没有VLAN标记的数据帧，将在Native VLAN内转发。

注:这里要关闭BPDU的干扰。命令：spanning-tree bpdufilter enable

如图。
SW4
vlan 10
SW4的e0/2
interface Ethernet0/2
 switchport access vlan 10
 switchport nonegotiate
 switchport mode access
 spanning-tree bpdufilter enable
end

SW5
vlan 20

interface Ethernet0/2
 switchport trunk encapsulation dot1q
 switchport trunk native vlan 20
 switchport mode trunk
 spanning-tree bpdufilter enable
end
