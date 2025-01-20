# GUI Scale COSMIC Desktop Applet
=====================================


## About
--------

A secure, memory-safe Tailscale GUI management applet for System76 COSMIC desktop environment.


## Project Overview
-----------------

Provides a user-friendly interface for managing Tailscale configurations within COSMIC.


## Key Features
-------------

* Secure Tailscale network (tailnet) management
* Memory-safe Rust implementation
 + Ownership system for memory safety
 + No unsafe code blocks
 + Validated external data
 + Buffer overflow protection
* Comprehensive error handling
* Integration with system security policies
 + Proper permission handling
 + Minimal system privileges


## Security Architecture
----------------------

Layered security approach:

1. **Privilege Management**: Minimal required permissions, capability isolation
2. **Error Handling**: Rust's built-in error types, no information leakage


## Dependencies
------------

1. Install Tailscale
2. Run: `sudo tailscale set --operator=$USER`


## Screenshots
-------------

![gui-scale-applet-panel](/screenshots/gui-scale-panel.png)
![gui-scale-applet-open](/screenshots/gui-scale-applet-open.png)


## Installation
--------------

### Arch Linux

1. Install from AUR: `gui-scale-applet`
2. Alternatively, use an AUR helper: `yay -S gui-scale-applet`

### Fedora/Fedora-based

1. `sudo dnf copr enable bhh32/gui-scale-applet`
2. `sudo dnf update --refresh`
3. `sudo dnf install -y gui-scale-applet`

### Debian/Ubuntu/Pop!OS

1. Download deb package from releases section.
2. Install manually.

### Other Distros

1. `git clone https://github.com/cosmic-utils/gui-scale-applet.git`
2. `cd gui-scale-applet`
3. `sudo just install`