# RPRT: Reconnaissance for Physical Red Teaming

**Objective:** Get close and map how the target's security actually works, so the team can pick the way in.

Reconnaissance is the short, focused, breach-oriented phase. Surveillance told you what normal looks like and when the window opens. Recon goes up to the controls themselves and characterizes them: which doors, which locks, which readers, which cameras, which gaps. The output is an attack path with a primary and a fallback, documented well enough to brief and to hand to the client afterward. This file is the companion to the OSINT and Surveillance checklists and comes last in that arc.

## Recon vs. Surveillance

- **Surveillance** answers *what is normal here?* Patient, distant, observation over time. Pattern of life, people flow, the rhythm of the place.
- **Recon** answers *how do I get in?* Short, close, and intentional. You are assessing specific entry points and controls, often from the hot zone, sometimes from inside under a pretext.

Recon carries more risk than either OSINT or surveillance because you are near or on the target and your purpose is harder to explain. Treat every recon look as exposure and keep it brief.

## Scope of This Document

This is an assessment checklist. It tells you what to identify and how to characterize a control's strength, placement, and use. It does **not** cover how to defeat locks, clone credentials, or bypass sensors. Those are exploitation techniques governed by your training and the rules of engagement, performed only during an authorized breach. Recon documents the vulnerability. The op exploits it.

## Top 5 Starting Points

1. Walk or drive the full perimeter once and identify every way in: main, side, employee, dock, emergency.
2. For each entry, characterize the door, the lock, the reader, and the egress method, then photograph it.
3. Map camera placement and find the blind spots between coverage.
4. Read the access-control culture: do badges get checked, do doors get held, do people get challenged.
5. Identify a primary entry path and at least one fallback before you leave.

## Authorization and Legal Boundaries

Recon puts you closest to the line, so the paperwork matters most here.

- **Carry the authorization letter on your body.** Signed, naming the assessing org, the client signatory, target addresses, dates, and the activities permitted. This is your get-out-of-jail document when a guard or police officer asks.
- **Know the breach boundary.** Recon and breach are sometimes separate engagements. If the ROE authorizes assessment only, you do not actually defeat a control, enter without permission, or test a lock. Confirm what "recon" means for this job before you go.
- **Scope discipline.** Stay on the named target. Shared buildings, neighboring tenants, and third-party property are out unless explicitly listed.
- **Credential and network tools are governed by the ROE.** Characterizing badge technology or surveying wireless can be in scope. Cloning a card or touching the live network is exploitation and only happens if the engagement authorizes it.
- **Audio.** Recording conversations triggers wiretap and consent laws. Use audio for your own voice notes, not to capture other people, unless counsel cleared it in writing.
- **Comms and abort.** Have a check-in cadence, a client emergency contact reachable during the look, and clear abort criteria. Two operators are safer than one for on-site recon.

If it is not in the authorization and the ROE, it does not happen.

## Zones, Cover, and Deniability for Recon

Most recon happens in the hot zone, up against the controls, so cover has to carry more weight than it does in surveillance.

- You usually need a reason to be exactly where you are: a delivery, a contractor visit, a tenant tour, a job interview, a wrong-building visitor. Anchor the pretext to something real (a vendor that services the site, a tenant that exists) so it survives a question.
- Keep dwell short. A close look that lasts thirty seconds and moves on beats a lingering inspection that gets remembered.
- Observe controls indirectly where you can. You can read a lot about a door on the way past it without stopping to study it.
- Build the cover story from a kernel of truth. A story with real elements is easier to remember and tell, which lowers the cognitive load and the tells that come with lying.
- Have the exit decided before you commit. If the cover does not hold cleanly, leave smoothly rather than improvise.

## 1. Exterior Reconnaissance (Perimeter and Entry Points)

### Building Access Points
Identify and photograph every entry: main entrances, side and employee-only doors, loading docks and maintenance access, emergency exits. For each, characterize:
- Door type: solid versus glass, single versus double, sidelights, automatic operator or ADA push button
- Swing direction (inswing or outswing) and hinge location (interior or exterior) and type (standard or security hinges)
- Lock and latch type: deadlatch, deadbolt, panic/crash bar, electric strike, magnetic lock
- Whether it currently sits locked or unlocked, and whether it is ever propped
- Egress method: does a person have to badge to exit (anti-passback), or is exit free
- Request-to-exit (REX) presence and type (motion sensor, touch bar, button), visible through the glass
- Fail-safe versus fail-secure behavior where you can infer it (what happens to the lock on power loss)
- Door position switches or contacts, and the gap at the frame

