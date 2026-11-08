# Recommended distros

Recommended distributions for everyone based on hardware and use cases
Heavy preference for nativeness and modern tooling
Require atomicity or immutability to be on this list

## Desktops

If there is an app you want to run on a 24/7 headless server
and they do not provide a headless/pure CLI variant or doesn't run without a desktop,
contact the developer to make a CLI variant or abandon it entirely.
Your server does not deserve to run a desktop environment just for that.
You will reduce component lifespan needlessly.
A server is a server and a desktop is a desktop.

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

## Servers

### [Bluefin Server](https://projectbluefin.io/server/)

- To be decided

### BuildStream based bootc image

- Ability to remove package management bloat
- Lower upstream complexity

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
