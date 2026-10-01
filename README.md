# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, business, events, video, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-2.0.0-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widget builder designed for editorial websites, magazines, portals, newspapers, corporate websites, business directories, event websites, video portals, and high-traffic production environments.

Create professional frontend content blocks using multiple templates, multiple native content sources, Custom Lists, cache-first rendering, production-safe import/export tools, responsive typography controls, template-aware customization, and modern Joomla 6 architecture.

Version **2.0.0** activates the shared **DevArt Sources** plugin engine by default (`source_engine=plugin`) with automatic legacy fallback. The install package embeds a pinned `pkg_devartsources` companion (same pin as DevArt Slider 2.0.0) and installs or upgrades it when missing or older. Host-local Custom Items / Custom Lists stay in-product. Explicit Options choices (`legacy` / `shadow` / `plugin`) are preserved on update.

Built specifically for Joomla 6 and PHP 8.3+ with strict typing, modern MVC architecture, and enterprise-oriented performance principles.

---

## What’s new in 2.0.0

- Soft cutover to shared Sources providers (Articles, DevArt Business, Events, Video)
- Build-time bundled `pkg_devartsources` 1.0.0 — one ZIP install for Widgets + Sources
- Plugin cache TTL ceiling, empty-store parity, warm visibility recheck
- Safer fail-closed paths (unknown source types, SafeLog, diagnostics on Dashboard)
- Legacy engines retained as fallback until a later soak-based cleanup

---

## Requirements

- Joomla 6.0+
- PHP 8.3+

## Package

- Package: `pkg_devartwidgets`
- Version: `2.0.0`
- SHA-256: `758b2db59a977306ef6b2d98721165d4a4ab4f83a08f435240a891c814c6d880`
- Extensions: `com_devartwidgets`, `mod_devartwidget`, `plg_content_devartwidgets`
- Bundled companion: `pkg_devartsources` 1.0.0
- Languages: 15 locales (`en-GB`, `el-GR`, `fr-FR`, `de-DE`, `es-ES`, `it-IT`, `pt-PT`, `cs-CZ`, `nl-NL`, `pl-PL`, `ru-RU`, `uk-UA`, `ja-JP`, `tr-TR`, `zh-CN`)

## Install / Update

1. Install or update `pkg_devartwidgets_v2.0.0.zip` via Joomla Installer (or Joomla Update when advertised).
2. Sources is installed/upgraded automatically from the bundled companion when needed.
3. Confirm Components → DevArt Widgets → Options → **Source engine** is `Plugin` (or keep your explicit choice).

## Links

- Releases: https://github.com/devartgr/joomla-devart-widgets/releases
- Update stream: https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/update.xml
- Changelog: https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/changelog.xml
- Site: https://devart.gr

## License

GNU General Public License version 3 or later.
