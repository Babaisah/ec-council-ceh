Ethical hacking fundamentals

- CYBER KILLCHAIN METHODOLOGY
	cyberkill chain are the steps to take out a cyberattack from the reconnaissance phase to the exfiltration phase  
	STEPS 
		RECONNAISSANCE - gathering information
		WEAPONIZATION - creating the weapon such as backdoors, malware and ransomware
		DELIVERY - sending/ delivering the weapon to the victim 
		EXPLOITATION - exploiting vulnerabilities
		INSTALLATION -  installing malwares , maintaining access
		COMMAND AND CONTROL - Creating a communication path between the victim and target
		ACTIONS ON OBJECTIVES - taking out the objective


- TTPs
	tactics, techniques and procedures : this describes the behaviours of the threat actors and their structural framework of executing a cyberattack
		TACTICS: this describes the way an attacker performs a cyberattack
		TECHNIQUES : these are technical procedure used by an attacker 
		PROCEDURES : these are the procedures of how the actors execute a cyberattack  (organizational approach that the actors follow)

 
- ADVERSARY BEHAVIORS
	these are tactics and actions used by threat actors to gain access to a system 
	these are behaviors that indicate compromise, these are activities done by threat actors when they've compromised ons system. this is done to escalate privilege or gain access to other systems on the network
		BEHAVIORS
			DNS TUNNEL 
			CONNECTION TO COMMAND AND CONTROL SERVER
			USE OF POWERSHELL 
			INTERNAL RECONNAISSANCE
			USE OF CLI
			UNSPECIFIED PROXY CONNECTIONS

- IOC
	INDICATOR OF COMPROMISE : THESE ARE EVENTS(clues, artifacts or forensic data) THAT INDICATE COMPROMISE.
		TYPES:
			-EMAIL INDICATORS : SENDER'S EMAIL, EMAIL ATTACHMENTS, EMAIL SUBJECT (this is more useful when its a phishing attack)
			-NETWORK INDICATORS : URLS, DOMAIN NAMES , IP ADDRESS (in detecting cc servers)
			-HOST BASED INDICATORS : FILE HASHES, FILENAMES, BACKDOORS, DLL(DYNAMIC LINK LIBRARY, HEX)
			-BEHAVIORAL INDICATION : POWERSHELL ACTIVITIES, REMOTE COMAND EXECUTION.
					ALL THESE INFORMATION CAN BE FED TO A FIREWALL OR SECURITY DETECTION SYSTEM 

- HACKING:
	Hacking This refers to using a system in a way its not built to use. (outside the creators purpose)
	Hacking in IT refer to exploiting vulnerabilities to gain unauthorised access to a system 
		TYPES OF THREAT ACTORS
			BLACK HAT HACKERS : OFFENSIVE (DESTRUCTIVE ACTIVITIES )
			WHITE HAT HACKERS : DEFENSIVE (PROTECTIVE)
			GRAY HAT HACKER  : DEFENSIVE AND OFFENSIVE
			SCRIPT KIDDIES :(LOW SKILLS)HACKERS THAT USE PRE-BUILT TOOLS FOR HACKING 
			CYBER-TERRORISTS : MOTIVATED BY POLITICAL OR RELIGOUS BELIEF 
			HACKTIVIST : PROMOTE POLITICAL AGENDA 
			ORGANISED HACKERS : E.G ANONYMOUS , LAZARUS 
			STATE-SPONSORED
			INDUSTRIAL SPIES
			INSIDER THREATS 
			SUICIDE HACKERS : BLACKHAT HACKERS THAT DON'T CARE ABOUT BEING CAUGHT 


- HACKING PHASE
	-RECONNAISSANCE : THIS IS A PHASE WHERE INFORMATION ABOUT THE TARGET IS BEING     GATHERED 
		TYPES 
			PASSIVE : THIS DOESNT INVOLVE GETTING IN CONTACT WITH THE TARGET . PASSIVE RECON INCLUDE INFORMATIONS AVAILABLE TO THE PUBLIC, THESE INFORMATION MIGHT BE RELEASED BY THE TARGET INTENTIONALLY OR BY MISTAKE
			ACTIVE : THIS INVOLVES GETTING IN CONTACT WITH THE TARGET. E.G USING NMAP TO SCAN OPEN PORTS ON THE SITE OR NETWORK
	-SCANNING 
		THIS IS A PRE-ATTACK PHASE WHERE THE THREAT ACTOR SCANS THE TARGET NETWORK. THIS CAN BE DONE BY USING TOOLS LIKE NETWORK MAPPER, VULNERABILITY SCANNERS, ETC . THIS IS DONE TO EXTRACT INFORMATION SUCH AS LIVE HOSTS AND OS VERSION.
	-GAINING ACCESS
		 EXPLOITING VULNERABILITIES FOUND IN THE PREVIOUS PHASES TO GAIN UNAUTHORISED ACCESS 
	-MAINTAINING ACCESS
		THIS IS DONE BY USING TOOLS LIKE BACKDOORS, TROJANS AND ROOTKITS
		PWN 
	-CLEARING THE LOGS (covering tracks)
		THIS IS DONE BY HACKERS TO STAY CLANDESTINE AND UNDETECTED IN THE SYSTEM

