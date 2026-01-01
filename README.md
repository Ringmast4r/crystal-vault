# Crystal Vault

![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fringmast4r%2Fcrystal-vault&count_bg=%23CF142B&title_bg=%23555555&icon=&emoji=&title=VISITORS&edge_flat=false)
![GitHub repo size](https://img.shields.io/github/repo-size/ringmast4r/crystal-vault)
![GitHub last commit](https://img.shields.io/github/last-commit/ringmast4r/crystal-vault)
![GitHub Pages](https://img.shields.io/website?url=https%3A%2F%2Fringmast4r.github.io%2Fcrystal-vault%2F&label=GitHub%20Pages)
![License](https://img.shields.io/github/license/ringmast4r/crystal-vault)
![Stars](https://img.shields.io/github/stars/ringmast4r/crystal-vault)
![Forks](https://img.shields.io/github/forks/ringmast4r/crystal-vault)

![Wanted Poster](assets/Wanted%20Poster.PNG)

Venezuela OSINT Intelligence Dashboard documenting the regime's centralized surveillance infrastructure and exposed government systems.

**Live Dashboard:** [https://ringmast4r.github.io/crystal-vault/](https://ringmast4r.github.io/crystal-vault/)

---

## Overview

Crystal Vault documents Venezuela's centralized surveillance database announced in December 2024. The system, built by Chinese company ZTE, merges citizen identity records, banking data, and social program participation for over 30 million Venezuelans.

The regime exposed their infrastructure through unsecured WordPress REST APIs. Approximately **4.34 GB** of data was retrieved without authentication, including government office locations, staff GPS coordinates, and operational statistics.

---

## Key Statistics

| Metric | Count |
|--------|-------|
| Total Data Exfiltrated | 4.34 GB |
| Media Files | 9,716 |
| Images with EXIF Metadata | 13,209 |
| Staff Phone GPS Locations | 345 |
| OFAC Sanctioned Individuals | 210 |
| Cracked Gravatar Emails | 35 |
| CNE Intranet Routes Exposed | 78 |
| Personnel Records | 1,550 |

---

## Intelligence Modules

### Main Dashboard (`index.html`)
- Overview with key statistics
- Interactive map with 479 locations (134 SAIME offices + 345 GPS coordinates)
- Media gallery with 9,716 files across government agencies
- EXIF metadata analysis
- GPS Intel tab with phone model and datetime extraction
- Cracked Gravatar hashes (35 emails recovered)
- OFAC sanctions cross-reference
- Personnel database

### Hezbollah Intel (`hezbollah_intel.html`)
- Iranian/Hezbollah presence in Venezuela
- Network analysis and connections

### Margarita Intel (`margarita_intel.html`)
- Margarita Island specific intelligence
- Tourism and government overlap analysis

### Timeline (`timeline.html`)
- Chronological events and data points

### GPS Section (`gps_section.html`)
- Detailed GPS coordinate analysis
- Phone metadata extraction

### Glossary (`glossary.html`)
- Venezuelan government terminology
- Agency abbreviations and explanations

---

## Data Sources

| Agency | Description | Files |
|--------|-------------|-------|
| SAIME | Immigration & ID Services | 134 office locations |
| INCES | Worker Training Institute | Media files |
| AVN | State News Agency | Media files |
| SAREN | Notary Registry | Media files |
| VTV | State Television | Media files |
| CANTV | State Telecom | Media files |
| Sistema Patria | Social Control System | App ecosystem data |

---

## Repository Structure

```
crystal-vault/
├── index.html              # Main dashboard
├── gps_section.html        # GPS analysis
├── hezbollah_intel.html    # Hezbollah intelligence
├── margarita_intel.html    # Margarita Island intel
├── timeline.html           # Event timeline
├── glossary.html           # Terminology guide
├── OFAC_Sanctions/         # US Treasury sanctions data
├── OpenData/               # Government open data
├── assets/                 # CSS, JS, images
├── docs/                   # Documentation
└── exfil/                  # Exfiltrated data samples
```

---

## Technical Details

### Exposed Endpoints
- WordPress REST API: `/wp-json/wp/v2/users`
- Media endpoints: `/wp-json/wp/v2/media`
- Geographic data: `/wp-json/` various routes
- CNE Intranet: 78 exposed internal routes

### EXIF Analysis
- 13,209 images processed for metadata
- 345 contained GPS coordinates from staff phones
- Phone models identified: Samsung, iPhone, Huawei, Xiaomi
- Timestamps extracted for operational patterns

### Gravatar Hash Cracking
- 35 email addresses recovered from MD5/SHA256 hashes
- Cross-referenced with WordPress user enumeration
- Key accounts: government webmasters, officials

---

## Purpose

This research serves:
- Journalists investigating Venezuelan government operations
- Researchers studying authoritarian surveillance systems
- The 7+ million Venezuelan refugees whose personal data remains in government databases
- Human rights organizations documenting abuses

All data comes from publicly accessible APIs and US government records (OFAC).

---

## Disclaimer

This repository documents publicly exposed government infrastructure for research and journalism purposes. No systems were compromised - all data was accessible without authentication through misconfigured public APIs.

---

## License

MIT License - See LICENSE file for details.
