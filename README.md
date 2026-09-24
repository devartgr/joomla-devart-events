# DevArt Events for Joomla

Professional event management for Joomla 6, designed for municipalities, cultural organizations, associations, conferences, educational institutions, publishers, businesses, and high-traffic event portals.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-1.1.2-orange)
![License](https://img.shields.io/badge/License-GPL--2.0--or--later-red)

## Overview

DevArt Events is a native Joomla 6 package for creating, managing, and publishing professional event directories.

It supports events with multiple dates, categories, tags, saved or manual venues, maps, calendars, media, frontend filtering, structured data, and multilingual interfaces.

The package is built for modern Joomla websites with an emphasis on stability, security, scalability, clean routing, and lightweight frontend rendering.

## Included Extensions

The package installs:

- `com_devartevents` — administrator and frontend event component
- `mod_devartevents` — configurable frontend event module

No plugins are installed by the package.

## Requirements

- Joomla 6.0 or newer
- PHP 8.3 or newer
- Modern MariaDB or MySQL
- PHP ZIP and SimpleXML extensions for package installation and repository tooling

Joomla 3, Joomla 4, Joomla 5, and PHP 8.2 or older are not supported.

## Event Management

Create and manage events with:

- Multiple independent event dates
- Start and optional end date
- All-day events
- Scheduled, cancelled, postponed, and sold-out date statuses
- Featured events
- Categories and tags
- Saved or manually entered venues
- Main image and gallery support
- Image upload and optimization
- Introductory and full event descriptions
- Contact details
- Website and social links
- Video and map information
- Joomla publishing state, access, and language controls

## Event Date Sources

Built-in event sources include:

- Upcoming Events
- Today Events
- Past Events
- All Events
- Featured Events
- Selected Categories
- Selected Tags
- Calendar

Frontend ordering is based on event dates rather than event creation or publishing dates.

### Date Semantics

Today, Upcoming, and Past classification is based on event start dates.

When an event contains multiple dates, it is included when any matching occurrence satisfies the selected source or date range.

An event that started before today is treated as past even if its optional end date is later. This start-based behavior is intentional.

## Administrator

The Joomla administrator interface provides:

- Event management
- Category management
- Tag management
- Venue management
- Published, unpublished, archived, and trashed filtering
- Featured and unfeatured filtering
- All, Today, Upcoming, and Past event filtering
- Category filtering
- Search and sortable event lists
- Import, export, backup, and maintenance tools
- Dashboard hub with Options and Modules shortcuts
- Configuration for maps, media, frontend layouts, SEO, and structured data

## Categories and Tags

Organize events with:

- Nested categories
- Primary and additional event categories
- Tags
- Category listing pages
- Category and tag event views
- Optional category images and icons
- Event counts
- Joomla access and language filtering

## Venue Management

Events can use saved venues or manually entered locations.

Venue information can include:

- Venue name
- Address
- City
- Region or state
- Country
- Postal code
- Latitude and longitude
- Contact information
- Website
- Map coordinates

## Maps

Supported map providers include:

- OpenStreetMap
- Google Maps

Available map functionality includes:

- Address search
- Coordinate lookup
- Interactive marker selection
- Draggable map markers
- Event list maps
- Module maps
- Configurable map display and map event limit
- Locally vendored Leaflet assets
- OpenStreetMap attribution on map controls

## Calendar

Calendar functionality includes:

- Monthly event calendar
- Multiple events per date
- Localized month and weekday names
- Previous and next month navigation
- Event indicators and links
- Configurable module calendar range
- Site-timezone-aware month bounds and titles
- Responsive frontend rendering

## Frontend Event Listings

Frontend listings support:

- Search
- Category filtering
- Tag filtering
- Venue filtering
- Featured filtering
- Date range filtering
- Configurable results per page
- Top or sidebar filter layouts
- Cards, compact, directory, and overlay layouts
- Responsive desktop, tablet, and mobile columns
- Optional event images, intro text, location, contact information, tags, and featured badges
- Clean Joomla alias routing
- Canonical URLs based on Joomla `live_site`

## Frontend Module

The DevArt Events module can display:

- Upcoming events
- Today events
- Past events
- All events
- Featured events
- Events from selected categories
- Events from selected tags
- A single event
- Selected events
- Category listings
- Event maps
- Event calendars

Module single-event and selected-events fields use a searchable modal picker. Category, tag and map filters use Joomla list-fancy-select.

The component and module use the same event-date engine and RouteHelper-based links for consistent results.

## Performance

DevArt Events is designed for large Joomla websites.

Performance features include:

- Indexed event occurrence table
- Database-level date filtering
- Database-level ordering
- Native Joomla pagination
- Database-level totals
- Batched indexing of existing and imported event dates
- Automatic date-index synchronization after event changes
- Bounded calendar and map queries
- Cache-friendly rendering
- Minimal frontend dependencies

## SEO and Structured Data

Built-in SEO support includes:

- Google Event JSON-LD
- Open Graph metadata
- Twitter Card metadata
- Canonical URLs
- Joomla metadata integration
- SEO-friendly alias routing
- Configurable event image and description output

## Import and Export

Data-management tools include:

- Event CSV import and export
- Category CSV import and export
- JSON backup and restore
- Venue and relationship preservation
- Rebuilding of derived event-date indexes
- Category-tree maintenance
- Diagnostic tools

Always create a backup before importing or restoring data.

## Media

Event media functionality includes:

- Selection through Joomla Media Manager
- Direct upload and optimization
- Automatic processed-image storage
- Configurable image dimensions and quality
- Main image and gallery support
- Existing Media Manager images remain unmodified

## Multilingual Support

Version 1.1.2 includes:

- English (`en-GB`)
- Greek (`el-GR`)
- French (`fr-FR`)
- German (`de-DE`)
- Spanish (`es-ES`)
- Italian (`it-IT`)
- Portuguese Brazil (`pt-BR`)
- Czech (`cs-CZ`)
- Dutch (`nl-NL`)
- Polish (`pl-PL`)
- Russian (`ru-RU`)
- Ukrainian (`uk-UA`)
- Japanese (`ja-JP`)
- Turkish (`tr-TR`)
- Chinese Simplified (`zh-CN`)

Administrator, frontend, module, map, calendar, contact, share, and package-installation text uses Joomla language keys.

## Security

Security features include:

- Joomla ACL integration
- CSRF protection for administrator actions
- Namespaced Joomla 6 APIs
- Joomla Framework filesystem APIs
- Input validation
- Escaped administrator and frontend output
- Hardened HTML/URL sanitization
- Controlled map and iframe URL handling
- Absolute URLs prefer configured `live_site`
- Safe package and manifest validation
- No backward-compatibility plugin requirement

## Installation

1. Download the latest package ZIP.
2. Open **System → Install → Extensions** in Joomla.
3. Upload `pkg_devartevents_v1.1.2.zip`.
4. Confirm that both the component and module were installed.
5. Open **Components → DevArt Events** and review the configuration.
6. Create or import events and configure the required Joomla menu items or modules.

For updates, install the new package over the existing version or use Joomla Update when the release is available through the update server.

Always test updates on a staging website before production deployment.

## Joomla Native Updates

The package supports Joomla native updates through:

```text
https://raw.githubusercontent.com/devartgr/joomla-devart-events/main/update.xml
```

Updates are applied to the complete `pkg_devartevents` package so the component and module remain on the same version.

## Current Release

Version: `1.1.2`

Download:

```text
https://github.com/devartgr/joomla-devart-events/releases/download/v1.1.2/pkg_devartevents_v1.1.2.zip
```

SHA-256:

```text
84a8c12834ebf8f35f592bacb5e1cfa4bde60ebd81d8e6cfb5269e0201be3d0c
```

Release notes:

```text
https://github.com/devartgr/joomla-devart-events/releases/tag/v1.1.2
```

## Verification

Version 1.1.2 passed:

- PHP syntax validation
- XML validation
- Manifest validation
- Manifest reference validation
- Version-consistency validation
- Language-file syntax and key-parity validation
- Source-integrity validation
- ZIP archive-integrity validation
- SHA-256 verification
- Local Herd installation smoke QA on Joomla 6

Repository validation does not replace testing on the target Joomla installation.

## Development

The `source/` directory is the only development source.

Generated packages belong under `builds/` and must not be edited directly.

Validate the repository with:

```shell
php scripts/validate.php
```

Build a new non-overwriting package with:

```shell
php scripts/build.php
```

## License

DevArt Events is distributed under the GNU General Public License version 2 or later.

See `LICENSE.txt` for the complete license text.

## Author

Kostas Stathopoulos — DevArt

Website: [https://devart.gr](https://devart.gr)

GitHub: [https://github.com/devartgr/joomla-devart-events](https://github.com/devartgr/joomla-devart-events)
