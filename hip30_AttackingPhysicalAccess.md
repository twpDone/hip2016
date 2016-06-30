#PAC Physical Access system
You can found it everywhere, and even if system looks physically differents,
they are quite similar

##PACs Components
* Acces control point
  * Door
  * Gates
* Credential reader
* ?

##Acces Cards
* Low freqs
    * older
    * cheap
    * easy to deploy
    * unsecure
* Hi freqs
    * >13 <56 MHz
    * Sometimes encrypted

`schemes about freq length`
//obviously on Lower freqs you can store less data

```
 1   2   3   4
 |___|___|___|...

 1 2 3 4 5 6 7
 |_|_|_|_|_|_|....
```

##PACs Componnents
* Acces control server (offten an old windows server)

##Read Creds
`scheme`

`more schemes (about communication network)`

##Split Personality of security

* Computer security
* Physical security

A lot of similar sub points

##why PACs deployements are insecure
* gap between phy sec and comp sec is closing
* ?
* ?

###Physical sec culture
* from military
* lack technical understanding
* unaccustomed to patching / addressing vulns
* vendor loyal
* Resistant to change

###HID iClass
* card & reader perform mutual authent with 64bit encryption key
* this key is programmed at factory

#Attack Surfaces ans exploits
* Acces cards
* Readers
* Request to exit devices
* Acces control pannel
* Access control server
* ?

> Proxmark3 
> Grid-it
//Ad time ?

##Access card attacks - Long Range
* Expensive
* Misread custom formats
Based on arduino

##Design Prestation
`lots of photos`

##Access card attacks - Low tech
* **Most vendor print it on the card**
* Sometimes on the *box*

##Reader attacks
* BLEKey
  * Replay attacks
  * See blackhat conf

##Request to exit device attacks
* If theres a gap between doors
You can trigger the cell even from the outside
// trad : utiliser un ceintre (pas cher)
* Long Ballons for clowns

##Access Control Panel attacks
* Remember how important door controlers are ?

    * FTP Open
    * Web servers
    * SNMP
Care:
* Devices are fragile (no mass scanning)
* Many web interfaces wor only in IE
* Don't change settings (**you probably can't change it back**) 

Ports to look for:
* TCP
    * 21
    * 23
    * 80
    * 9999
* UDP 
    * 161

`screen of web interface (very talkative)`

> VertX
* skimmer
* fuzzer
* lot of other stuff

##Hunting Access Servers
DNS/Scan Keywords
* CCURE
* ? 
//too fast

##Other PACS Ressources
* sharepoint
* email

#Putting it together
* Long range reader
* Duplicate cards to make fake employee cards
* observed security guard daily activity

* Hardware keylogger
* capture creds
* acces to acces server
* duplicate card with the most acess

> All your base are belong to us

#Long road ahead
* Physical security
* Comp sec

@hacktressog on Twitter


