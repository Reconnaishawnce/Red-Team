# OPRT: OSINT for Physical Red Teaming

**Objective:** Identify information that lets you reach secured assets the way an adversary would — *before* setting foot on target.

A passive-first reconnaissance checklist for physical red team operations. Work top to bottom, or jump to the section you need. Everything here is **information gathering**: collect, correlate, and build a picture of the target. Bypass and on-site tradecraft live in other files.

---

## !! Read First — Authorization & Scope

Physical red teaming is legal only when it's authorized in writing and bounded by an agreed scope. Before any of the below:

- **Signed authorization** ("get-out-of-jail" letter) naming the assessing org, the client signatory with authority over the property, target addresses, dates/windows, and permitted activities. Carry a copy on site.
- **Written scope / Rules of Engagement (ROE):** in-scope buildings and floors, out-of-scope tenants/neighbors, permitted techniques (tailgating, pretext, badge testing, etc.), hard "do not touch" list, and the kill/abort criteria.
- **Third-party boundaries:** shared buildings, neighboring tenants, public sidewalks, and other companies' assets are out of scope unless explicitly named. OSINT can sweep them up by accident — segregate and discard.
- **Data handling:** PII, employee details, and badge photos collected during recon are sensitive. Store encrypted, share only with the engagement team, and destroy per the contract.
- **Emergency contact** on the client side reachable during the live phase.

> If it isn't in the authorization letter and ROE, it isn't in scope.

---

## Operator OPSEC

Recon can tip off a target as easily as the live op can.

- **Sock-puppet accounts** for LinkedIn, social, and people-search sites — never your real identity. Age them; don't create-and-immediately-stalk.
- **Egress hygiene:** VPN/residential proxy for sensitive lookups. Some people-search and ad-library sites log and notify.
- **Stay passive online.** Browsing public listings, maps, and social media is passive. Do **not** log into, scan, port-probe, or otherwise touch the target's live infrastructure during the OSINT phase — that's active and usually out of the OSINT scope.
- **Don't poison the well.** Friending employees, joining their Slack/Discord, or RSVPing to their events under a sock puppet can burn a pretext you'll want later. Decide deliberately.
- **EXIF your own captures.** Strip metadata from screenshots/photos before they leave your machine.

---

## Top 5 Starting Points

1. **Google Dork for document leakage**
   `site:example.com filetype:pdf` (also `docx`, `xlsx`, `pptx`)
2. **Google Earth & Street View** — including the historical-imagery timeline (Earth Pro)
3. **Building blueprints / layout**
   - Landlord & broker sites (LoopNet, CoStar)
   - City planning & permit documents
4. **LinkedIn** — employees, badge photos, org structure
5. **Job listings (current + archived)** — systems, processes, and social-engineering hooks

---

## Favorite Links & Tools

