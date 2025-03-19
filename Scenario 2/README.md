# Kill Chain Attack Description: Data Anonymisation ETL Pipeline Scenario 1: Malicious Data Injection
 
 ## Stages of the Attack
 
 ### Reconnaissance
 The attacker researches the target website to identify vulnerabilities or entry points.
 
 ### Weaponization
 The attacker creates malicious scripts or fake data to inject into the website.
 
 ### Delivery
 The attacker exploits a vulnerability (e.g., cross-site scripting, XSS) to inject malicious content into the website.
 
 ### Exploitation
 The web scraper collects the malicious content along with legitimate data.
 
 ### Installation
 The data processor stores the malicious content in a DataFrame or other data structure.
 
 ### Command and Control (C2)
 If the malicious content includes scripts, they may attempt to exploit downstream systems (e.g., databases, analytics platforms).

 ### Actions on Objectives
 The attacker exfiltrates sensitive data using the malicious content.