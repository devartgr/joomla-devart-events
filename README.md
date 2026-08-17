# DevArt Events for Joomla

Professional event management for Joomla 6, designed for municipalities, cultural organizations, associations, conferences, educational institutions, publishers, businesses, and high-traffic event portals.

![Joomla](https://img.shields.io/badge/Joomla-6.x-blue)
![PHP](https://img.shields.io/badge/PHP-8.3%2B-green)
![Release](https://img.shields.io/badge/Version-1.0.11-orange)
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

An event that started before today is treated as past even if its optional end date is later. This start-based behavior is intentional in version 1.0.11.

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
- Configuration for maps, media, frontend layouts, SEO, and structured data

Event-level manual ordering is not displayed in the administrator event list. Frontend ordering is controlled by menu and module configuration and by the selected event-date source.

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
- Configurable map display
- Safe frontend map rendering

Leaflet assets are loaded with Subresource Integrity metadata.

## Calendar

Calendar functionality includes:

- Monthly event calendar
- Multiple events per date
- Localized month and weekday names
- Previous and next month navigation
- Event indicators and links
- Configurable module calendar range
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

The component and module use the same event-date engine for consistent results.

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
- Bounded calendar queries
- No fixed 1000-event ceiling for date-aware module sources
- Cache-friendly rendering
- Minimal frontend dependencies

The canonical event data remains stored with the event, while the indexed occurrence table is maintained as derived data for efficient queries.

## SEO and Structured Data

Built-in SEO support includes:

- Google Event JSON-LD
- Open Graph metadata
- Twitter Card metadata
- Canonical URLs
- Joomla metadata integration
- SEO-friendly alias routing
- Configurable event image and description output

Optional Schema.org properties such as performer, organizer, and offers are not required for an event to render.

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

Direct optimized uploads are processed when the event is saved.

## Multilingual Support

Version 1.0.11 includes:

- English (`en-GB`)
- Greek (`el-GR`)

Administrator, frontend, module, map, calendar, contact, share, and package-installation text uses Joomla language keys.

Additional Joomla language packs can translate the component and module without PHP or JavaScript overrides.

## Security

Security features include:

- Joomla ACL integration
- CSRF protection for administrator actions
- Namespaced Joomla 6 APIs
- Joomla Framework filesystem APIs
- Input validation
- Escaped administrator and frontend output
- Controlled map and iframe URL handling
- Subresource Integrity metadata for Leaflet assets
- Safe package and manifest validation
- No backward-compatibility plugin requirement

## Installation

1. Download the latest package ZIP.
2. Open **System → Install → Extensions** in Joomla.
3. Upload `pkg_devartevents_v1.0.11.zip`.
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

Version: `1.0.11`

Download:

```text
https://github.com/devartgr/joomla-devart-events/releases/download/v1.0.11/pkg_devartevents_v1.0.11.zip
```

SHA-256:

```text
bdb860762e91f38e12ca389af996003ba0ec84e3eb6d489a196b42c283f16d11
```

Release notes:

```text
https://github.com/devartgr/joomla-devart-events/releases/tag/v1.0.11
```

## Verification

Version 1.0.11 passed:

- PHP syntax validation
- JavaScript syntax validation
- XML validation
- Manifest validation
- Manifest reference validation
- Version-consistency validation
- Language-file syntax and key-parity validation
- Source-integrity validation
- ZIP archive-integrity validation
- SHA-256 verification
- Installation and functional testing on Joomla 6.1.2

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

The build process:

- Reads the package manifest
- Validates PHP, XML, manifests, references, versions, and language files
- Creates the declared component and module archives
- Creates the outer Joomla package
- Verifies source integrity
- Generates a SHA-256 checksum
- Refuses to overwrite an existing release build

## License

DevArt Events is distributed under the GNU General Public License version 2 or later.

See `LICENSE.txt` for the complete license text.

## Author

Kostas Stathopoulos — DevArt

Website: [https://devart.gr](https://devart.gr)

GitHub: [https://github.com/devartgr/joomla-devart-events](https://github.com/devartgr/joomla-devart-events)
