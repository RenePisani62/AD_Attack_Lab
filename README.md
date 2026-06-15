# AD_Attack_Lab
A lab comprising Windows Server 2022, Windows 10 w/s and a Kali Linux w/s. Where attack scenarios are executed.

LLMNR Poisoning Overview
Demonstrates where an invalid hostname generates a network broadcast attempting to resolve an unknown/invalid hostname. Kali w/s is monitoring network traffic by using Responder. Domain controller (DNS) broadcasts username and password hash of operator attempting to locate unknown/invalid host. Kali w/s intercepts credentials and presnets password hash to next application.
Successfully captured a NetNTLMv2 authentication exchange using Responder after forcing a hostname resolution failure. Hashcat was able to process the capture, confirming the validity of the hash. A dictionary attack using RockYou completed with status "Exhausted," indicating the password was not present in the supplied candidate set. The exercise demonstrated credential exposure rather than password recovery.
Added Windows 11 pro to the network and attempted the same set of tests as on Windows 10.
In this lab, Windows 10 fell back to LLMNR/mDNS for unresolved hostnames and Responder captured authentication. Windows 11, under similar adapter/DNS settings, did not emit observable LLMNR, mDNS, or NBT-NS traffic for the same invalid hostname test.
