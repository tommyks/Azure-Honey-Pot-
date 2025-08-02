# Building a SOC and honey net in Azure with live traffic
The first steps for this home lab are to create a resource group, virtual network, and a virtual machine.

<img width="1270" height="285" alt="image" src="https://github.com/user-attachments/assets/47e0fc30-6f39-4e90-a94f-64b6e4b97779" />

The next thing to do is to edit the inbound security rules of the firewall to allow any traffic from any traffic to passthrough to try and capture as much traffic as possible.

<img width="566" height="554" alt="image" src="https://github.com/user-attachments/assets/a0038d5d-3d0e-4b7f-8cbe-b980aa009fc4" />

Now I'll connect to the virtual machine that was created to also allow any traffic through the firewall.
<img width="810" height="298" alt="image" src="https://github.com/user-attachments/assets/6f60b326-a2f3-4b76-afe5-aede8cc7d318" />

Now I'll ping the virtual machine from my own device to ensure that the VM is reachable over the internet.
<img width="682" height="473" alt="image" src="https://github.com/user-attachments/assets/8105824f-91a0-4004-a6f5-d8119353491a" />

Next I'll need to connect a log analysis workspace to a SIEM (Microsoft Sentinel) and install/configure Windows Security Events.
<img width="2524" height="1008" alt="image" src="https://github.com/user-attachments/assets/c4284035-884e-48fb-9a57-ab996cd76af5" />

The monitoring tool is now instsalled.
<img width="1905" height="432" alt="image" src="https://github.com/user-attachments/assets/e3350df9-0f3c-4493-8eb7-7d877efe6c66" />

Next I'll head over to the log analytics workspace to verify the logs are being sent over. I'll run a KQL query to view the logged events.
<img width="2214" height="1215" alt="image" src="https://github.com/user-attachments/assets/89d432b3-8538-43a3-adcc-c04c669595b7" />
Only about 10 minutes have passed and over 1000 events have been forwarded over.

Filtered the data a bit.
<img width="1518" height="680" alt="image" src="https://github.com/user-attachments/assets/6518bcda-6c6d-48e9-b963-0f5e76c9e71d" />

Looks like the first attacker in the table appears to be from Ukraine.
<img width="1303" height="1077" alt="image" src="https://github.com/user-attachments/assets/d93506e2-eaf2-41f2-9646-95ea418c60f7" />
