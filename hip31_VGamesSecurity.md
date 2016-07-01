#Security for Video Games
by ANSSI

#PS1
* Wobble Architecture
* Attacks
    * Action Replay 
    * Modchips

* No security
* DRM Bypassed

#XBox1
Contains a secret boot ROM

* Arch similar to PC
* Some security feature
    * Secure boot
    * Bootloader code burned in MCPX (SouthBridge)
    * Storing in custom memory zone
    * **All bypassed**

* Attacks
    * Full Control of the plateform
    * Break secure boot

The secure code, moves from southbridge to CPU. So you can play with the Bus.
XBox EavesDropping Was done by a student .

**Many Vulns**

#XBox360


* 64 bytes Power-PC Proc
* Cryptographic coprocessor
* Hypervisor 

* Some integrity checks
[ ] Data
[ ] Kernel Code
[x] Hypervisor

* Anti-Downgrade feature
    * hardware e-fuse inside the CPU (uniq custom security key)
    * Efuse is Blown at upgrade so the code change
        * Blocks replay attacks

##King Kong Attack 
GPU SHader use Data in Ram (*which is not protected by integrity checks*)
**Patch before became public**
Attackers tried to downgrade, so they had to deal with the e-fuse protection.

##Time Attack
They performed a **time attack** to guess/read the key
Possible by syncronizing at Boot with the POST (debug) Port

##Glitch Attack
CPU is too fast so they slowed down the proc
The integrity check of the 4BL by the 2BL can be glitched with a pulse inserted.

#PS3

* secureboot
* PPE/Hypervisor 
    * Not protected
* DMA Mitigation
* No w^x protection

> Hello hypervisor , i'm geohot
* Glitch attack but not exploitable for games
* ?
* **Major** Vuln in 2010
    * retrieve **private keys**

#PS4
* CPU: X86-64 arch
    * Same as XboxOne
* FreeBSD Kernel
* Sec features
    * Secure boot
    * Free BSD Kernel
        * w^x
        * Userland ASLR 

##SPI flash cloning
* Clone IDs

##Software exploit chain 

###Webkit vuln
First software vuln
Adress leak the attack

###Jailed
ROP is limited *native code execution required*
As bypass w^x protection, you can set pointers to ROP

##BADIRET kernel Vuln
GS Confusion to be in kernelland and point to *userland* 
Possible because IDT can be Writable, no SMAP protection

#Conclusion
Attackers mix both hardware and software vulns.