| Tool | Use |
|---|---|
| [IntelTechniques](https://inteltechniques.com/tools/Address.html) | OSINT tool collection (address, person, company) |
| [OSINT Framework](https://osintframework.com/) | Categorized index of OSINT resources |
| [Hunter.io](https://hunter.io) | Email pattern / address discovery |
| [WiGLE.net](https://wigle.net) | Wardriving / SSID + BSSID + BLE mapping |
| [Shodan](https://shodan.io) | Internet-exposed devices, cameras, controllers |
| [SunCalc](https://www.suncalc.org) | Sun position / shadow & lighting timing |
| Maltego / SpiderFoot / recon-ng | Link analysis and OSINT automation |
| theHarvester | Email, subdomain, and name enumeration |
| ExifTool | Metadata extraction from leaked docs/photos |
| [OpenCorporates](https://opencorporates.com) | Corporate registration & ownership |

---

## 1. Facility Reconnaissance (Physical & Perimeter)

### Building Addresses & Locations
- Google Maps (Street View, Satellite, Earth 3D)
- **Historical imagery** (Google Earth Pro timeline) — watch fencing, lot usage, construction, and where vehicles actually park change over time
- Bing Maps (Bird's Eye / oblique angles)
- Apple Maps (Sometimes has more recent streetview images)
- **NearMap / oblique aerial providers** — higher-res, multi-angle rooftops and yards
- OpenStreetMap (often tags entrances, parking, barriers)
- LinkedIn for building names & architect/designer portfolios
  - *e.g.* `site:linkedin.com "123 Main Street" design OR architect`

### Interior Layout via Listings & Tours *(new)*
Real estate marketing leaks interiors more than any blueprint.
- **Commercial/residential listings** (LoopNet, CoStar, Zillow, Redfin) — floor plates, finishes, server/utility rooms
- **Matterport / 360° virtual tours** — walk the lobby, spot turnstiles, reception layout, badge readers, and after-hours door positions
- **Listing video & drone footage** on YouTube/Vimeo and broker sites
- **Google indoor maps / "see inside"** for malls, lobbies, and large tenants
- Internet Archive — pull *older* listings the landlord later took down

### Access Points & Security Features
- Parking lots & garages (employee vs. visitor)
- Entrances/exits: main, side, loading dock, emergency
- Fencing, gates, turnstiles, bollards, mantraps
- Guard shacks, sensors, lighting, cameras

### Building Infrastructure
- HVAC (rooftop access)
- Utility & telecom rooms / MPOE
- Roof access points (fire escapes, ladders, hatches)
- External staircases and catwalks

### Business Directory & Listings
- Google Business Profile
- Yelp / TripAdvisor (interior photos in reviews)
- LoopNet / CoStar
- Tax records → building owner; pivot to owner's site for PDFs
- Internet Archive for older listings & site versions

### Proximity Risks & Enablers
- Nearby police stations, government offices, politician offices
- Embassies, consulates, intelligence/federal facilities
- Shooting ranges, jails, prisons
- Encampments, tents, temporary housing
- Crime maps and recent local police reports
- **Scanner feeds** ([Broadcastify](https://www.broadcastify.com)) — PD/security response cadence near the site

### Blueprints & Technical Documents
- ID the building **owner** → search their site: `site:owner-domain.com filetype:pdf`
- ID the **property management** company → same treatment
- Municipal records: construction permits, **certificate of occupancy**, city/zoning filings, **fire marshal** records
- **Procurement / bid documents & RFPs** *(new)* — public-sector and large-tenant bids frequently specify the exact access-control, camera, and alarm systems being installed

---

## 2. Employee & Organizational Intelligence

### Employee Name Harvesting
- LinkedIn (Company → "People")
- ZoomInfo / RocketReach / SignalHire
  - When signing up, do **not** grant email access or install their plugins — that's how they scrape your contacts.
- Staff bios on the company site
- **theHarvester / SpiderFoot** to automate and de-duplicate name + email collection

### Email Patterns
- Hunter.io and other format finders
- Confirm format from any single leaked address, then extrapolate
- `@company.com site:linkedin.com`
- *Caveat:* breach-data sites can confirm an email **format**, but treat the data as untrusted and stay within scope — don't reuse leaked credentials.

### Contact Info
- TruePeopleSearch / WhoCalledMe / TrueCaller (US)
- FOIA requests (public-sector targets)
- Company press releases with named contacts

### Org Chart & Reporting Lines *(new)*
- Reconstruct who reports to whom from LinkedIn titles/connections — pretexts land better when you reference a real manager or team
- Identify facilities, security, IT, and reception staff specifically
- Note recent hires (least familiar with who "belongs") and recent depart*ures* (names still trusted, badges maybe not yet revoked)

### Hiring & Job Posts
- LinkedIn, Indeed, Glassdoor, ZipRecruiter
- Flag references to badge access, security policies, vendor onboarding, visitor procedures

### Vendors & 3rd Parties
- Cleaning / maintenance / landscaping (Yelp, job postings, signage in Street View)
- IT and security-integrator vendors (non-`@company` email domains in posts and on LinkedIn)
- Shred/records vendors (Iron Mountain, Shred-it) — reveal document-handling cadence

### Corporate & Procurement Records *(new)*
- **OpenCorporates** / Secretary of State business filings — registered agent, officers, related entities
- **SAM.gov / USAspending.gov** — federal contracts and vendors (gov targets)
- **SEC EDGAR** 10-K / 8-K (public companies) — facilities, subsidiaries, risk language
- **UCC filings** — financed equipment sometimes names security/IT systems
- D&B / business credit profiles for structure and locations

### Ad & Technical Intel
- [Facebook / Instagram Ad Library](https://www.facebook.com/ads/library) — hiring pushes, event promos, brand imagery (uniforms, interiors)

---

## 3. Badge, Uniform & Pretext Recon

### Badge Photos
- LinkedIn profile pictures, "first day" posts, social media
- Conference slides and press kits (lanyards/badges in frame)

### Uniform & Dress Code
- Website staff photos
- Job listings mentioning "company-issued uniforms"
- Instagram, TikTok, X

### Courier & Vendor Pretexts
- FedEx, USPS, UPS, DHL, and named vendor logos/access points
- `"vendor name" site:company.com` in Google Images

### Pretext / Cover Development *(new)*
- Anchor every pretext to verifiable OSINT (real vendor names, real manager, current project, real internal lingo) so a casual challenge doesn't break it
- Map which pretexts fit which entrances/shifts (delivery → dock; "IT contractor" → after hours; "new hire" → morning rush)
- Pre-stage props consistent with the cover (work order #, vendor email signature, business card) — all fictional, never impersonating a real named individual without authorization
- Identify a plausible **callback/verification path** the target might use, and decide how your pretext survives it

---

## 4. Social Engineering Attack Surface

### Employee Habits & Check-ins
- Instagram / Facebook location tags
- X searches like "working at [Company]"
- [Strava Global Heatmap](https://www.strava.com/maps/global-heatmap), Fitbit, MapMyRun
  - *Most useful for rural/campus sites: surfaces running & biking routes near a facility, traffic patterns and exercise hotspots (loiter/surveillance cover), where people park, where fences are (a line the paths won't cross), and sometimes guard patrol routes along the perimeter.*

### Company Lingo & Internal Culture
- LinkedIn posts, Glassdoor reviews
- Industry Slack/Discord chatter (acronyms, team names, tooling)

### Events & Conferences
- EventBrite / Meetup RSVPs
- Company blog & speaker announcements
- Industry summits & attendee lists

### IT & Help Desk Clues
- Glassdoor reviews mentioning IT policy
- Help Desk / SOC job posts (MFA, password-reset, badge-reset workflows)

### Executive & VIP Profiles
- `"CEO name" filetype:pdf` (annual reports, decks)
- People-search tools: Pipl, FamilyTreeNow, OpenCorporates
- FOIA filings (public-sector execs)
- Public 10-Ks on investor pages
- Interviews — at-home (work-from-home reveals) or in-office (close-up interior/badge detail)

### Patterns of Life & Metadata *(new)*
- **EXIF on published photos** (ExifTool) — geolocation, capture device, sometimes interior detail
- **Document metadata** on leaked PDFs/Office files — usernames, software versions, internal file paths, printer names
- **Reverse image search** (Google Lens, Yandex, TinEye) to find where a badge/lobby photo originally appeared
- Posting cadence → infer work schedule, travel, and on-site vs. remote days

---

## 5. Building & Access Control Intelligence

> This section is about **identifying** what's deployed so the team can plan and scope. Defeating these controls is on-site tradecraft governed by the ROE, not OSINT.

### Wi-Fi Networks
- WiGLE.net (SSID/BSSID, sometimes BLE)
- War-driving on site (WiFi Pineapple, Kismet) — within scope only
- Conference/guest credentials leaked on Reddit, X, event pages

### RF / Wireless / BLE / Sub-GHz *(expanded)*
- **WiGLE** to pre-map SSIDs **and** BSSIDs around the perimeter before arriving
- **BLE landscape:** building automation, beacons, and some badge readers advertise over Bluetooth LE — useful for fingerprinting what's present (passive survey)
- **Sub-GHz / ISM (315/433/868/915 MHz):** gate remotes, wireless door/window sensors, and intercoms commonly live here — note their presence to scope whether RF is relevant
- Tools: Kismet, Airodump-ng (passive survey), SDR for spectrum awareness, Flipper Zero for ISM/BLE fingerprinting — **on-site, in-scope use only**

### RFID & Badge Systems
- Job posts naming **HID, Prox (125 kHz), iCLASS / Seos (13.56 MHz), Lenel, AMAG, Genetec** — tells you the credential technology and therefore what's in play
- Security-integrator contracts and case studies
- Glassdoor / employee handbooks for badge policy (PIN+card? tailgate culture?)

### Door Hardware & Locks *(new — identification only)*
- Listing photos, Street View, and lobby tours reveal **strike/lever/maglock** types, REX sensors, request-to-exit motion detectors, and whether doors fail-secure vs. fail-safe
- Brand markings on hardware (e.g., visible cylinder/lever manufacturers) inform what the on-site team should prepare for — recorded for planning, not bypass instructions here

### Cameras & Surveillance
- `inurl:/viewerframe?mode=` and similar legacy dorks (note: viewing third-party cameras out of scope is off-limits)
- Shodan for exposed cams/controllers **associated with the target only**
- LinkedIn/job posts naming Genetec, Axis, Milestone, Avigilon → coverage and analytics expectations
- Street View / tours → map visible camera placement and blind spots

### Fire & Safety Plans
- City planning / public records (floor plans are often public)
- Tenant handbooks
- Event-venue evacuation maps (frequently online)

---

## 6. Vehicle & Logistics Intelligence

### Corporate Vehicles
- Google Images: "Company fleet vehicles"
- Instagram hashtags: `#CompanyNameTrucks`
- DOT/DMV / FMCSA records

### Shipping & Receiving
- Yelp / Google reviews mentioning loading docks, freight, deliveries
- Guard or delay complaints in reviews (procedure leaks)
- Import/export records: [ImportYeti](https://www.importyeti.com/), [TradeMagellan](https://www.trademagellan.com)
  - *Use the free tiers to find records of interest, then Google the bill-of-lading or unique reference numbers for more detail. Free sites limit data, but the unique IDs unlock more once you know what you're after.*

### Maintenance Schedules
- Janitorial/landscaping job posts (often state shift times)
- Vendor schedules in handbooks
- Trash & shred pickup timing (document-discard windows)

### Drone / Aerial Recon *(new)*
- Pre-collected aerial imagery (Earth, NearMap) before any live flight
- Live drone recon only if explicitly authorized — check FAA Part 107, local ordinances, and the ROE; many sites near airports, prisons, or government facilities are no-fly

---

## 7. Tooling & Automation

- **Maltego** — entity link analysis (people ↔ company ↔ domain ↔ vendor)
- **SpiderFoot** — automated multi-source OSINT collection
- **recon-ng** — modular recon framework
- **theHarvester** — names, emails, subdomains
- **ExifTool** — metadata from harvested files
- **Google Earth Pro** — historical imagery, measurement, path planning
- Build a single case file (Maltego graph or structured notes) so facility, people, vendor, and access-control findings cross-reference cleanly

---

## 8. From OSINT to Op Plan

Recon is only useful if it converts into a plan:
- **Approach/egress routes** and timing (shift change, deliveries, lunch, after-hours) from habits + maintenance data
- **Best entry vectors** ranked by observed control gaps (tailgate-friendly door, unmonitored dock, weak visitor process)
- **Pretext ↔ entrance ↔ shift** matrix anchored to verified names/vendors/lingo
- **Control inventory** (badge tech, camera brand, lock/door type) so the on-site kit and skills are scoped before you arrive
- **Contingencies & abort criteria** tied to the ROE

---

## Reporting & Documentation

- Log **sources and timestamps** for every finding (clients and legal will ask how you knew)
- Capture screenshots with provenance; note what was OSINT vs. on-site
- Flag anything collected that's **out of scope** (neighbors, third parties) and quarantine it
- Deliver findings as actionable remediation, not just "we got in" — the value is closing the gaps you found

---

© 2024–2026. Released under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**. You may share and adapt this material for any purpose, even commercially, so long as attribution is provided.
