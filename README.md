# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, business, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.6.4-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widget builder designed for editorial websites, magazines, portals, newspapers, corporate websites, and high-traffic production environments.

Create professional frontend content blocks using multiple templates, flexible content sources, cache-first rendering, production-safe import/export tools, and modern Joomla 6 architecture.

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
- featured article sections
- category highlights
- editorial landing pages
- sidebar widgets
- trending content
- magazine layouts
- portal front pages
- mobile-friendly article lists

---

### Flexible Content Sources

Supported content sources:

- Latest Articles
- Selected Articles
- Category Articles
- Featured Articles
- Related Articles
- Custom Items

Filtering options:

- category filtering
- featured filtering
- article ordering
- maximum items
- skip offset
- exclude current article
- publication-aware selection

---

### Custom Items Builder

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

- add unlimited custom items
- drag-style ordering controls
- move up / move down support
- template compatible rendering

---

### Cache-first Frontend Architecture

Designed for high-traffic production environments.

Features:

- widget query caching
- configurable cache duration
- cache-safe rendering
- Joomla Page Cache compatibility
- Cloudflare friendly output
- CDN friendly rendering
- minimal frontend overhead
- lightweight CSS architecture
- no frontend database writes

---

### Thumbnail Cache Management

Production-safe thumbnail lifecycle management.

Features:

- automatic thumbnail retention cleanup
- configurable Thumbnail Retention Days setting
- administrator-only maintenance execution
- throttled cleanup workflow
- thumbnail cache statistics dashboard
- manual thumbnail cleanup tools
- full thumbnail cache clear tools

Designed to prevent uncontrolled thumbnail growth while avoiding frontend performance impact.

---

### Production-safe Import / Export

Backup and migration friendly workflows.

Features:

- widget export
- widget import
- preserve original widget IDs when possible
- safe fallback import
- restore-friendly workflows
- production migration support

Helps prevent module assignment issues during backup restore and migration operations.

---

### Administrator Features

- Dashboard interface
- Widget Manager
- Create Widgets
- Edit Widgets
- Duplicate Widgets
- Import Widgets
- Export Widgets
- Template Overview
- Global Configuration
- Cache Tools
- Thumbnail Maintenance Tools
- Cache Status Visibility
- Joomla ACL Permissions

---

### Production Safety

Operational hardening included.

Features:

- Keep Data uninstall option
- rollback-friendly updates
- non-destructive update workflows
- safe widget restore operations
- controlled cache handling
- thumbnail retention management
- administrator-only maintenance operations

---

## Included Extensions

This package installs:

- com_devartwidgets
- mod_devartwidget

---

## Requirements

- Joomla 6.x
- PHP 8.2+

---

## Installation

1. Download the latest release
2. Open:

   `System → Extensions → Install`

3. Upload the package ZIP
4. Open:

   `Components → DevArt Widgets`

5. Create widgets
6. Publish module instances

---

## Joomla Native Updates

Supports Joomla native updates through GitHub.

Update location:

`System → Extensions → Update`

Update server:

`https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/update.xml`

---

## Performance

Designed for production deployments and high-traffic websites.

Features:

- widget query caching
- cache-first rendering
- minimal frontend overhead
- widget-level cache isolation
- lightweight frontend CSS
- Cloudflare friendly output
- CDN friendly rendering
- administrator-only maintenance operations

Suitable for:

- editorial websites
- newspapers
- magazines
- portals
- business websites
- content-heavy Joomla installations
- high-traffic production environments

---

## Security Highlights

- Joomla ACL support
- CSRF protected administrator actions
- Joomla query builder protection
- XSS-safe output rendering
- strict input validation
- namespaced architecture
- safe cache file handling
- JED-ready packaging

---

## Compatibility

Supported:

- Joomla 6.x
- PHP 8.2+
- Joomla Native Update System
- Modern Joomla MVC Architecture

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- Legacy PHP versions

---

## Current Version

### 1.6.4

---

## Changelog Highlights

### v1.6.4

Added:

- automatic thumbnail retention cleanup
- thumbnail cache maintenance tools
- thumbnail cache statistics dashboard
- configurable thumbnail lifecycle management

Fixed:

- inactive Thumbnail Retention Days setting
- uncontrolled thumbnail cache growth

Improved:

- long-term thumbnail cache management
- administrator maintenance workflows

### v1.6.3

Fixed:

- dashboard cache clear CSRF workflow
- cache maintenance consistency

### v1.6.0

Added:

- preserve original widget IDs
- Keep Data uninstall option
- rollback-friendly update workflows
- dashboard cache tools

---

## Production Recommendations

Recommended settings:

Frontend:

- enable widget caching
- keep Joomla caching enabled
- use cache-first rendering
- optimize images before upload

Infrastructure:

- Cloudflare CDN
- Joomla Cache
- PHP OPcache
- modern PHP versions
- SSD storage

---

## Known Notes

- Always test updates on a staging environment before deploying to production.
- Thumbnail retention cleanup operates only from the Joomla administrator area and never during frontend rendering.

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
