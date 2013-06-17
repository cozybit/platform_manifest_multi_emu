platform_manifest_multi_emu
===========================

This repo contains the manifest modifications to build a multi-emulator with traffic capturing qemu version.

* HOW-TO build an SDK build with multi-emulator qemu version

1) Initialize a build environment (http://source.android.com/source/initializing.html)
2) Download and configure the repo tool (1st step at http://source.android.com/source/downloading.html)
3) Create a folder for AOSP source
   $ mkdir my_aosp
   $ cd my_aosp
   
4) Inside the folder execute the repo tool pointing to this repository
   $ repo init -u https://github.com/cozybit/platform_manifest_multi_emu.git
   
5) Synchronize repo
   $ repo sync -j4
   
6) Build customized Android SDK (http://tools.android.com/build)
   $ . build/envsetup.sh
   $ lunch sdk-eng
   $ make sdk
   
7) If build finishes correctly you should have an SDK custom build on out/host/linux-x86/sdk/
