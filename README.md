# Niagara-bogsnap
The bogsnap module in Niagara captures a real-time snapshot of a Niagara station’s program state and saves it as a file. Users can open these .bog files in Workbench to review the operational behavior of programs and parameters during real-time control activities.  

A snapshot includes not only the program logic but also real‑time point values, point statuses (such as OK, alarm, fault, down, stale, etc.), and platform‑service information. A typical application involves the station automatically saving the relevant program logic and real‑time point data the moment an alarm is triggered, and then emailing the resulting .bog file to the Niagara maintenance engineer.  
<img width="2138" height="597" alt="image" src="https://github.com/user-attachments/assets/86d9a0d6-3fcf-4d9f-8313-581c5d0058ad" />
The bog files will be exported to configured folder in the station:
<img width="886" height="297" alt="image" src="https://github.com/user-attachments/assets/33657a92-d050-42d5-a4c7-ac25f485b903" />
All bog files can be opened by workbench with values, status, etc. 
<img width="1562" height="471" alt="image" src="https://github.com/user-attachments/assets/2fd1ae49-00ad-439d-8eac-090e5cbf55d3" />

Compared to an on‑site visit to the JACE to inspect the program, analyzing a .bog file that contains real‑time point data enables the engineer to remotely assess the status and performance of the field‑running program.

This module can currently convert only the contents of the points folder and certain types of network drivers. In our tests on Niagara 4.14, the MQTT network, BACnet network, Modbus network, SNMP network, and OBIX network were all successfully converted into snapshot (.bog) files containing data and status information. The bogsnap also supports converting multiple Niagara station program folders at once via a single module, generating multiple .bog files simultaneously to improve efficiency.

However, conversion testing did not succeed in the following areas:  
• The Niagara network (password‑protected configurations that prohibit snapshot export)  

• The alarm console, where real‑time alarm information is lost during conversion  

• Historical data and .px files, which cannot be converted to .bog format  

We will continue testing the conversion of other components. If you have specific development requirements, please let us know via email: jason.zhang@gline‑net.com

This module is free to use, share, and deploy in appropriate scenarios, with all decisions and responsibilities resting solely on the user.
