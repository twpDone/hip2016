
#Type=5,Code=1 
#Lady in the middle

#MITM Approach
Attacking Routing Table 

> RFC 972

```python
>>> ICMP(type=5,code=1).show2()
###[ ICMP ]###
  type= redirect
  code= host-redirect
  chksum= 0xfafe
  gw= 0.0.0.0
```

#ICMP Redirect
Old redirection to avoid congestion

#(Ab)use Case: Compromise Single Gateway Environement (old way)
    * traffic **to** is redirected
    * traffic **back** keep the old behavior
Not working anymore, was working 
* Windows <= XP
* MacOs <=10.10
* Linux <=3.4

##Mitigation
* Linux >3.6 check if packet comes for (default) GW for the destination
* Started using FIB instead of routing table

`Handling ICMP redirect in TCP Module`

//FIB lookup

##Abuse now
* Mandatory to be in same network

1. trigger a communication from user to server
    * claim to be the server
2. Client anwser
3. spoof server handshake
4. Client send to GW
5. ICMP Redirect

##Exploit

[x] Windows all trigers
[ ] Mac
[x] Lin 2.6>3.5 Any
[x] Lin 3.6>4.6 UDP
?

##How to
* Be prepared to route a lot of traffic
* ipforwarding

#Demo
* Go Lang
* need root/SYSTEM

`redirect -A *ipAttacker* -p -G *gateway* -T *serverIP* -v *victimIP*

* Echo Req
...
* Redirect

* Handle Cleanup

#Summary
* One-way MITM
* Need to be in Same subnet

* You can/**must** disable it !

#CISCO
* Anti spoofing / Port security
* DHCP snooping

RFC
* 729
* 1122
* 1812
* 5827
* 972

dorota[dot]kulas[at]gmail[dot]com





