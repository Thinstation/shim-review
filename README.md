This repo is for review of requests for signing shim.  To create a request for review:

- clone this repo
- edit the template below
- add the shim.efi to be signed
- add build logs
- commit all of that
- tag it with a tag of the form "myorg-shim-arch-YYYYMMDD"
- push that to github
- file an issue at https://github.com/rhboot/shim-review/issues with a link to your branch

Note that we really only have experience with using grub2 on Linux, so asking
us to endorse anything else for signing is going to require some convincing on
your part.

Here's the template:

-------------------------------------------------------------------------------
What organization or people are asking to have this signed:
-------------------------------------------------------------------------------
Donald A. Cupp Jr.

-------------------------------------------------------------------------------
What product or service is this for:
-------------------------------------------------------------------------------
ThinStation OS Framework for Embedded Systems

-------------------------------------------------------------------------------
What's the justification that this really does need to be signed for the whole world to be able to boot it:
-------------------------------------------------------------------------------
We compile a custom kernel with out-of-tree modules that is distributed globally. This kernel and OS need to be bootable on Secure boot enabled systems.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Donald A. Cupp Jr.
- Position: Owner
- Email address: doncuppjr@yahoo.com
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:  
doncuppjr.pgp

-------------------------------------------------------------------------------
Who is the secondary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: None
- Position: N/A
- Email address: N/A
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:
N/A
-------------------------------------------------------------------------------
What upstream shim tag is this starting from:
-------------------------------------------------------------------------------
15

-------------------------------------------------------------------------------
URL for a repo that contains the exact code which was built to get this binary:
-------------------------------------------------------------------------------
https://github.com/rhboot/shim/releases/download/15/shim-15.tar.bz2  
https://github.com/Thinstation/thinstation/tree/6.2-Stable/ts/ports/components/shim

-------------------------------------------------------------------------------
What patches are being applied and why:
-------------------------------------------------------------------------------
https://patch-diff.githubusercontent.com/raw/rhboot/shim/pull/183.patch: Fix compiling on GCC 9, this patch was approved and merged. Back ported to this official release of SHIM.
sed for a typo: UNKOWN to UNKNOWN

-------------------------------------------------------------------------------
What OS and toolchain must we use to reproduce this build?  Include where to find it, etc.  We're going to try to reproduce your build as close as possible to verify that it's really a build of the source tree you tell us it is, so these need to be fairly thorough. At the very least include the specific versions of gcc, binutils, and gnu-efi which were used, and where to find those binaries.
-------------------------------------------------------------------------------
ThinStation  
git clone --depth 1 https://github.com/Thinstation/thinstation.git  
cd thinstation  
./setup-chroot -i  
./setup-chroot -e prt-get update -fr shim |tee shim-build.log  


gcc, 9.2.0, https://github.com/Thinstation/thinstation/tree/6.2-Stable/ts/ports/core/gcc  
binutils, 2.32, https://github.com/Thinstation/thinstation/tree/6.2-Stable/ts/ports/core/binutils  
gnu-efi, 3.0.11, https://github.com/Thinstation/thinstation/tree/6.2-Stable/ts/ports/opt/gnu-efi  

-------------------------------------------------------------------------------
Which files in this repo are the logs for your build?   This should include logs for creating the buildroots, applying patches, doing the build, creating the archives, etc.
-------------------------------------------------------------------------------
shim-build.log

-------------------------------------------------------------------------------
Add any additional information you think we may need to validate this shim
-------------------------------------------------------------------------------
Can't think of anything.
