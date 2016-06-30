#Voting between sharks
by scytl

##TLDR
Online voting is an open door for many attacks and the targets of many attackers.
You can do it *right* enven if there is a thousands ways to do it *wrong*.

###You must have an end to end verification.

* At your computer side
You have control by checking your vote
  * You must be able to check you vote
    * A uniq return code is generated and sended to you before voting
    * You can verify it after prparing your vote
    * You can verify it after casting you vote

* At network side
You have integry check
  * SSL encryption
  * Bulletin encrypted on client side

* At Election Board
Integrity of counting and decryption
  * Shamir secret sharing
    * To avoid decryption by one person
    * To avoid Administration of controlling the vote
  * Homomorfic encryption
    * Electoral Board can't decrypt one bulletin but all in one decrpytion operation
    * Ensure counting and decryption is done right

* Infrastructure
Vote must be anonymous, so you need an authent wich generate an ananymous token
  * Authent Service
    * 2 step authent 
    * Separated off the ballot box service

###TLDR Conclusion
* Similar to classical vote
* Protected by various crypto properties
* Better than postal
* But you cant trust the endpoint, you have to verify (certificates etc)
* Reduce attack surface 
  * short time exposition
  * 2 step authent
  * air gapped networks

##Internet Votting
Thousand ways to do it *wrong*

* Voting machines 
* Online sites 
  * onsite
  * remote

Convenient

##Changes
Physical paper + poll site
-> Sysadmins, ...
Increase risks

##What could be wrong 
* privacy
* integrity
* malware
* privates companies
* voter coercion
* hacking

EG. :Mafia can buy votes, a lot of things can go wrong...

##Privacy on the internet doesn't exists
###End to End Encryption
Need to secure and protect the vote, decryption can only be done by the electoral board
Share the secret between people of the electoral board, to prevent reading before the end of election
(Shamir shared secret) 3 people minimum

###Two agencies model
Anonymous token <- auth service
|->Ballot box service

the services must be independant 

###Mix-Net
Lower trust assumption needed

###Homomorphic tally
Not decrypting individual votes, but all in one with "homomorphic encryption"
=Efficient but restricted representation

##How Can I be sured that my vote have been counted
* Traditionnal vote*
* ballot in the ballot box, you can see it
* you sign

###tracing to decryption
*With e-vote*
Private receipt , *encrypted*
Sign the receipt at decryption

###Verifying decryption process
Control on integrity
Shuffle + Decrypt

prove the decryption has done correctly.
Verifying without secrets ? YES

What happen if i have a malware on my computer ?
Because the bulletin is encrypted, i can't check my own vote
*Return codes

At reception the server return the number of your choice 
Return code uniq for you
After chosing :
* Audit Bulletin
* Cast Bulletin

To avoid sending decryption info
We can decrypt on server then encrypt and send encrypt for voter
//Weakness if server taken over ?

end to end control
check + transmition integrity + decryption

##Private companies wanting to control vote
Administration + Electoral board
Create key in Air gapped Computers

One person cant decrypt, modify, generate fake result, add votes
You cant hide your vote, but so as in traditionnal (cameras, etc)

###Making it hard to large scale attack
2 steps authent
cant vote twice
cant vote with false credentials

###Prevent from hacking
Reduce attack surfaceisolated/offlin server for critical
* Few endpoints
* Short time frame
* Patches

Sysadmin can access every thing
* split responsability
* all previous points
Trust relies on Boards, auditor, ...
Sysadmin can destroy anything
Replace software ! *BUT we have end to end verifyability

#Conclusion
* A lot of advances sec controls
* Better than postal
* But you cant trust the endpoint, you have to verify
Based on many cryptographic properties





