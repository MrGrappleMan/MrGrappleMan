# Other distributions

Distros that might work for you, but are outdated in terms of modern tooling
No strict requirement of being atomic

## Desktops

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

VanillaOS
Flatcar Container Linux
blendOS
Nitrux

## Servers

### Proxmox

- Legacy apt based, prone to breakage
- VM centric, docker not by default
- Vast configurations
- Has addon enterprise software repos

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

### RHEL bootc based custom image

- For large enterprise deployments
- Multiple machines with deterministic execution
- Add cockpit or CasaOS UI into the image while building via GitHub actions
