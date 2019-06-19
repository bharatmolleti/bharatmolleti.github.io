---
layout: post
title: Torrent-Box using Raspberry PI 2
date: '2018-12-01 14:57:35'
---

The raspberry pi is a tiny, low cost, low power, single board computer ( SBC ).

In this post, I describe the steps used to create a low power always ON torrent box using the Raspberry PI 2.

This torrent box will be always connected to the internet via a virtual private network (VPN) and will also have an external USB hard disk attached to it.

<figure class="kg-card kg-image-card"><img src="/content/images/2018/12/main_board_hdd-1.jpg" class="kg-image"><figcaption>Raspberry PI 2B with HDD attached</figcaption></figure>
### Hardware Needed

1. Raspberry PI 2B.

2. ┬á5V 3A power supply with micro USB out.

3. 2.5 inch external Hard disc drive with full USB out cable.

4. Ethernet cable.

5. An 8 GB SD card.

### Software Stack

1. Raspbian Stretch Lite ( [https://www.raspberrypi.org/downloads/raspbian/](https://www.raspberrypi.org/downloads/raspbian/) )

2. Open VPN.

3. Deluged.

4. Samba File Share.

### Infrastructure

1. Private Internet Access VPN subscription.

2. Ethernet Port.

## Deluge Web UI
<figure class="kg-card kg-image-card"><img src="/content/images/2018/12/Deluge-WebUI.jpg" class="kg-image"><figcaption>Deluge Local Intranet Portal</figcaption></figure>

The magnet files can be added at the locally configured address : 192.168.0.100:8112, and the always ON torrent box would download the torrent for us.

## Samba Share
<figure class="kg-card kg-image-card"><img src="/content/images/2018/12/Samba-NFS.jpg" class="kg-image"><figcaption>SAMBA for file shares</figcaption></figure>

The downloaded files would be accessible via a the very convenient local network share option. Using deluge also gives us the option of adding the files via the watch folder in the network share.

## OpenVPN Configuration
<figure class="kg-card kg-image-card"><img src="/content/images/2018/12/IpInfo_VPN.jpg" class="kg-image"></figure>

Additional security is never a bad idea. Upon boot, the torrent box has been configured to connect to a VPN. All of the torrents are downloading using the VPN, ensuring the safety of the always connected torrent box.

( In progress ... )

