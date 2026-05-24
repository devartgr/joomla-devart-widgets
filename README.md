# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.2%2B-green)
![Release](https://img.shields.io/badge/Version-1.6.3-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widgets package built for editorial websites, magazines, portals, newspapers, and high-traffic content environments.

It provides lightweight cache-first frontend rendering, professional editorial widget templates, production-safe import/export workflows, administrator dashboard tools, and modern Joomla 6 architecture.

Designed specifically for Joomla 6 with strict typing, clean MVC architecture, and zero legacy baggage.

---

## Features

### Professional Editorial Templates

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

Use cases:

- homepage editorial blocks
- latest news sections
- magazine landing pages
- category featured blocks
- sidebar widgets
- trending story blocks
- compact article lists
- breaking news sections
- mobile-friendly editorial layouts

---

### Flexible Content Sources

Widget sources:

- Latest Articles
- Selected Articles
- Category Filtered Articles
- Featured Articles
- Current Article Context
- Custom Items

Filtering options:

- category filtering
- featured filtering
- ordering controls
- article limits
- skip offset
- exclude current article
- publication-aware article selection

---

### Cache-first Frontend Performance

Built for production and high traffic environments.

Features:

- frontend widget query caching
- configurable cache duration
- hard performance limits
- Joomla Page Cache friendly rendering
- Cloudflare friendly frontend behavior
- CDN-friendly output
- minimal frontend overhead
- lightweight CSS rendering
- no heavy frontend frameworks

---

### Production-safe Import / Export

Backup-safe administrator workflows.

Features:

- widget export
- widget import
- preserve original widget IDs when possible
- safe fallback import if ID conflict exists
- restore-friendly production workflows

This prevents module assignments from breaking during widget restore scenarios.

---

### Administrator Features

- Dashboard production management interface
- Widget manager
- Create / Edit widgets
- Duplicate widgets
- Import / Export widgets
- Template overview
- Global configuration
- Cache management tools
- Widget cache clear action
- Dashboard cache status visibility
- Joomla ACL permissions support

---

### Production Safety

Operational hardening included:

- Keep Data uninstall option
- controlled rollback / downgrade-friendly workflow
- non-destructive update behavior
- safe widget restore workflows
- cache-safe frontend rendering strategy

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

1. Download latest release
2. Open:

`System → Extensions → Install`

3. Upload package ZIP
4. Open:

`Components → DevArt Widgets`

5. Create widgets
6. Publish module instances

---

## Joomla Native Updates

Supports Joomla native updates via GitHub.

Update location:

`System → Extensions → Update`

Update server:

`https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/update.xml`

---

## Performance

Designed for production and high-traffic environments.

Features:

- widget query caching
- cache-first rendering
- minimal frontend overhead
- safe repeated rendering
- widget-level cache isolation
- lightweight frontend CSS
- CDN-friendly output

Suitable for:

- editorial websites
- magazine portals
- news websites
- content-heavy Joomla installations
- high traffic production deployments

---

## Security Highlights

- Joomla ACL support
- CSRF-safe administrator actions
- Joomla query builder protection
- XSS-safe rendering
- strict input validation
- namespaced architecture
- JED-ready packaging
- safe cache file handling

---

## Compatibility

Supported:

- Joomla 6.x
- PHP 8.2+
- Joomla native update system
- modern Joomla MVC architecture

Not supported:

- Joomla 3
- Joomla 4
- Joomla 5
- legacy PHP versions

---

## Current Version

1.6.3

---

## Changelog Highlights

### v1.6.3

Fixed:

- dashboard widget cache clear CSRF workflow
- administrator cache maintenance action consistency

### v1.6.0

Added:

- preserve original widget IDs during restore
- Keep Data uninstall option
- rollback-friendly production workflow
- dashboard cache tools

### Initial Release

Included:

- professional editorial widget templates
- import / export workflows
- widget duplication
- dashboard administrator interface
- cache-first frontend rendering
- Joomla ACL permissions
- GitHub updater support

---

## Production Recommendations

Recommended defaults:

Frontend:

- enable widget caching
- keep Joomla caching enabled
- use one widget per editorial block

Infrastructure:

- Joomla Page Cache
- Cloudflare CDN
- PHP OPcache
- production image optimization

---

## Known Notes

- Always test template integration with your Joomla template and cache stack before production deployment

---

## Author

Kostas Stathopoulos  
DevArt  
https://devart.gr/

GitHub Repository:

https://github.com/devartgr/joomla-devart-widgets

---

## Disclaimer / Limitation of Liability

This software is provided "as is", without warranty of any kind.

DevArt shall not be liable for data loss, downtime, rendering issues, cache conflicts, production failures, or issues resulting from use or misuse.

Always test in staging before production deployment.

Maintain proper backups.

---

## License

GNU General Public License v3 or later
