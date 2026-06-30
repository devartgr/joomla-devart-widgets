# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, business, events, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.8.0-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widget builder designed for editorial websites, magazines, portals, newspapers, corporate websites, business directories, event websites, and high-traffic production environments.

Create professional frontend content blocks using multiple templates, multiple native content sources, cache-first rendering, production-safe import/export tools, responsive typography controls, template-aware customization, and modern Joomla 6 architecture.

Version **1.8.0** completes the first generation of the **DevArt multi-source rendering architecture**, allowing the same rendering engine and frontend templates to display Joomla Articles, DevArt Business, DevArt Events and Custom Items.

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
- event listings
- portal front pages
- responsive content blocks

---

## Multiple Content Sources

### Joomla Content

- Latest Articles
- Selected Articles
- Category Articles
- Featured Articles
- Related Articles

### DevArt Business

Display business directory content using all existing widget templates.

Business source supports:

- All Business Categories
- Selected Business Categories
- Include Child Categories
- Maximum Items

Business-specific administrator options are displayed automatically while article-only options are hidden.

### DevArt Events

**New in v1.8.0**

Display event listings using exactly the same widget templates.

Event source supports:

- Today
- Upcoming
- Past
- All
- Featured

Category options:

- All Event Categories
- Selected Event Categories
- Include Child Categories
- Maximum Items

Event ordering is handled automatically using the same event date logic as DevArt Events.

### Custom Items

Create completely custom widget content independent of Joomla content.

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

---

## Unified Multi-Source Rendering Engine

A single rendering engine powers every supported source.

Supported sources:

- Joomla Articles
- DevArt Business
- DevArt Events
- Custom Items

All frontend templates automatically work across every supported content source without requiring separate template implementations.

This architecture provides a consistent user experience while simplifying future DevArt integrations.

---

## Template and Theme Controls

Template-aware administrator interface.

Features:

- theme presets
- custom theme mode
- custom colors
- overlay opacity
- overlay direction
- template-aware option visibility
- source-aware option visibility

Only settings relevant to the selected source and template are displayed.

---

## Responsive Typography

Frontend typography includes:

- responsive mobile text
- mobile text scaling
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
- template-safe rendering

The experimental Resize mode has been removed to ensure consistent frontend layouts.

---

## Cache-first Architecture

Designed for high-traffic production environments.

Features:

- widget query caching
- configurable cache duration
- module cache support
- Joomla Page Cache compatibility
- Cloudflare friendly rendering
- CDN friendly output
- minimal frontend overhead
- lightweight CSS architecture
- no frontend database writes

---

## Thumbnail Cache Management

Features:

- automatic cleanup
- configurable retention
- administrator-only maintenance
- throttled cleanup
- dashboard statistics
- manual cleanup
- full thumbnail cache clear

---

## Production-safe Import / Export

Features:

- widget export
- widget import
- preserve original IDs when possible
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

Features:

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

Supports Joomla native updates through GitHub.

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
- widget-level cache isolation
- lightweight frontend CSS

Suitable for:

- newspapers
- magazines
- editorial websites
- portals
- business directories
- event websites
- corporate websites
- high-traffic Joomla installations

---

## Security Highlights

- Joomla ACL
- CSRF protection
- Joomla Query Builder
- XSS-safe rendering
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
- Modern Joomla MVC Architecture

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- Legacy PHP versions

---

## Current Version

### 1.8.0

---

## Changelog Highlights

### v1.8.0

Added:

- native DevArt Events source
- Today, Upcoming, Past, All and Featured event filtering
- Event Categories support
- All Event Categories mode
- unified event-date rendering using the DevArt Events engine
- event support across all existing widget templates

Improved:

- expanded multi-source architecture
- source-aware administrator interface
- automatic hiding of article-only options
- unified event selection across DevArt Events, Slider and Widgets
- long-term platform extensibility

Compatibility:

- existing Joomla Articles widgets continue to work unchanged
- existing DevArt Business widgets continue to work unchanged
- no database changes
- no migration required

---

## Production Recommendations

Frontend:

- enable widget caching
- enable Joomla caching
- use module cache where appropriate
- optimize images before upload
- use Crop mode for predictable layouts

Infrastructure:

- Cloudflare CDN
- Joomla Cache
- PHP OPcache
- SSD storage
- modern PHP versions

---

## Known Notes

- Always test updates on a staging environment before production deployment.
- Thumbnail maintenance runs only from the Joomla administrator.
- DevArt Business source requires DevArt Business when used.
- DevArt Events source requires DevArt Events when used.

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

Always test on staging environments before production deployment and maintain proper backups.

---

## License

GNU General Public License v3 or later
