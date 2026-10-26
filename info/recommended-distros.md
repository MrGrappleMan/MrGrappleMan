# Recommended distros

Recommended distributions for both veterans and beginners, based on hardware and use cases.
Heavy preference for nativeness, atomicity, immutablity, and modern tooling

## Desktops

- Require atomic and immutability

### General Workstations

Bluefin Dakota

- Modern tooling like systemd-boot, uutils
- Significantly reduced legacy bloat like dnf and rpm components
- Rolling release GNOME OS, though high stability
- Preset AI, Development, CLI integrations

### Gaming

Bazzite

- Not recommended for casual gamers, Dakota is better
- Only for dedicated serious competitive gaming machines
- Seamless controllers and hardware support
- Suitable for gaming consoles or HTPCs
- Dedicated Gamescope and Big Picture Mode presence

## Servers

### umbrelOS

- Easy installation of apps and services
- Rugix based OTA updates and atomic discarding of unintended core system changes
- Seamless Tailscale access
- Wifi access backup support
- Machines in dock for virtualization
- umbrel.local easy access, static DHCP has reduced requirements though still highly recommend

### ZimaOS

- idk

### Proxmox

- Legacy apt based, prone to breakage
- VM centric
- Vast configurations
- Has addon enterprise software repos

### RHEL bootc based custom image

- For large enterprise deployments
- Multiple machines with deterministic execution
- Add cockpit or CasaOS UI into the image while building