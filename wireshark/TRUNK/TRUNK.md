####
ע����ʹ��Trunkʹ��IEEE 802.1Q��װʱ�����Գ���Native VLAN֮�����
��VLAN���ϱ�ǣ����802.1Q�յ�һ��û��VLAN��ǵ�����֡������Native VLAN��ת����

ע:����Ҫ�ر�BPDU�ĸ��š����spanning-tree bpdufilter enable

��ͼ��
SW4
vlan 10
SW4��e0/2
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
