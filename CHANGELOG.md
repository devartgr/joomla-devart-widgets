# Changelog

## 2.0.2 - 2026-11-06

Remove orphan **DevArt Sources Updates** site (private `update.xml` URL caused Joomla “Could not open update site”). Pin Sources companion **1.0.2** (no public updateservers; companion-only). Requires Joomla 6.0+ and PHP 8.3.0+. No database schema changes.

- Fix: installer deletes stale Sources update-site rows on install/update
- Fix: bundled `pkg_devartsources` **1.0.2** (never-downgrade when older)

## 2.0.1 - 2026-10-31

M7 plugin-only cut for shared sources. Removes in-product Articles/Business/Events/Video legacy fetch paths, shadow compare, Options `source_engine` field, and legacy fallback. Installer forces `source_engine=plugin`. Shared sources fail closed (empty) when Sources is unavailable. Custom Lists resolve nested shared rows via `SourceEngine`. Host-local `custom` / `custom_items` stay in-product.

Also in this release:

- Re-pin Sources companion to **1.0.1** (same SHA as Slider 2.0.2)
- Clear `.webp` (and `.jpeg`) thumbs in retention / Clear thumbnails; Dashboard counts them
- Green `VisibilityRulesTest` for empty-string publish windows; remove dead `admin/script.php`
- Memoize video table columns on warm recheck; CustomList cache key omits template/theme
- Document article warm-recheck category/tag bounded staleness; Events host path already applies `publish_down`
- Admin list Status column uses jgrid published icons (Widgets / Custom Lists / Items)
- Frontend Play/Pause video `aria-label` from site language (`data-dw-video-playpause-label`)
- `AuditTimestampsTrait` uses `getDatabase()`; PHPStan scan path updated to Joomla 6.2.0 workspace

No official update-server downgrade; keep the **2.0.0** ZIP on GitHub Releases for manual rollback only.

## 2.0.0 - 2026-10-01

- Soft cutover: Options default `source_engine=plugin`; installer activates plugin only when missing/invalid (preserves explicit legacy/shadow/plugin).
- Build-time embed of pinned `pkg_devartsources` **1.0.0** (same SHA as Slider 2.0.0 triad pin); package installer installs/upgrades Sources when missing/older (never downgrades; not a package child).
- Neutral filter mapping for Sources providers (`categoryIds`, `categoryMode`, `selectedIds`, `timeFilter`, …).
- Plugin cache TTL = min(operator `cache_minutes`, provider hint); storeMode parity with legacy; display fields in cache key; FallbackStats request dedupe.
- SafeLog class-only; unknown `source_type` → `EmptySource`; Events over-fetch cap 1000; Dashboard SourceRegistry conflicts + diagnostics.
- Host `CachedSource` for plugin providers; installer preserves explicit `source_engine` on update; exclude package `update.xml` from ZIP (circular SHA).
- Legacy retained as fallback until M7 (post-soak plugin-only cleanup; manual ZIP rollback safety net — see `docs/source-engine.md`).

## 2.0.0 development line notes (pre-RC)

