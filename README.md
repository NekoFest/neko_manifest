# NekoFest #

## Setting up your machine ##

 You must be running a 64-bit Linux distribution and must have installed some packages to build
 Paranoid Android. Google recommends using [Ubuntu](http://www.ubuntu.com/download/desktop) for
 this and provides instructions for setting up the system (with Ubuntu-specific commands) on
 [the Android Open Source Project website](https://source.android.com/source/initializing.html#setting-up-a-linux-build-environment).

 Once you have set up your machine according to the instructions by Google, return here and carry
 on with the rest of the instructions.

## Getting Started ##
 1. Initialize the source code

 ```bash
  repo init -u https://github.com/NekoFest/neko_manifest -b tm
 ```

 2. Download the source code

 ```bash
  repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
 ```

## Building ##
 1. Set up build environment
 ```bash
  . build/envsetup.sh
 ```

 2. Initialize a target
 ```bash
  lunch neko_device-buildvariant
 ```

 3. Build the source code
 ```bash
  mka neko
 ```
