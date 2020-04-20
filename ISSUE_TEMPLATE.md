Make sure you have provided the following information:

 - [x] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
	https://github.com/ThinStation/shim-review
 - [x] completed README.md file with the necessary information
 - [x] shim.efi to be signed
 - [x] public portion of your certificate embedded in shim (the file passed to VENDOR_CERT_FILE)
 - [x] any extra patches to shim via your own git tree or as files
 - [x] any extra patches to grub via your own git tree or as files
 - [x] build logs


###### What organization or people are asking to have this signed:
`Donald A. Cupp Jr.`

###### What product or service is this for:
`ThinStation OS Framework for Embedded Systems`

###### What is the origin and full version number of your shim?
`https://github.com/rhboot/shim/releases/download/15/shim-15.tar.bz2 15`

###### What's the justification that this really does need to be signed for the whole world to be able to boot it:
`I compile a custom kernel with out of tree modules that is distributed globally. This kernel and OS need to be bootable on Secure boot enabled systems.`

###### How do you manage and protect the keys used in your SHIM?
`AES256 Hardware Key with Pin Entry`

###### Do you use EV certificates as embedded certificates in the SHIM?
`No`

###### What is the origin and full version number of your bootloader (GRUB or other)?
`REFInd: https://git.code.sf.net/p/refind/code [4a84fc], gummiboot: https://github.com/systemd/systemd/archive/v244.tar.gz [244]`

###### If your SHIM launches any other components, please provide further details on what is launched
`SHIM will launch either the REFInd or gummiboot bootloader.`

###### How do the launched components prevent execution of unauthenticated code?
`Both REFInd and gummiboot communicate with the SHIM to authenticate code to be executed.`

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
`No. Only REFInd and gummiboot will be signed. Each of which only execute signed kernels.`

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
`Linux Kernel 5.4.33: No Patches`

###### What changes were made since your SHIM was last signed?
`N/A Never Signed`

###### What is the hash of your final SHIM binary?
`511e5518678ad3a694347257129413ff3f607993f095d521803a4be79d69f6fb  shimx64.efi`
