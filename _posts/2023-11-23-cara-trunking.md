---
title: "Cara Trunking VLAN Cisco Packet Tracer"
author_profile: false
excerpt: "Trunking berfungsi melewatkan traffic VLAN dari switch yang berbeda. Antara switch lantai 1 dan lantai 2 terhubung. PC1, PC2, PC5 dan PC6 masuk dalam VLAN 10 sedang PC3, PC4, PC5 dan PC6 masuk dalam VLAN 20. "
breadcrumbs: true
header:
  teaser: "https://github.com/Julius-Ulee/School-Programs/assets/61336116/af924502-89f0-4e48-81a2-72c653453fd3"
last_modified_at: 2023-11-23T:00:00-01:00
categories:
  - Computer
tags:
  - Cisco
  - Network
comments: true
show_date: true
---

Trunking berfungsi melewatkan traffic VLAN dari switch yang berbeda. Antara switch lantai 1 dan lantai 2 terhubung. PC1, PC2, PC5 dan PC6 masuk dalam VLAN 10 sedang PC3, PC4, PC5 dan PC6 masuk dalam VLAN 20. 

![image](https://github.com/Julius-Ulee/School-Programs/assets/61336116/af924502-89f0-4e48-81a2-72c653453fd3){: .align-center}

Konfigurasi VLAN pada seperti dibawah. Membuat vlan 10 dan vlan 20. 

```yml
switch1(config)#vlan 10
switch1(config-vlan)#vlan 20
switch1(config-vlan)#int f0/1
switch1(config-if)#sw access vlan 10
switch1(config-if)#int f0/2
switch1(config-if)#sw access vlan 10
switch1(config-vlan)#int f0/3
switch1(config-if)#sw access vlan 10
switch1(config-vlan)#int f0/4
switch1(config-if)#sw access vlan 10
Switch0(config)#vlan 10
Switch0(config-vlan)#vlan 20
Switch0(config-vlan)#int f0/1
Switch0(config-if)#sw access vlan 10
Switch0(config-if)#int f0/2
Switch0(config-if)#sw access vlan 10
Switch0(config-vlan)#int f0/3
Switch0(config-if)#sw access vlan 10
Switch0(config-vlan)#int f0/4
Switch0(config-if)#sw access vlan 10
```

Konfigurasi interface yang saling terhubung antar switch dengan mode trunk. Lakukan pada kedua switch. 

```yml
Switch0(config)#int f0/10
Switch0(config-if)#switchport mode trunk
Switch1(config)#int f0/10
Switch1(config-if)#switchport mode trunk
```

Ping dari satu PC ke PC lain dan ketikkan perintah show vlan. 

```yml
PC>ping 10.10.10.11
Pinging 10.10.10.11 with 32 bytes of data:
Reply from 10.10.10.11: bytes=32 time=17ms TTL=128
Reply from 10.10.10.11: bytes=32 time=0ms TTL=128
Reply from 10.10.10.11: bytes=32 time=0ms TTL=128
Reply from 10.10.10.11: bytes=32 time=0ms TTL=128
Ping statistics for 10.10.10.11:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 0ms, Maximum = 17ms, Average = 4ms
PC>ping 10.10.10.13
Pinging 10.10.10.13 with 32 bytes of data:
Reply from 10.10.10.13: bytes=32 time=11ms TTL=128
Reply from 10.10.10.13: bytes=32 time=0ms TTL=128
Reply from 10.10.10.13: bytes=32 time=0ms TTL=128
Reply from 10.10.10.13: bytes=32 time=1ms TTL=128
Ping statistics for 10.10.10.13:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 0ms, Maximum = 11ms, Average = 3ms
PC>ping 20.20.20.20
Pinging 20.20.20.20 with 32 bytes of data:
Request timed out.
Request timed out.
Request timed out.
Request timed out.
Ping statistics for 20.20.20.20:
Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
PC>
```

PC dapat melakukan ping ke sesame VLAN beda switch namun tidak bisa ke beda VLAN. 

```yml
Switch1#sh int trunk
Port Mode Encapsulation Status Native vlan
Fa0/10 on 802.1q trunking 1
Port Vlans allowed on trunk
Fa0/10 1-1005
Port Vlans allowed and active in management domain
Fa0/10 1,10,20
Port Vlans in spanning tree forwarding state and not pruned
Fa0/10 1,10,20
```
