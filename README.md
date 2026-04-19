# siggy-snap

This repository provides [Snap](https://snapcraft.io/) packaging for
[siggy](https://siggy.chat/), a terminal-based
[Signal](https://signal.org/) messenger client.

I imagine I'll release this to the official Snap store once I've sorted
out the confinement, but for now if you'd like to use it, follow these
steps:

1. [Set up Snapcraft](https://documentation.ubuntu.com/snapcraft/stable/how-to/set-up-snapcraft/)
2. Check out this repository
3. Pack the Snap:
```bash
snapcraft pack
```
4. Install the Snap:
```bash
snap install ./siggy_1.6.0_amd64.snap --dangerous
```
5. Connect the interface that allows siggy to access signal-cli's data directory:
```bash
snap connect siggy:signal-cli-data
```
