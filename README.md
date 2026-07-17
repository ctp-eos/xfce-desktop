# CTP-EOS XFCE Desktop

## Overview

CTP-EOS XFCE Desktop is the desktop environment foundation for the CTP-EOS Linux platform.

This repository maintains a customized XFCE desktop stack built from upstream XFCE components, with CTP-EOS branding, configurations, patches, and automation layered separately from the upstream source tree.

The goal is to provide a stable, lightweight, customizable desktop experience while maintaining a clean separation between upstream XFCE development and CTP-EOS-specific modifications.

---

# Repository Structure

```
xfce-desktop/
│
├── upstream/
│   ├── xfdesktop/
│   ├── xfce4-panel/
│   ├── xfwm4/
│   ├── thunar/
│   ├── xfce4-session/
│   ├── xfce4-settings/
│   ├── xfconf/
│   └── other XFCE components
│
├── branding/
│   ├── wallpapers/
│   ├── themes/
│   ├── icons/
│   ├── backgrounds/
│   └── CTP-EOS visual assets
│
├── config/
│   ├── xfce4/
│   ├── gtk/
│   ├── sessions/
│   └── default desktop settings
│
├── configs/
│   └── existing CTP-EOS configuration assets
│
├── patches/
│   ├── xfdesktop/
│   ├── xfwm4/
│   ├── xfce4-panel/
│   └── source modifications
│
├── scripts/
│   ├── build scripts
│   ├── deployment tools
│   └── automation utilities
│
└── .gitignore
```

---

# Development Philosophy

CTP-EOS maintains a downstream development model:

* `upstream/` contains the XFCE source baseline.
* `branding/` contains CTP-EOS identity and visual design.
* `config/` contains default user experience settings.
* `patches/` contains intentional source-level modifications.
* `scripts/` contains development and build automation.

Changes should be isolated into the appropriate layer rather than directly modifying upstream source whenever possible.

---

# Upstream Components

This repository currently tracks XFCE desktop components including:

* xfdesktop
* xfwm4
* xfce4-panel
* Thunar
* xfce4-session
* xfce4-settings
* xfconf
* libxfce4ui
* libxfce4util
* xfce4-terminal
* xfce4-appfinder
* xfce4-notifyd
* xfce4-power-manager
* xfce4-pulseaudio-plugin
* xfce4-whiskermenu-plugin
* Mousepad
* Ristretto

---

# Future Development Roadmap

## Branding Layer

Future CTP-EOS desktop identity work will include:

* CTP-EOS GTK themes
* XFWM window manager themes
* custom wallpapers
* icon themes
* login/session branding
* desktop artwork packages

---

## Default Desktop Experience

Future configuration work:

* XFCE panel layouts
* application menu customization
* default keyboard shortcuts
* desktop appearance presets
* power management defaults
* notification settings
* file manager defaults

---

## Build and Release Automation

Future scripts will support:

* automated XFCE desktop builds
* package generation
* testing environments
* ISO integration
* deployment workflows

---

## Patch Management

Source changes will be maintained through:

* clearly documented patches
* component-specific directories
* upstream comparison tracking
* reproducible changes

---

# Contributing

Contributions should maintain the separation between:

1. Upstream XFCE source
2. CTP-EOS customizations
3. Build and deployment tooling

Before submitting changes:

* document the purpose of modifications
* keep patches isolated
* avoid committing generated build files
* maintain reproducible build processes

---

# License

This repository contains upstream XFCE components and CTP-EOS-specific modifications.

Individual upstream components remain subject to their respective licenses.

CTP-EOS additions are maintained according to their project licensing terms.
