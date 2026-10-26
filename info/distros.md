# Recommended distros

Recommended distributions for both veterans and beginners, based on hardware and use cases.
Heavy preference for nativeness, atomicity, immutablity, and modern tooling

## Desktops

- Require atomicity or immutability to be on this list

If there is an app you want to run on a 24/7 headless server
and they do not provide a headless/pure CLI variant or doesn't run without a desktop,
contact the developer to make a CLI variant or abandon it entirely.
Your server does not deserve to run a desktop environment just for that.
You will reduce component lifespan needlessly.

### General Workstations

[Bluefin Dakota](https://projectbluefin.io/dakota/)

- Modern tooling like systemd-boot, uutils
- Significantly reduced legacy bloat like dnf and rpm components
- Rolling release GNOME OS, though high stability
- Preset AI, Development, CLI integrations
- Smooth delta updates
- Homebrew ready

### Gaming

[Bazzite](https://bazzite.gg/)

- For casual gamers, Dakota is better
- Best for dedicated serious competitive gaming PCs
- Seamless controllers and hardware support
- Suitable for gaming consoles or HTPCs
- Dedicated Gamescope and Big Picture Mode presence

### Others

VanillaOS
Flatcar Container Linux
blendOS
Nitrux

### Experimental or for tinkerers

AerynOS

- Fast package manager
- Optimized for speed
- Currently has limited packages
- Atomic, but not immutable
- Updates can be done without reboots

NixOS

- 1 to 1 reproducibility down to home path as well
- Immutable nix store, mutable core paths
- Core system immutability can be achieved by impermanence
- Best for ricers
- Steep learning curve
- Not true immutability, this lets users granularly choose, but increasing security risks and uncertainties if not handled properly.
- Frequent chances of breakages, though rollbacks can be done.

## Servers

### [umbrelOS](https://umbrel.com/umbrelos)

- Easy installation of apps and services
- Rugix based OTA updates and atomic
- Mutable for current session, but unintended core system changes are wiped on reboot
- Seamless Tailscale access
- Wifi access backup support
- Machines in dock for virtualization
- umbrel.local easy access

### ZimaOS

- To be decided

### Proxmox

- Legacy apt based, prone to breakage
- VM centric, docker not by default
- Vast configurations
- Has addon enterprise software repos

### RHEL bootc based custom image

- For large enterprise deployments
- Multiple machines with deterministic execution
- Add cockpit or CasaOS UI into the image while building via GitHub actions

### [Bluefin Server](https://projectbluefin.io/server/)

- To be decided

## Installation media creation

### Ventoy

- For multi ISO setups, not requiring flash
- Even a phone can move a file to it and you can use it
- Good for a dedicated recovery USB
- Works by hacky workarounds, which can sometimes conflict with modern images or cause dracut errors
- Unstable at times, may not map layouts correctly as intended by the image creator
- Good for live only session type images, though some persistence options may work
- You can sha256sum individual images

### Direct flash tools or dd

- Work reliably most of the time
- Data verification is tool dependent
- Lets image makers use strict path mapping to the live loop files
- eg. Etcher, Fedora Media Writer, Impression and Rufus
- Rufus supports windows to go, if you want
