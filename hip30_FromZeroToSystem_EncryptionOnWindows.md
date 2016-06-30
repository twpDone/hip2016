#From Zero to SYSTEM on Full Disk Encrypted

#Them 
@tgills
@NabeelAmhedBE

#Inspiration
Bypass Local Authent to defeat Full Disk Encryption

MS15-122
* trust relationship before local cache is updated

#BitLocker
* TPM
* Pre-boot PIN
* USB key

##Focus on TPM
 * Bitlocker key is in TPM

##Trust Relationship
* computer password used for trust
* randomly generated 30 days
* 2 computer account passwd are stored
* stored in  HKML\....

#Bypassing the patch
Legitimate DC vs Rogue DC

#Ticket Missing
#SPN
MSDN definition
Service/Host or
Service/Host:Port

#Demo 
on 2 vms
You need to know The username and domain name (often stored)

"I don't trust the DC, i can't login"
CN Client Properties - Modify SPN
Make passwd expire

Prompt for new password
> Local cache is not poisoned
> login Works

**GG**

#Kerberos Pass Change
DC says Password Expired
Server send a TGT which is used by client for pass change
6. C -> KPass
7. KPass <- S
8. TGT <- S
9. C -> Req(TGT)

Pass Changed on DC
Cache not poisoned but trust is established.

#BlueBox
* Automated exploit of MS-15-122
??
?

#What's next
* extract data
* requires admin privileges to

#Trust relation
* Trust is not (always) validated

#Group policies
Road to group policies to priv esc
* User conf
    * during login
    * User / SYSTEM
* computer login
    * before login
    * SYSTEM
    * Machine account passwd (*bad*)

 DNS ->
<-RPC 
<- Init LDAP op
<- get GPO info
<- read GPO File

#Example
CMD as user
* DL Netcat
* run NC as SYSTEM
* connect to service as user

#why it works
* Client auth ok on Serv
* Traffic remains intact
* assume that user creds are enough


#IS IT NEW ?
* Luke Jennings Works
* Mitm ms15-011 ms15-014

# Win10 ?
[x] gpoUpdate 
[ ] Windows failed 

Glad  this is fixed.

##Compare W7 vs W10
On W10 is using an SID on LDAP request

###User SID : 
new User SID is created when a New domain is created

###Possibilities
* set the SID
    * windows sysprop (new random SID)
    * Commertial tools
* Offlin NTDS.DIT file
* Samba NT4 PDG

###Mimikatz
2.1 new SID module

#Demo
*logged in*
gpupdate
-> Error msg
**need the SID**  // different on local and on Rogue DC
Run mimikatz on DC
patch NTDS service
Patch SID
** gpupdate on client
[x] OK


