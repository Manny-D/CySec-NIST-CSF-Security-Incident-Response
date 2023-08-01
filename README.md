<h1>Security Incident Response via NIST CSF</h1>

<h2>Scenario</h2>
A fictional multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses recently experienced a DDoS attack, which compromised the internal network for two hours until it was resolved.

During the attack, the organization’s network services suddenly stopped responding due to an incoming flood of ICMP packets. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services. 

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through an unconfigured firewall. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack. 
</br></br>


<h1>Incedent Report Analysis</h1>
<h2>Summmary</h2>
A security event occurred when network resources were inaccessible.  The cybersecurity team determined the cause was  due to an incoming flood of incoming ICMP packets or DDoS attack. The team blocked the attack and stopped all non-critical network services so that critical ones could be restored.  

<img src="https://www.bsigroup.com/globalassets/localfiles/en-us/images/misc/nist.jpg"/>

<h2>Identify</h2>
A malicious  actor(s) targeted the organization with an ICMP flood attack which affected the entire internal network. 

<h2>Protect</h2>
To mitigate this from happening in the future, the following changes need to be made to the firewall: 
Rule to limit rate of incoming ICMP packets, and
Source IP verification to check for spoofed IP addresses on incoming ICMP packets. 

Also consider adding IDS/IPS systems to monitor/filter suspicious activity.  


<h2>Detect</h2>
See above (Protect section)

<h2>Respond</h2>
For future security events:

- Refer to playbook on incident response and notify management. 
- Isolate affected systems.
- Restore critical systems affected. 
- Review SIEM tool(s) / IDS / IPS dashboard for info.
  - alerts should be configured/sent when suspicious activity is detected from the suggestions made above. 


<h2>Recover</h2>
To recover from DDoS / ICMP flooding, network resources need to return to a normal state: 

- Attacks can be blocked at the firewall.
- All non-critical network services need to be stopped to reduce internal traffic.
- Critical services should be restored.
- Once flooding has timed out, non-critical services can be restored. 
