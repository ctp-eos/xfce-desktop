
---

# Development Philosophy

CTP-EOS maintains a downstream development model:

* `upstream/` contains the XFCE source baseline.
* `branding/` contains CTP-EOS identity and visual design.
* `config/` contains default user experience settings.
* `patches/` contains intentional source-level modifications.
* `plugins/` contains the curated XFCE plugin ecosystem.
* `packaging/` contains distribution build resources.
* `scripts/` contains development and build automation.
* `docs/` contains project architecture and contributor documentation.

Changes should be isolated into the appropriate layer rather than directly modifying upstream source whenever possible.

This approach keeps upstream XFCE components maintainable while allowing CTP-EOS-specific improvements to evolve independently.

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

Additional XFCE components and plugins will be integrated through the appropriate project layers.

---

# XFCE Plugin Strategy

CTP-EOS maintains a curated XFCE plugin ecosystem focused on:

* desktop usability
* system visibility
* stability
* lightweight operation
* integration with the CTP-EOS workflow

Plugins are maintained separately from the core XFCE source tree.

Planned plugin categories include:

## Desktop Integration

* Application launchers
* Menu customization
* Clipboard management
* Screenshot utilities

## System Monitoring

* CPU monitoring
* Memory monitoring
* Network monitoring
* Hardware sensors
* Disk activity monitoring

## User Information

* Weather information
* System status widgets
* Custom CTP-EOS status utilities

Plugin selections will be managed through manifests to provide reproducible desktop builds.

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
* user experience presets

---

## Build Pipeline

The CTP-EOS XFCE desktop build process will follow:

1. Import upstream XFCE sources
2. Apply CTP-EOS patches
3. Apply branding assets
4. Apply default configurations
5. Install selected plugins
6. Build packages
7. Integrate into CTP-EOS releases

The goal is a reproducible desktop build process where upstream components and CTP-EOS customizations remain clearly separated.

---

## Build and Release Automation

Future scripts will support:

* automated XFCE desktop builds
* package generation
* testing environments
* ISO integration
* deployment workflows
* upstream synchronization

---

## Patch Management

Source changes will be maintained through:

* clearly documented patches
* component-specific directories
* upstream comparison tracking
* reproducible changes
* isolated modifications

---

# Contributing

Contributions should maintain the separation between:

1. Upstream XFCE source
2. CTP-EOS customizations
3. Plugin selections
4. Build and deployment tooling

Before submitting changes:

* document the purpose of modifications
* keep patches isolated
* avoid committing generated build files
* maintain reproducible build processes
* preserve upstream compatibility

---

# License

This repository contains upstream XFCE components and CTP-EOS-specific modifications.

Individual upstream components remain subject to their respective licenses.

CTP-EOS additions are maintained according to their project licensing terms.
