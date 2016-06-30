#Voting between sharks
by scytl

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





