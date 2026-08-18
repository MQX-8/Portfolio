Back to [Main](https://mqx-8.github.io/Portfolio/).

This page is where I post my documented projects, home labs and reports. Not all the projects I work on will end up here, only the more exciting ones. Each entry was something I was curious about and wanted to research, learn more about, and become more skilled/experienced in. I believe learning something because you *want* to is significantly different than because you *have* to. So, I figure challenging myself with these projects not only demonstrates additional hands-on experience and skills, but also allows me to learn on a deeper level. Especially considering all the research, troubleshooting, and documentation.  

# <span style="color: #4af137;">**SOC Detection and Incident-Triage Home Lab**</span> <span style="color: #3d000;">***(In Progress)***</span>
[***FULL DOCUMENTATION HERE.***](https://mqx-8.github.io/Portfolio/Projects_Labs_Reports/SOC_Triage_Lab)

# <span style="color: #9a848d;">**Project Overview**</span>
I designed this lab to include a Kali Linux attack machine, a Windows 10 host, an Ubuntu host running OWASP Juice Shop, and an Ubuntu Server acting as Wazuh Server to simulate realistic SOC scenarios. Sysmon and Sysmon for Linux are installed on the 2 workstations and the Wazuh agents are configured to push those logs to the Wazuh server.  

**UPDATE:** 18 August 2026
<blockquote><p>This lab was originally intended to be proof of concept for T1 SOC Analyst skills, thus I wasn't too worried about a secure network design. However, the Security/Blue Team/Cautious instincts in me are screaming to put in the extra time and work to implement a 5th VM -- a pfSense firewall to to isolate the SIEM infrastructure on a dedicated management subnet. Endpoint-to-SIEM communications will now be restricted by stateful firewall policy to required Wazuh services.</p><blockquote>  

# <span style="color: #4af137;">**Local Network Traffic Analysis: Investigating Suspicious Outbound Connections with WireShark -- Home Lab**</span>
[***FULL DOCUMENTATION HERE.***](https://mqx-8.github.io/Portfolio/Projects_Labs_Reports/Local_NTA_Wireshark)

# <span style="color: #9a848d;">**Project Overview**</span>

A brief packet capture of the 192.168.1.0/24 home network identified four previously unmapped TCP sessions between workstation 192.168.1.224 and local endpoint 192.168.1.217 on destination port 8009. Traffic anomalies were triaged to determine the origin, protocol context, initiating processes, and legitimacy of the sessions.

Triage objectives:
- Identify and classify the previously unmapped endpoint.
- Validate the protocols and services observed in the packet capture, including SSDP, UPnP, DIAL, and Google Cast.
- Correlate the four network sessions with the local processes that initiated them.
- Determine whether the activity represented malicious behavior, a misconfiguration, or legitimate baseline telemetry.
