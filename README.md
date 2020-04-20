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
I compile a custom kernel with out of tree modules that is distributed globally. This kernel and OS need to be bootable on Secure boot enabled systems.

-------------------------------------------------------------------------------
Who is the primary contact for security updates, etc.
-------------------------------------------------------------------------------
- Name: Donald A. Cupp Jr.
- Position: Owner
- Email address: doncuppjr@yahoocom
- PGP key, signed by the other security contacts, and preferably also with signatures that are reasonably well known in the linux community:  
'-----BEGIN PGP PUBLIC KEY BLOCK-----

mQENBF6cr0MBCADbuKFE6FCYz2jfX+zEygIRD+9KTS79ASE0JXSb29LTHQN7tYy6
dPe6/Bz1XiTEjpGt7DD+/2ObFiXESFOt1uzWmq/ts+n0x4IRR2isfipTDq4W7rHy
Osvr8yvRclsIoBWM57uU2eXuZudFpGwrTXEVHn0B4vT9yrGLRjmIyGkAr7uimQrd
ngc4xL3jVKqavQTs7LDWB4FMxzTHrooBJM5Ic4yzOKFxEa4DbRW4GREEVtbuaDo6
WS4Ak1zrTfh5aajsLY/GttruC+qKtytNJvI9TAknwUfukEFSim/OM34mWXVUho4I
CV+8j8FRmGCgKYghM6D8hnW9z/oM08RDolabABEBAAG0KERvbmFsZCBBLiBDdXBw
IEpyLiA8ZG9uY3VwcGpyQHlhaG9vLmNvbT6JAVQEEwEIAD4WIQRyUr5rdHIvvpY0
1Ct0kLaN89oNeAUCXpyvQwIbAwUJA8JnAAULCQgHAgYVCgkICwIEFgIDAQIeAQIX
gAAKCRB0kLaN89oNeNEvCACnk8VvKZXLWD2OHzkatTDK5o2flVXxiC6EV1p0VRvs
U7zmL3kGT7EyIL+jJzDdtINVZw7lAhsWB+S+gh+tONx+dKLPg7H1jF4c7IdHe5gu
5XB1WSYUmSEybAq5OqwMTKAb8SDjMqunVYr9tr5sR4bByMV6iyO0/4sjg8s3ByP/
LJKMeomnn/PXnZ1ccEfrMxOsku4EnQkCvog63pIhY4XnHLz+Tl7AkDiW39fGWdBo
jE0LGUZhewo4St2ug1yCyK1pwtjVlEqY4iaT6VJd33+aoSCSsXxw89Xy/WDKi4IL
sYWtxvLdV3kWyRvjwAXT6wRjjL8ASNmNyXPXhTWoW/lIuQENBF6cr0MBCADrdZ5s
2k3GxUt9MM+Lcm1MEjRdkENTqFnFl1OLpAlO6yw8juYDBaW+6I9qwRwvg99ggWlX
3xyQAhmajlh41iqqnLsJI1zUfwZCfHSkcmnSIoczofEzQlb2rPv/CpjKVs/7hnrW
+jfzDzWhNkH5bcZMH4WweijoE9NSyTU7bPU+vknmB7KsAKIkBTFnZ4j0uKK6GIpt
9GA/D+FUBCHQ5lhlFtVS1IWHoI87OszdVfONpBiiBj2upLLMs/76jafEnk7JdeTl
mFdFYLM0GEGmTAMUDpbaZF0JZlI3XssACawk8k7fQb9K55hXZej6uXMaApuni2sZ
mbUNE/+v1sThIYdrABEBAAGJATwEGAEIACYWIQRyUr5rdHIvvpY01Ct0kLaN89oN
eAUCXpyvQwIbDAUJA8JnAAAKCRB0kLaN89oNeLGnB/90sPTrwHcpPixabJaWrtdn
CNwS3A+4npu4WfNhdOdzMT5+vmb79ogNX3TsoTv1I0ufdkNDX9QTrEH5Ul/NIoz9
skOXQtdO6Oz+fxv+/WtlXRLDs0IXCPjR0W51ZePU1hzMYIuv6lGaiFcV8B1ELg3I
xIm1RvLcP40BZQTmaFG5IWqrYSPCdpftEjoackDpkSAOBZLdaGEBxq2IwoXzfyLY
+RXlDjlUVpNI6vUFSEFzvN/mDnfv43x08VAaLhxd5WO0tF80PU536DK5TZVy3vk8
4D555qI0jaAJHq/uKcgXH9VuQc2oUA32L1BzkMmnbPVTCm6izzoTSpmRl6jbONbv
=OYoc
-----END PGP PUBLIC KEY BLOCK-----'


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
git clone https://github.com/Thinstation/thinstation.git  
cd thinstation  
./setup-chroot  
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
