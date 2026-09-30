---
name: cosmic-desktop-customization
description: "Use to customize Pop!_OS COSMIC themes, dock, and styles."
version: 1.0.0
author: Hermes Agent
license: MIT
platforms: [linux]
metadata:
  hermes:
    tags: [cosmic, pop-os, linux, desktop, theming, wayland]
    category: system-customization
---

# COSMIC Desktop Customization

Manage and theme the Pop!_OS COSMIC desktop environment (Epoch 1, Wayland/Rust).

## When to Use
Use when configuring, theming, or altering layout settings on Pop!_OS 24.04+ (COSMIC DE), including dock behavior, panel applets, frosted blur, window control placement, color palettes, and GTK compatibility.

## Core Concepts
- COSMIC DE does not use GNOME Shell or Mutter. GNOME Shell extensions and GNOME Shell CSS themes do not affect the desktop.
- COSMIC stores desktop configurations in `~/.config/cosmic/` using individual parameter files or Rust Object Notation (RON).
- Non-COSMIC apps (GTK 3/4, Electron) continue to read `~/.config/gtk-3.0/settings.ini`, `~/.config/gtk-4.0/settings.ini`, and standard XDG icon directories (`~/.local/share/icons`).

## Workflow

### 1. Theme and Color Customization
COSMIC Dark theme parameters live in `~/.config/cosmic/com.system76.CosmicTheme.Dark/v2/`:
- `primary`: Background and surface colors in RON format (`base: "#1E1E1EFF", component: (...)`).
- `accent_button`: Accent and highlight colors.
- `corner_radii`: Border radius settings (`radius_s`, `radius_m`, `radius_l`).
- `frosted`: Blur strength (`Medium`, `Heavy`).
- `frosted_windows`, `frosted_applets`, `frosted_system_interface`: Boolean switches (`true`/`false`).

### 2. Dock Configuration
Dock settings live in `~/.config/cosmic/com.system76.CosmicPanel.Dock/v1/`:
- Floating centered dock: Set `expand_to_edges` to `false`, `anchor` to `Bottom`.
- Autohide: Set `autohide` to `true` and `autohide_behavior` to `OnDemand` (or `Never`).
- Translucency: Set `opacity` (e.g. `0.85`), `border_radius` (e.g. `16`), `margin` (e.g. `6`).
- Applet layout (`plugins_center`): To keep a clean app dock, omit workspace buttons and keep `com.system76.CosmicAppList` and `com.system76.CosmicPanelLauncherButton`.

### 3. Top Panel Configuration
Panel settings live in `~/.config/cosmic/com.system76.CosmicPanel.Panel/v1/`:
- Edge-to-edge bar: Set `expand_to_edges` to `true`, `anchor` to `Top`, `size` to `XS`.
- Center plugins: Typically holds `com.system76.CosmicAppletTime`.

### 4. Icons, Cursors, and GTK Fallback
For third-party apps to match the desktop style:
1. Install icon themes to `~/.local/share/icons/` (e.g. WhiteSur-dark, Papirus-Dark).
2. Set GTK 3/4 settings in `~/.config/gtk-3.0/settings.ini` and `~/.config/gtk-4.0/settings.ini`.
3. Apply via gsettings:
   ```bash
   gsettings set org.gnome.desktop.interface icon-theme '<name>'
   gsettings set org.gnome.desktop.interface cursor-theme '<name>'
   gsettings set org.gnome.desktop.interface gtk-theme '<name>'
   ```

## Pitfalls
- Do not attempt to install GNOME extensions on Pop!_OS 24.04 COSMIC; the shell is not running and extension installers will fail or be ignored.
- COSMIC settings daemon watches `~/.config/cosmic/` files live, but syntax errors in RON files can cause themes to fallback to defaults. Validate formatting before overwriting.
