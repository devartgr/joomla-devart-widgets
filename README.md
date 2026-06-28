# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, business, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.7.0-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widget builder designed for editorial websites, magazines, portals, newspapers, corporate websites, business directories, and high-traffic production environments.

Create professional frontend content blocks using multiple templates, flexible content sources, cache-first rendering, production-safe import/export tools, responsive typography controls, template-aware customization, and modern Joomla 6 architecture.

Version **1.7.0** introduces the first **multi-source architecture**, allowing the same rendering engine and templates to display content from both Joomla Articles and DevArt Business.

Built specifically for Joomla 6 and PHP 8.2+ with strict typing, modern MVC architecture, and enterprise-oriented performance principles.

---

## Features

### Professional Widget Templates

Included templates:

- Full Width Overlay Grid
- Clean Editorial Cards
- Alternating Magazine
- Hero + Secondary Grid
- Timeline Editorial
- Breaking News Ticker
- Compact News List
- Hover Feature Cards
- Simple Color Cards
- Hero Feature Grid
- Numbered Top Stories
- Minimal Editorial List

Perfect for:

- homepage content blocks
- featured sections
- category highlights
- editorial landing pages
- sidebar widgets
- trending content
- magazine layouts
- business listings
- portal front pages
- responsive content blocks

---

## Multiple Content Sources

Supported sources:

### Joomla Content

- Latest Articles
- Selected Articles
- Category Articles
- Featured Articles
- Related Articles
- Custom Items

### DevArt Business

New in **v1.7.0**

Display business directory content using exactly the same templates already available for Joomla Articles.

Business source supports:

- All Business Categories
- Selected Business Categories
- Include Child Categories
- Ordering
- Maximum Items

When DevArt Business is selected, the administrator interface automatically hides article-specific options for a cleaner configuration experience.

---

## Custom Items Builder

Create completely custom widget content without Joomla articles.

Supported fields:

- Title
- Subtitle
- Intro Text
- Image
- Link
- Link Target
- Badge Label
- Read More Text
- Optional Date

Features:

- unlimited custom items
- move up / move down ordering
- template compatible rendering

---

## Unified Rendering Engine

One rendering engine powers every supported source.

The same frontend templates automatically work with:

- Joomla Articles
- DevArt Business

Future DevArt applications can reuse the same architecture without requiring additional frontend templates.

---

## Template and Theme Controls

DevArt Widgets includes template-aware administrator options designed to keep the interface clean.

Features:

- theme presets
- custom theme mode
- custom colors
- overlay opacity
- overlay direction
- template-aware option visibility
- source-aware option visibility

Only relevant settings are displayed depending on the selected template and content source.

---

## Responsive Typography

Frontend text can be adjusted independently for mobile devices.

Features:

- responsive mobile text
- mobile text scale
- desktop typography controls
- rem-based typography
- template-safe rendering

---

## Image Handling

Supported image modes:

- Crop
- Original

Features:

- predictable editorial layouts
- crop positioning
- lazy loading
- thumbnail generation
- template-safe image rendering

The experimental Resize mode was removed to ensure consistent frontend layouts.

---

## Cache-first Architecture

Designed for high-traffic Joomla websites.

Features:

- widget query caching
- configurable cache duration
- module cache support
- Joomla Page Cache compatibility
- Cloudflare friendly output
- CDN friendly rendering
- minimal frontend overhead
- lightweight CSS
- no frontend database writes

---

## Thumbnail Cache Management

Production-safe thumbnail lifecycle management.

Features:

- automatic cleanup
- configurable retention
- administrator-only maintenance
- throttled cleanup
- dashboard statistics
- manual cleanup tools
- full thumbnail cache clear

---

## Production-safe Import / Export

Designed for backups and migrations.

Features:

- widget export
- widget import
- preserve original IDs
- restore-friendly workflows
- production migration support

---

## Administrator Features

- Dashboard
- Widget Manager
- Create Widgets
- Duplicate Widgets
- Import / Export
- Template Overview
- Global Configuration
- Cache Tools
- Thumbnail Maintenance
- Cache Status
- Joomla ACL

---

## Production Safety

Operational hardening includes:

- Keep Data uninstall option
- rollback-friendly updates
- non-destructive upgrades
- safe restore workflows
- controlled cache handling
- administrator-only maintenance

---

## Included Extensions

- com_devartwidgets
- mod_devartwidget

---

## Requirements

- Joomla 6.x
- PHP 8.2+

---

## Installation

1. Download the latest release.
2. Open:

   `System → Extensions → Install`

3. Upload the package ZIP.
4. Open:

   `Components → DevArt Widgets`
5. Create widgets.
6. Publish module instances.

---

## Joomla Native Updates

Supports Joomla native updates via GitHub.

Update server:

`https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/update.xml`

---

## Performance

Designed for production deployments.

Features:

- widget query caching
- cache-first rendering
- module cache support
- Cloudflare friendly output
- CDN friendly rendering
- lightweight frontend CSS
- widget-level cache isolation

Suitable for:

- newspapers
- magazines
- editorial websites
- portals
- business directories
- corporate websites
- high-traffic Joomla installations

---

## Security Highlights

- Joomla ACL
- CSRF protection
- Joomla Query Builder
- XSS-safe output
- strict validation
- namespaced architecture
- safe cache handling
- JED-ready packaging

---

## Compatibility

Supported:

- Joomla 6.x
- PHP 8.2+
- Joomla Native Updates
- Modern Joomla MVC

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- Legacy PHP

---

## Current Version

### 1.7.0

---

## Changelog Highlights

### v1.7.0

Added:

- native DevArt Business source
- Business Categories support
- All Business Categories mode
- unified business rendering engine
- business support across all existing widget templates

Improved:

- multi-source architecture
- source-aware administrator interface
- automatic hiding of article-only options
- consistency with DevArt Slider source handling
- long-term platform extensibility

Compatibility:

- existing Joomla Articles widgets continue to work without changes
- no database changes
- no migration required

---

## Production Recommendations

Frontend:

- enable widget caching
- enable Joomla caching
- use module cache where appropriate
- optimize images before upload
- use Crop mode for editorial layouts

Infrastructure:

- Cloudflare CDN
- Joomla Cache
- PHP OPcache
- SSD storage
- modern PHP versions

---

## Known Notes

- Always test updates on staging before production deployment.
- Thumbnail maintenance runs only from the Joomla administrator.
- DevArt Business source requires the DevArt Business component to be installed.

---

## Author

Kostas Stathopoulos  
DevArt  
https://devart.gr

GitHub Repository:

https://github.com/devartgr/joomla-devart-widgets

---

## Disclaimer / Limitation of Liability

This software is provided "as is", without warranty of any kind.

DevArt shall not be liable for data loss, downtime, rendering issues, cache conflicts, production failures, or issues resulting from use or misuse of this software.

Always test on staging before production deployment and maintain proper backups.

---

## License

GNU General Public License v3 or later