- Companion `pkg_devartsources` **1.0.0**: query failures → `SourceResult::fail`; install-only plugin enable; `SourceContext::$timezone`.
- Fix `ItemRouteHydrator` dynamic RouteHelper calls (PHP treated `Class::{$method}` as a class constant → broken Events/Video/Business URLs).
- M4-2B: component Options expose `source_engine` (legacy / shadow / plugin).
- PluginSourceAdapter maps Events / Business / Video for shared `pkg_devartsources`.
- PluginSourceAdapter maps Business (`devartbusiness`) filters, ordering, and random overfetch for shared `pkg_devartsources` Business provider.
- PluginSourceAdapter maps Video (`devartvideo`) filters and ordering for shared `pkg_devartsources` Video provider; Articles-only exclude_current remains host-owned.
- Thumbnail cache prefers WebP when GD supports `imagewebp`, with JPEG fallback; non-blocking per-thumb lock avoids concurrent encode stampede (News-aligned). Events payload stampede remains covered by `WidgetCache::remember` via CachedSource.
- Consolidate shared content-display flags into `RenderOptions`; inject `RendererRegistry` through administrator DI into `WidgetRepository`.
- Register shared `WidgetRepository` and `WidgetCache` in the administrator DI provider; module, content plugin, and site WidgetModel resolve via `bootComponent` getters (News-aligned).
- Introduce `VisibilityRules` shared publish-up/down SQL for cold queries and warm `CachedItemVisibility` rechecks; Articles warm path uses the shared filter.
- Migrate Article onto CachedSource (Always store; page-independent overfetch when exclude_current; visibility recheck on warm hits).
- Migrate CustomList onto CachedSource (SkipEmpty; always finalise published/visibility/exclude_current/limit after load).
- Events: stop filtering `publish_down` on cold/fallback/cached visibility so `past`/`all` match com_devartevents lists (time filters use the date index / dates_json).
- Load `com_devartwidgets` site language from module/plugin render so empty-state strings resolve instead of raw keys.
- Migrate Events onto CachedSource with EmptyShortTtl + day-sensitive policy; extract EventsCacheRules for unit-tested empty/day rules.
- Introduce CachedSource decorator + SourceCachePolicy; migrate Video and Business sources onto CacheableSourceInterface (Article/Events/CustomList unchanged).
- Finish remaining small quality items: Items form URL field accepts SafeHrefUrl-compatible values; module/plugin outer catch uses SafeLog; WidgetCache `remember()` single-flight fill (News-aligned) wired into all cached sources.
- Preserve widget `custom_list_id` when the assigned Custom List is unpublished; clear widget refs when a list is deleted; zero orphan ids on save when the list row is missing.
- Custom Items media paths share `SafeLocalMediaPath` on admin save and frontend render (local `images/` only; blocks remote/`//`/`data:`/`..`/bad extensions); remove unused WidgetModel cleanLocal* duplicates.
- Header/footer link admin fields accept the same SafeHrefUrl-compatible relative/hash/query values as Custom Items (text + string filter; server still validates).
- Custom Items frontend links use the shared `SafeHrefUrl` allowlist so relative/hash/query links saved in admin still render.
- Saving as Custom Items with an empty (omitted) subform persists `custom_items: []` instead of restoring previous rows from merge-from-existing.
- Admin template visibility hides overlay/image fields without disabling them, so values edited before a template switch still POST; widgets and custom lists show a Modified column.
- Admin audit timestamps (`created`/`modified`/`*_by`) on widget, custom list, and item store; restore edit form userState after validation failure; empty multi-select POST sentinel so clearing categories/tags/selected ids actually persists.
- Joomla Cache API for widgets uses shared `cachebase` (`JPATH_ROOT/cache`) and pending generation flush is News-aligned (`onlyIfPending` + non-blocking lock).
- Widget cache directory is shared under `JPATH_ROOT/cache/com_devartwidgets` so admin Save invalidates the same generation the frontend reads (avoids stale FE payloads when `JPATH_CACHE` differs per app).
- Events: honour `publish_up` on cold/fallback/cached visibility (not `publish_down` — past/all use the date index); prefer indexed `#__devartevents_event_dates` (via `EventDateIndexHelper`) before LIMIT when available.
- Cache generation reconciles backend vs sidecar and keeps the highest monotonic generation.
- Business/Video cached visibility matches cold LEFT JOIN semantics for inaccessible primary categories.
- Runtime `WidgetConfig::getArray()` caps/dedupes IDs at 200; import enforces export-symmetric count and per-list caps.
- Module dispatcher wraps `bootComponent` + render in try/catch; repository render logs are throttled.
- Access levels use `AccessLevels` / `whereIn` (no hand-built `implode` IN lists); installer warns when required tables are missing.
- Thumbnail publish never deletes an existing target after a failed rename; CI adds PHP 8.5 and a real PHPStan gate (downloads Joomla CMS).
- Cached visibility accepts WidgetConfig and rechecks selected categories / featured on warm hits; shared `SafeHrefUrl` policy used by `safeUrl` / `anchorAttrs` / admin URL helper.
- Throttled `SafeLog` for fail-closed paths (cache, render, Events fallback, route hydrate); `ItemRouteHydrator` uses a provider table; WidgetCache encode/decode FORMAT_VERSION unit tests.
- Events: treat `past` as day-sensitive TTL; cache empty results with a short TTL (≤60s) to avoid repeat heavy scans.
- Cap/dedupe selected and category ID arrays (200); shared `DuplicateAliasDetector` for widget/list save retries.
- Export preflight count caps (widgets/lists/items) before loading full payloads; AliasUniquenessMigrator logs failures, truncates for suffix, verifies unique indexes.
- Add PHPUnit for pure classes (`IdListOrder`, `WidgetShortcode`, URL/payload helpers, `CacheTtl`) and GitHub Actions CI (`php -l`, validate, PHPUnit).
- Cached visibility rechecks primary category state/access/language for Business, Events, and Video; request-scoped ID/list memo across widgets.
- Move shared `renderHeader` / `renderFooter` / `safeAlign` / `formatFloat` into `BaseWidgetRenderer`.
- Persist thumbnail failure markers (`.fail`, 24h TTL) beside cache targets; collapse Business/Video category child expansion to one query.
- Harden pre-release: `WidgetRepository::render()` catches Throwable with logging; module/plugin/component share the same fail-closed boundary.
- Content plugin namespace moved to `DevArt\Plugin\Content\Devartwidgets`; request-wide shortcode cap (30) plus per-article (10).
- Cached visibility rechecks Video `publish_up`/`publish_down` and Events `publish_up`; IntegrationAvailability refreshes stale-negative table lists and purges on package install/update.
- Import uses `WidgetSettingsNormalizer`; preserve-ID alias collisions get unique suffixes; export fails closed on list query errors; import rollback preserves the original exception.
- WidgetCache treats `store() === false` as failure and falls back to the file sidecar; reject protocol-relative `//` URLs in `safeUrl` / admin URL helper.
- Sync `joomla.asset.json` and `docs/current-state.md` to 2.0.0 / 15 languages.
- Add local PHPStan tooling (Composer + `phpstan.neon` level 5 + baseline), matching DevArt News.
- Pass optional `DatabaseInterface` through `SourceFactory` into source constructors; `WidgetRepository` and `CustomListSource` reuse the shared DB.
- `ArticleSource` shares its DB with `ArticleQueryBuilder`.
- Move dashboard stats/card preparation from `tmpl/dashboard/default.php` into `Dashboard\HtmlView` (layout stays presentation-only).
-
## 1.9.9 - 2026-09-29

Last published production release (`releases/pkg_devartwidgets_v1.9.9.zip`).
Full shipped item list: `source/package/changelog.xml` (version 1.9.9) and GitHub release notes for `v1.9.9`.