### Perimeter Security
- Fencing: height, material, gaps, climbability, anti-climb features
- Walls, gates (manual or automatic), bollards, barriers, vehicle controls
- Guard stations and patrol routes (cross-reference the surveillance pattern of life)
- Cameras: visible and concealed, dome versus bullet versus PTZ, height, coverage arcs
- Sensors: ground, building, pole-mounted, or drone/UAS detection
- Lighting coverage and the dark zones between fixtures, and whether lights run on timers or photocells
- Natural cover and concealment around the perimeter (vegetation, structures, grade)

### Signage and Entry Policies
- Posted visitor policies and check-in requirements
- Restricted-area and no-trespassing warnings
- Stated rules on badges, guests, and escorts
- "Premises monitored" or recording notices (a tell about both cameras and legal posture)

### Parking and Vehicle Access
- Employee versus visitor parking, and how each is controlled
- Vehicle security checks, gate arms, guard booths
- License plate readers, decal or permit enforcement, ticketing
- Whether a vehicle can be staged on or near the lot without drawing attention

## 2. Entryway and Access Control Recon

### Door Security
- Keypads (mechanical or electronic, fixed or randomized layout)
- Badge readers (low-frequency prox, high-frequency smart card, or mobile/BLE)
- Biometric readers (fingerprint, face, iris) and whether they are primary or secondary
- Buzzer and intercom systems: who responds, and do they verify before releasing the door
- Propped or unattended side entrances

### Turnstiles and Badge Systems
- Are badges required, and are turnstiles optical (waist-high) or full-height
- How easily a person can tailgate or piggyback, and whether doors fully close between people
- Whether employees display badges openly or keep them hidden, and how they wear them
- Whether security checks faces against the badge or a screen, or just watches the light turn green
- Anti-tailgate sensors and badge-back enforcement
- Badge color-coding by access level, which leaks who can go where

### Reception and Visitor Handling
- Are visitors signed in, escorted, and issued a temporary badge
- Is the front desk always staffed, and can it see all the entrances it is responsible for
- Is reception also doing other work that pulls attention off the door
- Is there enough lobby staff to both help visitors and monitor access at once
- Visitor management system in use (paper log, kiosk, photo badge)

### Delivery and Contractor Access
- Where couriers drop packages, and whether there is a separate delivery entrance
- Whether maintenance and contractor crews need a badge, and how they are vetted
- Whether contractors are escorted or allowed through security to go get a badge
- Dock procedures: who signs, how long the bay stays open, is it watched

## 3. Interior Reconnaissance (If Access Is Permitted)

Only if the ROE allows you inside. Everything here is observation, not interference.

### Security Desk and Cameras
- Where guards sit, what they can see, and whether they are watching the monitors
- Interior camera placement and the blind spots between coverage, especially elevator lobbies and stairwells

### Floor and Vertical Access Control
- Elevators: is a badge required to select a floor, and which floors are open
- Stairwells: are the doors access-controlled, locked from the stairwell side, and which floors allow re-entry
- Whether stairs offer a way around a turnstile or elevator control

### Workstation and Information Security
- Unattended unlocked laptops and desktops, clean-desk discipline
- Visible credentials, sticky-note passwords, or sensitive documents
- Printers and multifunction devices, and whether they require a badge to release jobs
- Badge-sharing or tailgating happening inside

### Networking and Wireless
- Visible guest and corporate SSIDs, and whether guest is segregated
- Open network jacks in lobbies, conference rooms, and common areas
- Employee use of USB drives or external storage
- Passive wireless survey only, and only if scoped. No association, no scanning of the live network unless authorized.

### Sensitive Areas and Emergency Routes
- Signage or layout pointing to server rooms, IDF/MDF closets, records, and mailrooms
- Emergency exits: alarmed or silent, crash-bar equipped, usable for egress
- Fire stairwells: locked from the inside, re-entry behavior, whether opening one alarms

## 4. Employee Behavior and Security Culture

The human layer is usually the softest, and it is pure observation.

