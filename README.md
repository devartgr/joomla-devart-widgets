# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, business, events, video, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-2.0.1-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widget builder designed for editorial websites, magazines, portals, newspapers, corporate websites, business directories, event websites, video portals, and high-traffic production environments.

Create professional frontend content blocks using multiple templates, multiple native content sources, Custom Lists, cache-first rendering, production-safe import/export tools, responsive typography controls, template-aware customization, and modern Joomla 6 architecture.

Version **2.0.1** completes the **M7 plugin-only** cut for shared Articles / Business / Events / Video sources (legacy, shadow, and Options engine switch removed). The install package embeds pinned `pkg_devartsources` **1.0.1** (same pin as DevArt Slider **2.0.2**) and installs or upgrades it when missing or older — never downgrades. Host-local Custom Items / Custom Lists stay in-product. Shared sources fail closed when Sources is unavailable.

Built specifically for Joomla 6 and PHP 8.3+ with strict typing, modern MVC architecture, and enterprise-oriented performance principles.

---

## What’s new in 2.0.1

- M7 plugin-only for shared Articles / Business / Events / Video (no legacy/shadow fallback)
- Re-pin embedded `pkg_devartsources` to **1.0.1** (same as Slider 2.0.2)
- Admin Status columns use jgrid published icons; Play/Pause video aria-label from site language
- Thumb retention clears `.webp`/`.jpeg`; warm-path and cache-key hygiene
- Keep **2.0.0** on GitHub Releases for **manual** rollback only — no official update-server downgrade

---

## Requirements

- Joomla 6.0+
- PHP 8.3+

## Package

- Package: `pkg_devartwidgets`
- Version: `2.0.1`
- SHA-256: `e783fdb4f3bea0528048bdae36a1d41e36041dc94a1d377ad94b9267b0218f97`
- Extensions: `com_devartwidgets`, `mod_devartwidget`, `plg_content_devartwidgets`
- Bundled companion: `pkg_devartsources` 1.0.1
- Languages: 15 locales (`en-GB`, `el-GR`, `fr-FR`, `de-DE`, `es-ES`, `it-IT`, `pt-PT`, `cs-CZ`, `nl-NL`, `pl-PL`, `ru-RU`, `uk-UA`, `ja-JP`, `tr-TR`, `zh-CN`)

## Install / Update

1. Install or update `pkg_devartwidgets_v2.0.1.zip` via Joomla Installer (or Joomla Update when advertised).
2. Sources is installed/upgraded automatically from the bundled companion when needed (never downgraded).
3. Shared sources require DevArt Sources; Custom Items / Custom Lists remain host-local.

## Links

- Releases: https://github.com/devartgr/joomla-devart-widgets/releases
- Update stream: https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/update.xml
- Changelog: https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/changelog.xml
- Site: https://devart.gr

## License

GNU General Public License version 3 or later.
