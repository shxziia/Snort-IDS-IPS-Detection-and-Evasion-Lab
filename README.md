# Snort-IDS-IPS-Detection-and-Evasion-Lab

## Objective
[Brief Objective]

## Skills Learned
[Bullet Points]


## Tools used
[Bullet Points]

## Steps

Phase 1 - Start monitoring (IDS Mode)

Launch Snort in IDS mode.

The Snort sensor was launched in Intrusion Detection System (IDS) mode using Snort. This mode allowed Snort to passively monitor network traffic in real-time while generating alerts when traffic matches the defined detection rules. We'll use "sudo snort -A console -q -c /etc/snort/snort.conf -i enp0s8" to start Snort in live IDS mode.

Running Snort:

<img width="632" height="35" alt="image" src="https://github.com/user-attachments/assets/c00da0ac-32cf-433a-8079-62d76fe98f60" />

Start Packet Capture with Wireshark.

In order to validate network traffic independently from Snort alerts, Wireshark is used to capture and inspect live packets travelling through the lab network.
This ensured full packet visibility and allowed traffic generated during attack simulations and intrusion detections to be analysed at protocol level.
To ensure network traffic was observable, I generated ICMP echo requests from kali to the Metasploitable 2 target host to verify end to end connecctivity within the lab network.

<img width="1655" height="142" alt="image" src="https://github.com/user-attachments/assets/86aef9b2-e232-4661-ad1a-b561fe5f25b7" />

After starting the capture in Wireshark, I filtered the traffic to ICMP to focus only on the ping activity. From the capture, Wireshark showed successful comunication by capturing both ICMP Echo request and Echo Reply packets confirming end to end connectivity was working as expected. 