- **Badge discipline:** are badges worn consistently, and are the fronts visible enough to photograph and reproduce
- **Challenge culture:** do employees challenge unfamiliar faces, or assume someone else vetted you (diffusion of responsibility is your friend and their weakness)
- **Guard engagement:** active and scanning, or passive and bored
- **Escort and guest policy:** do visitors actually get escorted, do employees let in friends, family, or a confident stranger
- **Helpfulness as a vulnerability:** who holds doors, who walks a "lost" person in
- **Smoking and break doors:** the propped side door is a recurring gift
- **New-hire density:** in a fast-growing or high-turnover site, nobody knows everybody

## 5. Documentation and Exit Strategy

### Capture While You Can
- Sketch the layout and mark doors, readers, cameras, blind spots, and choke points
- Record security lapses specifically, with enough detail to brief and to remediate
- A notebook often draws less suspicion than a phone. Voice notes to yourself work where writing does not.

### Map Entry and Exit
- Identify a primary entry path and at least one fallback
- Locate legitimate places to be while inside (restrooms, break rooms) and the security desk to avoid
- Identify multiple egress options before you need them

### Leave Clean
- Do not stay in one spot too long, and rotate positions across looks
- If questioned, deliver the cover story and exit smoothly rather than escalating
- Use a cover story built on a kernel of truth. It is easier to remember and takes less effort to tell, which reduces the tells that come with a full fabrication.

## Recon Gear

Carry a small, discreet kit focused on documentation, mapping, and characterization. The right kit also reinforces your cover, so match it to the pretext.

### Essential Kit

| Item | Purpose |
|---|---|
| Authorization letter and photo ID | Your get-out-of-jail document and identity if challenged |
| Notebook and pen | Note-taking that looks less suspicious than a phone |
| Small flashlight | Reading locks, keypads, and hardware in dim light |
| Binoculars or monocular | Standoff observation of controls and signage |
| Earbuds with mic | Voice notes to yourself without obvious filming |
| Camera or covert body cam | Documentation, only where legally permitted, no suspicious movements |
| Small multitool | General utility, not for defeating controls outside scope |
| Power bank and cable | Keep devices alive across a long look |
| Bluetooth tracker (AirTag/Tile) | Tagging your own placed gear and testing asset-tracking response |
| Neutral clothing | No logos or flashy designs, dress to the environment and cover |
| Burner phone | Keeps sensitive media off your personal device, hand to client after |

### Optional Technical Kit (Experienced Operators)

| Item | Purpose |
|---|---|
| RFID reader/identifier | Characterize the badge technology in use (cloning is exploitation, ROE-gated) |
| Wi-Fi survey rig (Kismet, etc.) | Passive wireless reconnaissance, in scope only, no association |
| Thermal camera attachment | Spot IR illuminators and active electronics, and flag keypad-wear as a finding |
| Laser distance measurer | Calculate sight lines and camera coverage areas |
| Inspection mirror or periscope | Checking corners, behind objects, and under fixtures |
| Night vision / IR viewer | Identify cameras and infrared floodlights after dark |

Note on audio: recording other people's conversations is a wiretap and consent issue and is almost never in scope. Keep audio to your own notes unless counsel has cleared it.

## From Recon to the Op

Recon exists to produce a plan you can brief.

- **Attack path:** the chosen entry, the control that gets defeated or bypassed, and why it is the soft point
- **Primary and fallback:** never one plan. Identify a backup entry and a backup pretext.
- **Pretext-to-entry mapping:** which cover gets you to which door at which time, drawn from the surveillance window
- **Control inventory:** the door, lock, reader, and camera details that tell the breach operator what skills and kit to bring
- **Contingencies and abort:** what burns the op, what you do if challenged, and when you walk away

## Reporting

- Log positions, covers, timestamps, and sources for every observation
- Keep photos and sketches with provenance, and separate what was observed from what was inferred
- Quarantine and document anything out of scope
- Deliver findings as prioritized, fixable vulnerabilities (this door, this gap, this habit), not just "here is how we would get in." The value to the client is the remediation, not the war story.

© 2024-2026. Released under the Creative Commons Attribution 4.0 International License (CC BY 4.0). You may share and adapt this material for any purpose, even commercially, so long as attribution is provided.
