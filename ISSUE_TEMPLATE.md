Make sure you have provided the following information:

 - [x] link to your code branch cloned from rhboot/shim-review in the form user/repo@tag
	https://github.com/ThinStation/shim-review@ThinStation-shim-x64-20200509
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
`I compile a custom kernel, with out-of-tree modules, that is distributed globally to millions of Secure boot enabled systems.`

###### How do you manage and protect the keys used in your SHIM?
`AES256 Hardware Key`

###### Do you use EV certificates as embedded certificates in the SHIM?
`No`

###### What is the origin and full version number of your bootloader (GRUB or other)?
`Grub2: 2.04 
 https://github.com/Thinstation/thinstation/tree/6.2-Stable/ts/ports/opt/grub2 
 http://ftp.gnu.org/gnu/grub/grub-2.04.tar.xz 
 Fedora patches 0001 - 0210`

###### If your SHIM launches any other components, please provide further details on what is launched
`Does not load other components.`

###### How do the launched components prevent execution of unauthenticated code?
`GRUB enforces Secure Boot, using the accepted patches (see github.com/rhboot/grub2); fallback.efi and MokManager are shim components that enforce authenticated code already.`

###### Does your SHIM load any loaders that support loading unsigned kernels (e.g. GRUB)?
`No`

###### What kernel are you using? Which patches does it includes to enforce Secure Boot?
`Linux Kernel 5.4.33: No Patches`

###### What changes were made since your SHIM was last signed?
`N/A Never Signed`

###### What is the hash of your final SHIM binary?
`d001cbf8128378ac2311bfefca9eaf813b72ab2b7711e99785791d998ffd2d86 shimx64.efi`