- ETHICAL HACKI9NG
	-this is the use of hacking tools and techniques to identify security flaws and vulnerabilities in a system.
	--
	QUESTIONS TO BE ASKED/answered when securing a network or system
		What can an intruder see on the network 
		what can an intruder do with the information
		can anyone notice the intruders attemps
		are all of the components adequately protected, updated and patched
		how much time, money and effort is required to obtain adequate protection 
		are the information security measures in compliance with legal and industry standards
	SCOPE AND LIMITATION OF ETHICAL HACKING

- ETHICAL HACKING TOOLS
	GOOGLE DORKING:
		THIS IS A hacking method also known as google hacking or google-fu , this involve finding confidential informations that were inadvertently exposed to the internet.
		--
		the concept of google dorking revolves around using specific search operators to refine queries and obtain more targeted result
		https://www.exploit-db.com/google-hacking-database 
		--
		QUERIES 
		--site:  --used to specify a site
			iot site:microsoft.com
			this will return all microsoft sites with the word iot in it 
			admin password site:microsoft.com
			filetype -- this specifies the filetype such as filetype:pdf,jpg ...etc
		-- filetype:pdf confidential (this will return pdf files that are confidential)
				 	filetype:inc
		--intitle -- this query searches for a specified keyword in their title such as
			  intitle:loginpage.... etc
		--inurl -- this query searches for given keyword in the domains url .. e.g inurl:admin
			 -- inurl:admin login (this will return urls with admin logins)
			 --inurl:phpinfo.php (this will hopefully return server informayions)
		--site -- this query specifies a website or site e.g site:google.com ..
			 site:facebook.com "bala" (this query will check for the user bala in facebook)
		--link -- this query will return pages linked to a specified website .. e.g link:google.com
			 --link:facebook.com
		--related -- this query will return pages that are related to a specified site 
			 --related:redacted.com
		--intext -- this will return pages with a specified keyword in 
		 --"error in query" "mysql_fetch_assoc()" intext:"Warning: mysql_fetch_assoc()"
		--cache -- this will return pages cached versions of a website, this might be informations that have been taken down 
			 --cache:google.com
		--inurl:/wp-content/ intext:WordPress
		--
		--
		{--site:zoom.us inurl:us02web.zoom.us 
			this google dork query will return publicly availble zoom meetings}
	RECONNAISSANCE TOOLS
		 WEB EXTRACTOR (web scraping )
			IT EXTRACTS TARGETED DAT LIKE (EMAILS, PHONE NO, TITLE, DESCRIPTION, KEYWORDS) FROM TARGETED SITE
		tracert/traceroute 
			specifies the route to a domain or server, it uses the icmp protocol
			e.g tracert(windows) google.com 
				traceroute(linux)
			tcp traceroute
				tcptraceroute www.google.com
			imcp 
				tracert www.google.com
			udp 
				traceroute www.google.com
	SCANNING TOOLS 
			- NMAP :  NETWORK MAPPER USED TO EXTRACT INFORMation from live servers such as open ports and their infos etc. zenmap is the gui version of nmap
			- MEGAPING : MegaPing security scanner checks your network for potential vulnerabilities that might use to attack your network
			- -unicorn scan
		     - PRTG NETWORK MONITOR - a cloud based program used to monitor networks and servers
		     - HPING2/3
		     - NETSCAN TOOL PRO
		     - SOLARWIND PORT SCANNER
		     - OMNIPEEK NETWORK PROTOCOL ANALYZER
	ENUMERATION TOOLS
		(windows tool)
		-nbtsat : this is a windows tool that is used to enumerate hosts on a system. Displays NetBIOS over TCP/IP (NetBT) protocol statistics, NetBIOS name tables for both the local computer and remote computers, and the NetBIOS name cache
		-netbios enumerator : this is a tool that enumerates bios details such as netbios name, username, domain name, mac address.
		-global network inventory. www.magnetosoft.com 
		-HYENA 
![[Pasted image 20231019215908.png]]



--
NOTE
-----
hacking mainframe 
AD 
sql
snmp simple network management protocol