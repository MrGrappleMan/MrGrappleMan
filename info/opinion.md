# Opinions

## Planned obsolescence

Is good when

- The company actively accepts old devices and ethically utilizes them.
- The old devices are re-used for helping the manufacture of newer products.
- The old devices parts are used for repairs
- It is mainly targetted to front facing devices like laptops/phones
- To make ppl migrate to more secure and efficient new tech

Is bad when

- Sole intention is monetization or keeping the customers coming back
- Product is intentionally degraded when initial version had no problems \
and new version has no additional true benefits.
- Capping performance by OTA intentionally to make ppl buy new device

Is subjective when

- Ecosystem lock in

Exchange offers are carefully crafted for this, with virtually no disadvantage \
to the user. Apart from having no backup device, it is worth it for most users.
This best suits consumer facing devices like phones, laptops, consoles, etc.
For worker devices, it depends.

## Devices

These sections are not particularly distinct and some things may overlap.

Non volatile storage and battery should be easily replaceble by the consumer.
RAM is justified as it reduces mismatch chnaces, reduces power \
consumpution when close to the processor.

### AC+DC/interfaces/frontend facing devices/thin clients

These should be the main workstations for any user. Desktops may misbehave at \
any time.
These are more integrated and have less points of failure

Focus on net battery life and peak efficiency by default. Scale up performance \
only when needed by the user.

Let the user reschedule non essential/non critical tasks to work only on \
charging/AC.

For syncing personal data, prioritize its safety incase the device fails, so \
try sync even on battery.

For app/system updates, it is better to auto reschedule its download and \
installs only when on AC and not being actively used.
Only alert about it when a manual action like a restart is required, else \
system works on it silently without interrupting the user, disrupting their \
tasks or corrupting their data.
Transactional app updates apply only when the app is closed. \
You can let the update data download but not necessarily directly apply it \
once downloaded.

Avoid running dedicated/sustained high performance compute tasks like BOINC on \
a phone.
Even with all safeguards like battery temperature limits, work only on AC and \
a high disk save interval, there are many other vectors to worry about.
These include battery micro cycling if no bypass charging, battery charge \
limits not being present, OOM, heavy swap utilization/storage wear, etc.
Not only BOINC but HPC in general. Battery powered devices should avoid it.

It is better to exchange your old phone for a new one rather than keeping it \
as a spare compute node.
Why?
All risks related to battery and storage wear apply, you dont have to worry \
about where to keep it or its disposal when exchanged.

Ideal devices include phones and efficiency focused laptops, such as Macbook \
Air, Macbook Neo and ARM based laptops suitable of running atomic linux.
Unideal devices include gaming laptops and Macbook Pro. They are not suitable \
for a quiet workspace and you should just use a headless device for offloading.

With this philosophy, you should get a less powerful but more efficient modern \
device over a an older inefficient powerful device.

### AC only/workers/backend servers

Ideally should work 24/7 and have no ability to sleep but still allow energy \
saving by deeper power states as long as uptime keeps ticking.
Should participate in DePIN type tasks, BOINC, local agentic tasks, etc.
Just to the point that user main tasks are not slowed down.

Have capability to scale up to any performance level dynamically and always be \
up to date, unlike interfaces.

Ideal devices include Mac Mini, Mac Studio, any standalone for factor PCs and servers.
Unfavorable device that loosely fit into this are all in one PCs that fit into \
monitors/keyboards directly or anything that is morphed into an HID device.

### Combined ideal usage

From a professional/high throughput setup perspective, workers should not be \
used as a primary workstation.
It creates friction, when shifting from one device to the other like you get a \
call and have to go somewhere urgently.
You were working on your desktop physically with something running and you \
cant interrupt it. You may lose access temporarily or temporarily for a long \
time if no remote access method is configured.
Instead the better choice is to use the portable as a thin client and not pack \
or force too much power on it, to offload tasks to the worker and use for longer.
Simply working on a physically single device maintains true work focus and \
reduces mental context switching.

Now this may seem biased potentially due to this being the case in my home \
where if I want to use the worker type device as a destop, I lose ethernet \
and thus, reduced remote accessiblity. Wifi works, but not ideal, even with \
strong extender. Ethernet is usually guaranteed high throughput and headless \
device can focus exclusively on the task without extra HID processing.
When I can use the ethernet, due to the router setup, the monitor cannot sit \
due to an a unfavorable place and it also cannot be placed there properly.

Ideal setup on worker

- Configure a network level remote access method like Tailscale.
- Obviously enable and secure SSH with anything other than password.
- Block direct external root access.
- Keep minimal user-end type programs on it.
- If physical display is needed, get a dummy plug.
- Configure something like Rustdesk for remote access.
- Disable sleep or hibernation
- Optionally, add a UPS.
- Make sure the ethernet cables actually clip and the make the click sound on \
connection as loose ones can cause major problems if no one is there to its access.
- Assign it a static local IP, both wifi and ethernet.
- Add wifi connections for fallbacks.
- Ensure wifi extenders use the main router as DHCP single source of truth.

Ideal setup on interface

- Avoid programs that process anything with no benefit to you, your device or \
your personal data 24/7. Syncing is permitted.
- Install the client counterparts to the remote access software on the worker.
- Always consider battery lifespan and storage wear concerns, but just enough \
that you actually get work done on it.
- Avoid Electron/complete browser instance type apps on it. You are better \
off using the OS native web browser and let the tab of the 'plaform' sleep in \
the background without closing it, unless full integration is needed like \
Podman/Docker desktop.
- Use modern and lightweight counterparts like Zed instead of VSCode
- Carry a power bank with you wherever you go.
- Offload tasks to worker devices

## Operating Systems

