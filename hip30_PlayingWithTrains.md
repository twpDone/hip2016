#Cyber Trains Attacks ?

We will focus on a case that could have been a Hack.
Train increased it's speed until living the rails.

##Who is he
`You'll find this in his slides`

##Vector of attacks
.?

#ACS - 64
Amtrak Citiess Sprinter
* design by siemens based on eurosprinter and Vectron models
* Electric locomotive, no diesel combo
* Automation system by siemens Stet / Sibas 32

Thousands of ACS-64 are running.

`scheme of the sprinter`
* ATP/PCT 
* Console
* Air-Braking
* Belise
* TCU
* ..

`Driver console scheme`

##Fun and profit with the Train Communication Network
* Traction
* Brakes (not-airbrakes)
* Seat Reservation
* ... (a lot of stuff)

##MVB 
Addreses can be polled for status or response that will feed others on the bus.
1. You pull the lever
2. It probes the status of the lever
3. Saw that value as changed
4. It send the signal
5. increases the speed

Messages are in **plain text**
> What year is it 

###Weaknesses
* No authentication
* Traffic not encrypted
* No built-in screening process. Promiscuous.

* "Single Master" Yes... and **No**. (you can have many, but its built with one)

###Forging request
* ?
* ?
* ?
// wow that was fast
`see the slide`

###Wild Vuln appeared !
"DevicesScan protocol" probes for "unknown devices"

##Hijacking Mastership
CCU(master) ID:1 ID:1337(**BA bit=1**) ID:2
BA = Bus Administrator

Then Transfer the mastership  (for up to 256*1024 ms)

###What can we do
*Anything*
That's a question of knowledge and time

###Infection Vectors - Physical Domain
* Most 'accessible' location is in the *electronics cabinet*
* MVB extended Locations
* .?
* .?

`Notice No. 70 screen`

Not *supposed* to be connected to anything...

###Cliché
* Thx the Wifi (AmtraConnect)
* Amtrak ink

> Our wifi connects you at more than your destination

###Air Gap it
`another scheme about communication network`

?
?
?

###Conclusion
Its old and should be abandonned.


