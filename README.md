# DevArt Widgets for Joomla

Professional Joomla 6 widgets package for editorial, magazine, portal, business, events, video, and high-performance content websites.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-1.9.1-orange)
![License](https://img.shields.io/badge/License-GPLv3-red)

---

## Overview

DevArt Widgets is a modern Joomla 6 native widget builder designed for editorial websites, magazines, portals, newspapers, corporate websites, business directories, event websites, video portals, and high-traffic production environments.

Create professional frontend content blocks using multiple templates, multiple native content sources, Custom Lists, cache-first rendering, production-safe import/export tools, responsive typography controls, template-aware customization, and modern Joomla 6 architecture.

Version **1.9.0** added **Categories vs Specific items** selection, Slider-style lightweight pickers, and reusable **Custom Lists** that mix Joomla Articles, DevArt Business, DevArt Events, and DevArt Video. Legacy Manual/Mixed widgets normalise to Custom Lists. Existing category-based widgets keep working without re-save.

Version **1.9.1** uses Joomla native package updates only (`pkg_devartwidgets`, site client). Existing sites should install this package ZIP once. Later versions are found by Joomla Update.

Built specifically for Joomla 6 and PHP 8.3+ with strict typing, modern MVC architecture, and enterprise-oriented performance principles.

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
- video listings
- portal front pages
- responsive content blocks

---

## Multiple Content Sources

Each native source supports **Categories** or **Specific items**, with Slider-style ID search pickers for selected items.

### Joomla Articles

- Latest Articles
- Specific Articles
- Category Articles
- Featured Articles
- Related Articles
- Tag, author, and date filters

### DevArt Business

Display business directory content using all existing widget templates.

Business source supports:

- All Business Categories
- Selected Business Categories
- Specific businesses
- Include Child Categories
- Maximum Items

Business-specific administrator options are displayed automatically while article-only options are hidden.

### DevArt Events

Display event listings using the same widget templates.

Event source supports:

- Today
- Upcoming
- Past
- All
- Featured

Category and item options:

- All Event Categories
- Selected Event Categories
- Specific events
- Include Child Categories
- Maximum Items

Event ordering is handled automatically using the same event date logic as DevArt Events.

### DevArt Video

Display video content using the existing widget templates.

Video source supports:

- All Video Categories
- Selected Video Categories
- Specific videos
- Include Child Categories
- Featured Handling
  - Include Featured
  - Featured Only
  - Exclude Featured
- Ordering
  - Newest
  - Oldest
- Maximum Items

Video-specific administrator options are displayed automatically while unrelated article-only options are hidden.

### Custom Lists

Reusable lists that mix native sources in one widget.

Supported item types:

- Joomla Articles
- DevArt Business
- DevArt Events
- DevArt Video

Per-item display flags control title, intro, image, date, and category output.

Legacy Manual/Mixed widgets normalise to Custom until a list is selected.

Widgets can also be embedded in article content with `{devartwidget ID}`.

---

## Unified Multi-Source Rendering Engine

A single rendering engine powers every supported source.

Supported sources:

- Joomla Articles
- DevArt Business
- DevArt Events
- DevArt Video
- Custom Lists

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
- Custom Lists included in import/export
- preserve original IDs when possible (Super Users only)
- restore-friendly workflows
- production migration support

---

## Administrator Features

- Dashboard
- Widget Manager
- Custom Lists
- Create Widgets
- Duplicate Widgets
- Import / Export
- Template Overview
- Global Configuration
- Cache Tools
- Thumbnail Maintenance
- Cache Status
- Joomla ACL
- Content plugin shortcodes

---

## Production Safety

Features:

- Keep Data uninstall option
- rollback-friendly updates
- non-destructive upgrades
- additive Custom Lists tables
- existing widget rows are not rewritten
- safe restore workflows
- controlled cache handling
- administrator-only maintenance

---

## Included Extensions

- com_devartwidgets
- mod_devartwidget
- plg_content_devartwidgets

---

## Requirements

- Joomla 6.x
- PHP 8.3+

---

## Installation

1. Download the latest release.
2. Open:

   `System → Extensions → Install`

3. Upload the package ZIP.
4. Open:

   `Components → DevArt Widgets`

5. Create widgets.
6. Publish module instances or embed `{devartwidget ID}` in articles.

---

## Joomla Native Updates

Supports Joomla native updates through GitHub.

Updates are advertised for the package only:

- element: `pkg_devartwidgets`
- type: `package`
- client: `site`

Update server:

`https://raw.githubusercontent.com/devartgr/joomla-devart-widgets/main/update.xml`

The component, module, and content plugin do not register their own update servers.

Existing sites should install the `1.9.1` package ZIP once. Later versions are found by Joomla Update. If leftover DevArt Widgets update-site rows remain after install, use Rebuild Update Sites.

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
- video portals
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
- PHP 8.3+
- Joomla Native Updates
- Modern Joomla MVC Architecture

Not Supported:

- Joomla 3
- Joomla 4
- Joomla 5
- Legacy PHP versions

---

## Current Version

### 1.9.1

---

## Changelog Highlights

### v1.9.1

Changed:

- Joomla native updates now target `pkg_devartwidgets` with client `site`
- component, module, and content plugin no longer declare update servers

Notes:

- install this package ZIP on existing sites once
- later updates use Joomla native package updates
- Rebuild Update Sites if leftover DevArt Widgets update-site rows remain
- requires Joomla 6.0+ and PHP 8.3.0+

### v1.9.0

Added:

- Categories vs Specific items for Articles, Business, Events, and Video
- Slider-style lightweight pickers for specific items
- reusable Custom Lists mixing native sources
- Custom Lists administrator header, footer, and active submenu styling
- content plugin `{devartwidget ID}` for article embedding

Changed:

- Manual/Mixed widget sources replaced by Custom list selection
- language filters apply only when Joomla Language Filter / multilanguage is enabled
- Articles random ordering uses a bounded ID sample instead of SQL RAND()
- widget query cache stored under Joomla cache

Fixed:

- specific-item pickers open the selected source
- leftover specific items are cleared when the widget source changes
- Add selected adds items and closes the picker
- faster first Articles/Categories load on large sites
- Events first query hydrates intros only after time-filter and limit
- import preserve-IDs requires core.admin

Compatibility:

- existing category-based Articles, Business, Events, and Video widgets keep working without re-save
- existing widget rows are not rewritten
- Custom Lists tables are additive only
- frontend cache is purged after update
- requires Joomla 6.0+ and PHP 8.3.0+

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
- PHP 8.3 or newer

---

## Known Notes

- Always test updates on a staging environment before production deployment.
- Thumbnail maintenance runs only from the Joomla administrator.
- DevArt Business source requires DevArt Business when used.
- DevArt Events source requires DevArt Events when used.
- DevArt Video source requires DevArt Video when used.
- Legacy Manual/Mixed widgets normalise to Custom Lists until a list is selected.
- Existing sites should install the `1.9.1` package ZIP once before later Joomla native updates.

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