This is a rapidly evolving field that goes much beyond regular computers

A modern functioning OS should have the following features, not by a \
particular name, but a counterpart also works

- Immutability - Prevent user side breakage, keep base system secure.
It reduces the chances of a malicious script from implanting itself into a \
core directory or manipulating its contents.
- Hardware coordinated security - Like Secure boot, TPM 2.0, Apple Secure Enclave
- On disk encryption - Like LUKS2 or FileVault
- Atomiticy - Automatic system recovery and rollbacks, like bootc and SSV
- Reduced tunables - Let the system tune itself, or be locked to sensible \
modern defaults or heavily simplify user side tunables, while providing docs \
and info.
- Reproducibility - Reduced mutations make sure that issues are fixed as well \
as observed on multiple devices, letting the 'author' devs or contributors fix \
them faster.
- Transparent telemetry - Let devs fix issues fast without private user data transmission.
- More appliance like - Users can focus on their work over fixing issues \
manually. If they want to fix, fix it for the rest as well and publicly contribute.

Reduced customization isn't necessarily bad, it can promote unified workflows \
across machines. Users can prioritize work over customization in that case.
No customization is as bad as full customization - find a balance

## Licensing

GPL or any other forced copyleft license is better if you want to make an end \
product
Use permissive OSS licences for libraries or framworks

## Profitization

For profit vs Not for profit vs non-profit

For profit

- Works with the intention to monetize

Not for profit

- Registered as a for profit but tries to function as a non profit
- More sustainable in an unpredictable economy

Non profit

- Works exclusively for the intended goal
- Is fragile

## Practical refinement needed

Anything related to software in logical cases should be on a spectrum and power efficiency should be by default, but performance when required.(But the spectrum doesn't allow for illogical things like uselessly performing stuff at unreasonable cases). UI/UX animations are a waste of resources unless for accessibility and debugging or for cases for the UI to not be suddenly acting, especially in cases like touchscreen movement via fingers. Being systemd/GNOME(or SoCs as in hardware) like and being 'complete and well integrated' is better than what openrc and Hyprland with waybar are, even though they are arguably better. Using modern protocols is better but they are not to be confused with 5GHz and 2.4Ghz which are just different bands on a spectrum  for frequency and not protocols(like IPv6>IPv4). Compatibility for the old protocols should be ditched out by default, but compatibility should be optional and retrievable via downloads. Why should we keep maintaining compatibility? Of course not in the first place, we should switch to modern solutions or force the legacy projects to be developed to be modern accordingly. According to me, developers should introduce 2 layers for releases only - "One should be Stable Station the next one is Feature Station. In Feature station, features are added and but there is no guarantee of developers putting out bug fixes here. In Stable station, Features are released only after bug testing and assestation of bugs not being present or be minimal." Binaries, shouldn't be compiled centrally, but the workload should be distributed onto DPCs(explained later) as well as the central machine and then released as a whole to the community, not compiled by each user individually for their use. And it should be obvious by now but just in case, you should heavily prioritize open source. Freedom is not always the answer, since Atomic releases are the future. They perform upgrades in an excellent manner, with fallback mechanisms. So, what is the purpose of an ISO? It is to install an OS that is meant to be USED by the user, not continually tweaked in the system files, this means that your OS is not up to the mark, or not optimized. Is tweaking system files your job, is it productivity? User control is judicially correct because it is indeed their computer, but having a dynamically working system is a smarter choice. Sure you have to install applications, but that's not what tweaking is. When Windows updates, it updates the system, only during reboots, but rpm-ostreed.service manages this well. Not only is your current session undisturbed(apart from a small resource footprint in the background), but your system is too, updated silently. Again on modern protocols, they have active development usually meaning that they have a better approach to development. Another problem, people keep forking stuff instead of contributing to the original project! Not only will contributing to upstream projects give you support from a wider user base, components will be well integrated too. If the main founder of Wayland was granted to have his considerations thought about, maybe in another universe, Xorg would have been popular. The exception being the original upstream project has maintainers with different motos/mindsets/goals. There are 2 types of users. "It just works" or "It just works, but better", and it is obviously more logical to be a part of the latter, unless you deliberately want a setup and go approach like Debian. A funny fact is that tons of solutions such as AngularJS and Spelt Runes have been developed, but still most websites use jQuery. Also, cloud computing should be the future. This is because if we move onto the cloud there would be several advantages. A central united computer would be present, where there is a base OS that is always automatically updated like Silverblue, there would be data stored for each user with the modifications working with/overlaying the base. Each consumer would be handed a designated device which is only meant to view/interact with the cloud session. When the consumer uses the cloud pc via their designated device, the base os on the server will not be affected whatsoever but what the user will use is the base os overlaying their data stored on the server. There could be times when the base os on the server would update, causing weekly outages but is probably worth it considering the supercomputer's integration and ease of use to operate from the end of the server operators and the consumers. If the consumer wants to pay less monthly, they would have to buy a DPC(theres no definite full form for this acronym), which would be plugged into the consumer's house or wherever they want. The DPC would help compute for the server operators/company in a distributed way, in exchange for less money required for using the cloud computer. The consumer cannot use the DPC as a regular PC and is only meant for remote task assignment/use from the end of the enterprise/hosting company. This could also be a dream come true for repository maintainers as the server's base os would indirectly help/add to all user sessions. Users as well as the operators would have to spend less time resolving issues and just publish changes universally. This can heavily uplift community involvement and increase productivity. Ofc this already exists, but not in this way. During software development, before proceeding to add new features, fix your bugs first prior to adding new features. The base system would include binaries of applications intended for productive usage. The computer should be used for productivity, not useless ricing and tweaking. Its inner workings should be tweaked by itself within.
