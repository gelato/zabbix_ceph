http://it.kuchuk.net/2017/04/zabbix-ceph.html

=============================================
����, ��� ����������� � ���������� �������:

������������:
/etc/zabbix/scripts/
#  (�� CephAdmin �������) 

####Discovery Scprits####
#����������� ������� mon, osd, mds
ceph-daemon-discovery.sh
#����������� �������� �� ������� osd ������
ceph-osdnodes-discovery.sh
#����������� Pool-��
ceph-pools-discovery.sh

####DataGet Scprits####
#���� �������� ����� ������ (�������)
ceph-status.sh
#���� ������ � �������� Discovery ������
ceph-data.sh

������������:
/etc/zabbix/zabbix_agentd.d/

####Template Keys#### 
#  (�� CephAdmin �������)
/etc/zabbix/zabbix_agentd.d/ceph.conf 

������������:
WebUI Zabbix

####������ Ceph Cluster#### 
#��������� ����� WebUI Zabbix � Configuration > Templates : Import
zbx_export_template_ceph_cluster.xml


�� CephAdmin ������� ������������� � �������� ����� �� ��� ���� ��������
[root@cephadmin ~]# ssh-keygen
[root@cephadmin ~]# ssh-copy-id -i ceph@server1.river.ru
[root@cephadmin ~]# ssh-copy-id -i ceph@server2.river.ru
[root@cephadmin ~]# ssh-copy-id -i ceph@server3.river.ru
 
����������� ������ �������� � LatestData ����� ����� 5 �����. 
=============================================================