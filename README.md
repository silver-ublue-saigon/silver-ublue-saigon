# silver-ublue-saigon

[![build-ublue](https://github.com/silver-ublue-saigon/silver-ublue-saigon/actions/workflows/build.yml/badge.svg)](https://github.com/silver-ublue-saigon/silver-ublue-saigon/actions/workflows/build.yml)

This is a constantly updating template repository for creating [a native container image](https://fedoraproject.org/wiki/Changes/OstreeNativeContainerStable) designed to be customized however you want. GitHub will build your image for you, and then host it for you on [ghcr.io](https://github.com/features/packages). You then just tell your computer to boot off of that image. GitHub keeps 90 days worth image backups for you, thanks Microsoft!

For more info, check out the [uBlue homepage](https://universal-blue.org/) and the [main uBlue repo](https://github.com/ublue-os/main/)

## Kudos
All of this would not be possible without the continuing energy, drive and enthusiasm of Jorge Castro and the community at Universal blue!
My thanks goes out to anyone who made my tinkering possible, you're all amazing people. It is a fantastic community and project, and venturing in here gave me so much fun (and some @#!%#! also of course). And now, here we are, making my own immutable spins! Obviously I am a bit of a geek, but I am absolutely not a professional developer or sys-admin, which goes to show this is within (almost) everyone's reach.

For more info, check out https://universal-blue.org/

## Why and what?
Immutable OS's and distros are are applied increasingly more. Think about Fedora and its Silverblue and Kinoite, OpenSUSE and MicroOS, VanillaOS, EndlessOS, Nix and soon even Ubuntu, to name but a few. The reasoning behind it can be found in many places on the Internet; you might agree or not, but i am not going to repeat them all over here. But you can still find me editing the fstab file or adding a custom kernel in rolling releases like Arch, Tumbleweed or Siduction. 
I prefer my environment to be very minimal, with basically always the same applications on top of it.

Silver-Ublue-Saigon is my personal take on Silverblue (immutable Fedora Gnome), rebased by the Ublue team and where I have added some cli tools (i.e neofetch, htop, mc etc) and where I have pruned the original base image.

## Tools added or removed:

**Added:**                **Removed:**
- duf                     -firefox
- exa
- htop
- mc
- micro
- neofetch
  
## Installation

> **Warning**
> This is an experimental feature and should not be used in production, try it in a VM for a while!

To rebase an existing Silverblue/Kinoite installation to the latest build:

- First rebase to the image unsigned, to get the proper signing keys and policies installed:
  ```
  sudo rpm-ostree rebase ostree-unverified-registry:ghcr.io/silver-ublue-saigon/silver-ublue-saigon:latest
  ```
- Reboot to complete the rebase:
  ```
  systemctl reboot
  ```
- Then rebase to the signed image, like so:
  ```
  sudo rpm-ostree rebase ostree-image-signed:docker://ghcr.io/silver-ublue-saigon/silver-ublue-saigon:latest
  ```
- Reboot again to complete the installation
  ```
  systemctl reboot
  ```
## Closing statement
I won't include the usual yada yada about me not being responsible for either the content of this image nor for your deployment of it. If you've come this far you know what you are doing.

## Have fun!
