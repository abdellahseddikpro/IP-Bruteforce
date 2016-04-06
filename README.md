# IP-Bruteforce
This a free software that is use to brute-force a target(the target must be on your local network )if he is using an IP-based
ACL That allow a single host with a pre  defined  IP address to connect to the target, principle is is the host machine (attacker) 
keep changing the IP address of his machine then send an http request to the target

HOW TO USE :

IP-Bruteforce.py  "interface"  "url"                                                                                                                                                                                        
Exemple :                                                                                                                                                                                                                                                                                                                               
IP-Bruteforce.py eth0 192.168.1.1/index.html                                                                                                    
IP-Bruteforce.py wlan0 192.168.3.254/www/index.php
