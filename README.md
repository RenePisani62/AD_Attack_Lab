# AD_Attack_Lab
A lab comprising Windows Server 2022, Windows 10 w/s and a Kali Linux w/s. Where attack scenarios are executed.

LLMNR Poisoning Overview
Demonstrates where an invalid hostname generates a network broadcast attempting to resolve an unknown/invalid hostname. Kali w/s is monitoring network traffic by using Responder. Domain controller (DNS) broadcasts username and password hash of operator attempting to locate unknown/invalid host. Kali w/s intercepts credentials and presnets password hash to next application.
