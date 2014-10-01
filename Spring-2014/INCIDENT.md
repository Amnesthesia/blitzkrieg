# INCIDENTRESPONSE

### TL;DR: Principles of Incident Response & Disaster Recovery

* 23-29
* 47-49
* 55-60
* 93-94
* 109-123
* 131-134
* 145-166
* 169-172
* 200-201
* 210-214
* 228-237
* 316-322
* 406-415

**TOTAL:** 106 pages + [slides](Slides/SecurityPlanning), summaries & http://www.tripwire.com/state-of-security/security-data-protection/strengthening-the-intrusion-kill-chain/

**GLOSSARY: Page 521**

## Concepts
* Indicators of Attack **Page 131-134, 169-172**
	* Possible
	* Probable
	* Definite
* Attacks
	* Denial of Service
	* DNS amplification attack
	* Inappropriate usage
	* Malicious code / Malware
	* NTP amplification attack
	* Ping of Death attack
	* Smurf attack
	* Unauthorized Access
	* Waterholing attack
* Phases of Incident Response **Page 316-322**
	* Response
	* Recovery
	* Restoration
	* Resumption
* Incident response strategies
	* Protect & Forget
	* Apprehend & Prosecute
* Intrusion Kill Chain Model **http://www.tripwire.com/state-of-security/security-data-protection/strengthening-the-intrusion-kill-chain/**
	* Reconnaissance
	* Delivery
	* Installation
	* Command & Control (C2)
* Teams **Page 47-49**
	* Incident Response Team
	* Business Continuity Team
	* Crisis Management Team **Page 406-415**
	* Business Restoration Team
	* Coordinating CSIRT
		* COORDCERT
* Contingency planning **Page 23-29**
	- Business Impact Analysis **Page 55-60**
	- Risk management
	- Seven steps of contingency planning process (NIST) **Page 51**
		* Develop the contingency planning policy statement
		* Conduct Business Impact Analysis
		* Identify preventive controls
		* Develop recovery strategies
		* Develop an IT contingency plan
		* Plan, testing, training, and exercises
		* Plain maintenance
	- Five phases of Disaster Recovery plan
	- Rehearsal & testing strategies for Disaster Recovery and Incident Response
	- Backup strategies **Page 228-237**
		- Differential 
		- Electronic vaulting
		- Incremental
		- Mirroring
		- Remote journaling
* Incident handling
	* Incident response life cycle **Page 93**
	* Incident handling life cycle **Page 94**
* Contingency planning components
	* Business Impact Assessment (BIA) **Page 55**
	* Incident Response Planning (IRP) **Page 109**
	* Disaster Recovery Planning (DRP) **Page 111-123**
	* Business Continuity Planning (BCP)
		* Cold/Warm/Hot sites **Page 243-246**
	* ..? MOAR
* MIRSA model
* Forensics 
	* Collecting Evidentiary Material **Page 200-201**
	* Analyzing the evidentiary material **Page 210-214**
* Tools
	* Zenmap
	* Nmap
	* Snort
	* Wireshark
	* Types of Intrusion Detection/Prevention Systems **Page 145-166**
		* Terminology **Page 145**
		* Intrusion Detection System (IDS) **Page 149**
		* Network-based Intrusion Detection System (NIDS) **Page 150**
			* Anomaly based **Page 163**
			* Signature based **Page 165**
		* Intrusion Prevention System (IPS) **Page 163**
		* Intrusion Detection & Prevention System (IDPS) **Page 163**
		* Host-based Intrusion Detection System (HIDS) **Page 158**
		* Application-based Intrusion Detection System (AppIDS) **Page 161**
		* Honey* **Page 165-166**
			* Honeypots
			* Honeynets
			* Honeytokens
			* Trap & Trace system

## Summary

The US military defines the process of a kill chain as F2T2EA, where F2 is Find, Fix, T2 is Track, Target and EA is Engage, Assess. In short, Find, Fix, Track, Target, Engage, Assess is shortened into F2T2EA. Find targets suitable for the op; fix their location; track + observe; target with a suitable weapon to result in the desired effect, then engage it and assess the effects. 

It's referred to as a chain, because if any of these step fails, the process is interrupted, and all links must hold for the chain to be completed. Furthermore, a specific kill chain model for intrusions is outlined as 

* Reconnaissance
* Weaponization
* Delivery
* Exploitation
* Installation
* Command & Control (C2)
* Actions

Where the Reconnaissance phase consists of what Find and Fix was in the US military kill chain, followed by preparing a payload (Weaponization) and then delivering it through e.g email, websites or USBs (Delivery). After delivery comes exploitation -- triggering the code -- and this phase *could* be triggered automatically. Once this has been established, the host would be expected to call home -- this is the Command and Control (C2) phase. The malicious code makes the host establish a channel for communication with it, and with APT malware, subsequent commands are typically not automated.

The final phase is performing the actions, and is called Actions on Objectives (or imo, just Actions -- Objectives is implied). 

| Phase 			 | Detect | Deny | Disrupt | Degrade | Deceive | Destroy |
|--------------|--------|------|---------|---------|---------|---------|
|Reconnaissance| Web analytics|Firewall ACL| | | | |
|Weaponization | NIDS | | | | | |
|Delivery			 | Vigilant user | Proxy filter | In-line AV | Queuing | | | |
|Exploitation  | HIDS | Patch | DEP | | | |
|Installation  | HIDS | Chroot jail | AV | | | |
|Command&Control|NIDS | Firewall ACL | NIPS | Tarpit | DNS Redirect | |
|Actions       | Audit log | | | | | |


The Installation phase (or imo, Persistance) allows access to persist by installing the trojan or backdoor into the system; and to 

