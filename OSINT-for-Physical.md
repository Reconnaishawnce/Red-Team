# OPRT: Open Source Intelligence (OSINT) checklist for Physical Red Teaming Operations

**Objective**: Identify information that enables you to gain access to secured assets in the way an adversary would.  

---

## 🔥 Top 5 Starting Points

- **Google Dork** for document leakage  
  _e.g._ `site:example.com filetype:pdf` (.docx, .xlsx, .pptx)

- **Google Earth & Street View**

- **Building Blueprints**
  - Check landlord websites (LoopNet, CoStar)
  - City planning documents

- **LinkedIn for employees and badge photos**

- **Listed jobs**  
  Look for clues about systems, processes, and social engineering opportunities

  ## 🔥 Favorite Links & Websites

- **IntelTechniques** Tools for OSINT: [IntelTechniques](https://inteltechniques.com/tools/Address.html)
- **OSINT Framework** for the latest resources: [OSINT Framework](https://osintframework.com/)

---

## 1. 🏢 Facility Reconnaissance (Physical & Perimeter)

### ✔ Building Addresses & Locations
- Google Maps (Street View, Satellite, Earth 3D)
- Bing Maps (Bird’s Eye)
- OpenStreetMap
- LinkedIn (for building names and architect portfolios)
  - _e.g._ `site:linkedin.com "123 Main Street" Design OR Architect

### ✔ Access Points & Security Features
- Parking lots & garages (employee vs. visitor)
- Entrances/exits: main, side, loading, emergency
- Fencing, gates, turnstiles
- Guard shacks, sensors, lighting, cameras

### ✔ Building Infrastructure
- HVAC (rooftop access)
- Utility & telecom rooms
- Roof access points (fire escapes, hatches)
- External staircases

### ✔ Business Directory & Listings
- Google My Business
- Yelp / TripAdvisor (interior photos)
- LoopNet / CoStar
- Use tax records to ID building owner
- Search Internet Archive for older listings

### ✔ Proximity Risks & Enablers
- Nearby police stations, government offices, politicians
- Embassies, consulates, intelligence hubs
- Shooting ranges, jails, prisons
- Homeless encampments, tents
- Crime maps, local police reports

### ✔ Blueprints & Technical Documents
- Identify the owner of the building. Search their website for PDFs (Site:ids-center.com .pdf) 
- Identify the building management company. Search their website for PDFs
- Search local government/municipality documents for the address, including construction permits, city permits, and tax records.

## 2. 🧑‍💼 Employee & Organizational Intelligence

### ✔ Employee Name Harvesting
- LinkedIn (Company + “People”)
- ZoomInfo / RocketReach / SignalHire
  - When signing up for an account, do **not** give these websites access to your email and don't use their plugins. That is how they scrape/collect data. 
- Staff bios on the company site

### ✔ Email Patterns
- Hunter.io
- OSINT Email Lookup Tools
- Google Dork: `@company.com site:linkedin.com`

### ✔ Contact Info
- TruePeopleSearch / WhoCalledMe / TrueCaller (US)
- FOIA requests (public sector)
- Company press releases

### ✔ Hiring & Job Posts
- LinkedIn, Indeed, Glassdoor, ZipRecruiter
- Look for references to badge access, policies, vendors

### ✔ Vendors & 3rd Parties
- Cleaning, maintenance companies (Yelp, job postings)
- IT vendors (non-@company emails)

### Ad and Technical Intel
- [Facebook and Instagram Ad Library](https://www.facebook.com/ads/library)

---

## 3. 🪪 Badge & Uniform Recon

### ✔ Badge Photos
- LinkedIn profile pics, social media
- Conference slides and press kits

### ✔ Uniform & Dress Code
- Website staff photos
- Job listings for “company-issued uniforms”
- Instagram, TikTok, etc.

### ✔ Courier & Vendor Pretexts
- FedEx, USPS, DHL, vendor logos
- Google Images: `"vendor name" site:company.com`

---

## 4. 🎯 Social Engineering Attack Surface

### ✔ Employee Habits & Check-ins
- Instagram, Facebook location tags
- Twitter/X searches like “Working at [Company]”
- [Strava Global Heatmap](https://www.strava.com/maps/global-heatmap?sport=All&style=dark&terrain=false&labels=true&poi=true&cPhotos=true&gColor=blue&gOpacity=100#16.47/43.932252/-102.159401), Fitbit, MapMyRun
   - *This is useful for more rural sites. You can find common running or biking routes near a facility. You can learn nearby traffic patters and hotspots for exercise, which could enable loitering and opportunities for surveillance. This can also show where people park, where there are fences (if there's a line the paths don't cross), and you may even find guard patrol routes along the perimeter.* 

### ✔ Company Lingo & Internal Culture
- LinkedIn posts, Glassdoor reviews
- Industry Slack/Discord chatter

### ✔ Events & Conferences
- EventBrite, Meetup RSVPs
- Company blog & speaker announcements
- Industry summits and attendee lists

### ✔ IT & Help Desk Clues
- Glassdoor reviews
- Help Desk/SOC job postings (look for MFA, reset workflows)

### ✔ Executive & VIP Profiles
- Google Dork: `"CEO name" filetype:pdf`
- People search tools: Pipl, FamilyTreeNow
- FOIA filings (public sector execs)
- Public company 10-Ks (investor sites)
- Executive interviews (home or office reveals)

---

## 5. 🧱 Building & Access Control Intelligence

### ✔ Wi-Fi Networks
- Wigle.net
- War-driving (WiFi Pineapple, Kismet)
- Conference/guest passwords on Reddit or Twitter

### ✔ RFID & Badge Systems
- Job posts mentioning HID, Lenel, Prox, RFID
- Security vendor contracts
- Glassdoor or handbooks for badge policies

### ✔ Cameras & Surveillance
- Google Dork: `inurl:/viewerframe?mode=`
- Shodan.io (exposed cams, badge readers)
- LinkedIn for brands like Genetec, Axis, Milestone

### ✔ Fire & Safety Plans
- City planning/public records
- Tenant handbooks
- Event venue evacuation maps

---

## 6. 🚛 Vehicle & Logistics Intelligence

### ✔ Corporate Vehicles
- Google Image search: “Company fleet vehicles”
- Instagram hashtags: `#CompanyNameTrucks`
- DOT/DMV records

### ✔ Shipping & Receiving
- Yelp or Google reviews mentioning loading docks
- Complaints in reviews about guards or delays
- Import / Export Records: [ImportYeti](https://www.importyeti.com/), [TradeMagellan](https://www.trademagellan.com)
  - *Use the free sites to find data of interest, then google the bill of landing or other unique numbers that you want more information about. The free sites tend to provide limited information, but you can find additional details by searching for specific import/export records once you identify what you're interested in.* 

### ✔ Maintenance Schedules
- Janitorial job postings (include shift times)
- Handbook notes on vendor schedules
- Trash pickup info (for document discard timing)

---

© 2024. This checklist is released under the Creative Commons Attribution 4.0 International License (CC BY 4.0). You may share and adapt this material for any purpose, even commercially, so long as attribution is provided.

---

