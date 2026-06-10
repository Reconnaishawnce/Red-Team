# SPRT: Surveillance for Physical Red Teaming

**Objective:** Observe the target over time to learn what "normal" looks like, so you can predict it, exploit it, and disappear into it.

Surveillance is the patient phase. You are not yet trying to get in. You are building a pattern of life: who comes and goes, when, in what, through which door, watched by whom. Done right, it tells you the best window for the op and teaches you how to look like you belong. This file is the companion to the OSINT checklist and comes before focused breach recon.

## Surveillance vs. Recon

Keep the two jobs separate in your head, because they carry different risk and different goals.

- **Surveillance** answers *what is normal here?* It is observation over time. Pattern of life, people flow, parking habits, shift changes, guard behavior, the rhythm of the place. The output is a baseline you can blend into and a window you can act in.
- **Recon** answers *how do I get in?* It is focused, breach-oriented assessment of specific doors, locks, sensors, and gaps. Higher intent, higher risk, usually shorter and closer.

You surveil first to understand the environment, then run recon against the specific points that pattern of life flagged as soft. Treat this document as the surveillance half. Breach recon is its own file.

## Top 5 Starting Points

1. Sit in a coffee shop, on a bench, or in another spot with line of sight to the main entrance and watch normal activity for several hours before you do anything else.
2. Establish the norms: behavior, dress, belongings, gait, eye contact, friendliness, phone use. You cannot blend into a baseline you have not measured.
3. Capture primary entrances, secondary doors, and emergency exits.
4. Capture the security technology in use: turnstiles, cameras, readers, doors, gates, alarm signage.
5. Capture badge design from public and social sources, confirmed at distance in the field, so a convincing replica can be produced.

## The Core Discipline: Zones and Deniability

Every minute of surveillance, ask two questions. Where am I, and what is my reason for being here?

### Hot Zone vs. Cold Zone

A **hot zone** is anywhere your presence is inherently suspicious or where being noticed costs you the engagement. Directly outside the target entrance, inside the parking lot, loitering at the fence line, anywhere a guard or employee would reasonably wonder why you are there. In a hot zone, assume you are watched, minimize dwell time, never repeat the same position or vehicle, and prefer remote cameras or moving passes over a parked body.

A **cold zone** is a position with natural cover and distance where your presence reads as ordinary. A public park across the road, a cafe with a window, a parking structure two blocks away, a treeline on a rural approach. Cold zones buy you time and let you use better optics, but they still require a cover story and they still have eyes (neighbors, regulars, other cameras).

There is a transition band between them. A spot that is cold at 2pm on a weekday can turn hot at 6am when the lot is empty and a single parked car stands out. Re-evaluate the zone every time conditions change: time of day, traffic, weather, who else is around.

### Plausible Deniability

Deniability is the gap between what you are actually doing and the innocent explanation available if someone asks. You want that gap to be zero. Build two covers and keep them consistent:

- **Cover for status:** who you appear to be. A dog walker, a jogger, a delivery driver, a utility contractor, a photographer, a parent waiting for a kid, a fisherman, a birder.
- **Cover for action:** why you are doing the specific thing you are doing right now, in this spot, with this gear.

The test is simple. Does your activity match your cover without explanation?

- A person in a forest looking at a building through binoculars is suspicious. The same person with binoculars, a field guide, and a camera on a strap reads as a birder, and that is deniable.
- A person sitting in a parked car staring through binoculars at a building window is suspicious and has no cover. There is no innocent version of that.
- A dug hole, a hidden hide, a camera zip-tied to the target's own fence: not deniable, and often crosses from observation into trespass or worse.

Match the cover to the environment. A birder works in a park or a wood line and looks absurd in a corporate parking garage. A contractor in hi-vis works near a construction site or utility box and looks wrong in a residential cul-de-sac at midnight. Pick a cover the location already expects to see, then dress, equip, and behave to fit it. Pre-stage the props that sell it (the leash, the field guide, the clipboard, the coffee) and rehearse the one-line answer you give if challenged, then leave.

If your cover would not survive a polite "can I help you?" from a guard, you do not have a cover. You have a problem waiting to happen.

## Authorization and Legal Boundaries

Surveillance carries heavier legal exposure than open-source research because it happens in the physical world and can sweep in third parties. Before any field work:

- **Written authorization and scope.** The engagement letter must cover physical observation of the named target. Confirm the property boundaries and what vantage points are public versus private.
- **No audio.** Most jurisdictions treat audio recording very differently from video. Wiretap and two-party consent laws can make a recorded conversation a felony. Run cameras with audio disabled unless counsel has cleared it in writing. Overhearing public conversation is fine. Recording it usually is not.
- **Reasonable expectation of privacy.** Do not record into windows of residences, restrooms, locker rooms, or other private spaces, even from a lawful public position. Frame on entrances, lots, gates, and exteriors.
- **No tracking devices on people or third-party vehicles.** GPS trackers on vehicles you do not own raise trespass-to-chattels and stalking-statute issues and are almost never in scope.
- **No tampering with other people's devices.** Use cameras you own and control. Accessing or manipulating a target's or third party's camera, vehicle system, or network is unauthorized access and out of scope, full stop.
- **Stalking and harassment statutes** apply to individuals. You are assessing a facility and its routines, not following a named person around their personal life. Keep the focus on the site.
- **Drones** are governed by the FAA (Part 107), local ordinances, and the ROE. Many sites near airports, prisons, and government facilities are no-fly.

If it is not in the authorization and the ROE, it does not happen.

## Pre-Surveillance Planning

Plan before you sit. Fishing trips burn time and expose you for nothing.

### Define Objectives
- Write the specific questions this surveillance must answer (shift-change timing, guard cadence, tailgate culture, lot access method, the likely act window). Collect against the list, not at random.
- Decide what counts as "enough" so you know when to stop watching and pull off.

### Choose Your Method Mix
- Pick the lowest-exposure method that answers each question: standoff camera, fixed cold-zone post, foot pass, brief drive-by. See **Methods** below. Default away from mobile following unless it is scoped.

### Prepare Cover and Gear
- Cover for status and action chosen, dressed, and rehearsed before you arrive. Props staged. Gear matched to the cover and nothing that contradicts it.
- A second cover story ready in case the first is questioned.

### Bail and Reset Plan
- Decide in advance where you go if spotted: a real, unrelated public destination, not a panicked drive home.
- Identify where you can change appearance (reversible jacket, hat on or off, swap vehicle) and where you can stash or hand off gear.
- Know your exit before you need it.

## What to Collect: Pattern of Life

This is the product of surveillance. The goal is a baseline detailed enough that you can predict the site and spot the anomaly that is you. Vary your observation across hours, days, and conditions: weekday versus weekend, day versus night, fair weather versus rain, normal versus event days. Several short looks beat one long stakeout for both data quality and exposure.

### Temporal Rhythm
- Opening and closing times, and how rigid they are
- Shift changes (when guards and staff rotate, and the gap of distraction around it)
- Delivery windows and which carriers arrive when
- Cleaning and janitorial crew arrival and departure
- Lunch and break exodus, smoke-break timing and locations
- When the lot fills and empties, and the last person out
- Interior and exterior lights on/off schedule
- Guard patrol cadence: fixed post, roving, or none, and how alert

### People and Norms
Measure the baseline you intend to vanish into.
- Dress: business, casual, uniform, and how consistent
- Badges: worn on a lanyard or clipped, displayed or hidden, kept on outside the building or stripped at the door
- Bags and belongings: backpacks, laptop bags, lunch, what is normal to carry
- Gait and pace: purposeful, casual, hurried
- Eye contact and friendliness: do people greet strangers or ignore them, do they hold doors
- Phone use while walking and waiting
- Roles you can distinguish by dress, badge, or behavior (staff, exec, vendor, visitor, guard)
- Vendor baseline: typical uniforms, vehicles, where they go, how they are received
- Visitor baseline: escorted or not, lanyard color, where they wait
- Regulars you will see repeatedly, and who among them would notice a stranger

### Vehicles and Parking
How people park tells you the culture and gives you a way to blend.
- Assigned versus open parking, employee lot versus visitor lot versus street
- Access control on the lot: arm gate, badge, decal, permit hangtag, plate reader, or open
- Where executives park, where vendors and deliveries park, where visitors are funneled
- Habits: do people back in, leave engines running, sit in cars before going in, carpool
- Gate behavior: do cars tailgate through the arm, how long does it stay up
- Common vehicle types in the lot, so your vehicle matches rather than stands out
- Local plate norms (a rental or out-of-state plate sitting for hours is a flag)
- Delivery and maintenance timing, and whether those crews hold their own keys or badges

### Access Behavior
- Which doors actually get used versus which are decorative or alarmed
- Propped doors, smoke-break doors, doors left on a latch
- Badge-in versus buzzer-and-wait versus staffed reception
- Where people badge in (turnstile, elevator, interior doors) and whether guards actually check or wave people through
- Tailgating: is it routine, do people hold the door for strangers, are they distracted or rushed at the reader
- Observed visitor process: sign-in, escort, badge issue, or wave-through
- Loading dock and receiving: which bay, who signs, how long it stands open

### Security Posture Over Time
- Guards: patrol frequency and routes, fixed versus roving, armed or unarmed, uniform and kit, engaged and scanning versus heads-down
- Camera coverage and behavior: fixed versus PTZ, where they point, when a PTZ sweeps, the blind spots that open up as it moves
- Lighting at night: which areas are lit, which go dark, where the shadows fall
- Emergency exits: are they used routinely (propped for breaks), alarmed or silent
- Alarm response: if an alarm trips or a drill runs, how fast and how many respond, and from where
- After-hours: guard presence and posture, whether security escorts employees to their cars after dark
- How the whole posture changes off-hours and on weekends

### Capture Priorities (Shot List)
Record what exists and how it is used. Close-up assessment of locks, sensors, and hardware is the recon phase, not this one.
- Primary entrances, secondary and side doors, emergency exits, loading dock
- Security technology: turnstiles, mantraps, gates, cameras (count, type, placement), readers, intercoms, visible door hardware, alarm signage
- Badge design: color, layout, logo, photo placement, orientation, lanyard or clip, captured from public sources and confirmed at distance, for producing a convincing replica
- Lighting and dark spots after dark
- The norms above, documented well enough that an operator can dress and move to match

### Environment and People Flow
- Foot traffic patterns and natural loitering spots (bus stop, coffee, smoking area)
- Neighbors and adjacent businesses, and how nosy they are
- Police presence and patrol frequency in the area
- Who already belongs to the streetscape (dog walkers, joggers, regulars) so you can join it
- Public work-talk and exposed laptops: do employees discuss work or leave internal screens open in cafes (observe only, never record audio)
- Local rhythm that lets you become a recognized, unremarkable fixture

### People of Interest (Role-Based)
Keep this tied to the authorized target and to roles, not to anyone's personal life.
- Identify by dress and behavior which people likely hold elevated access (facilities, IT, management, security)
- Note who reads as approachable for a pretext interaction and who does not
- Observe whether badges are worn off-site, at lunch or in the lot, which is both a capture opportunity and a finding to report

## Blending In and Field Tradecraft

Pattern of life is also how you learn to vanish into the scene.

- Dress to the environment and the cover, one notch more boring than average. Gray man, not memorable.
- Match the pace and demeanor of the people around you. Purposeful, unhurried, slightly bored.
- Become a regular slowly. The car that has been in the cafe lot every morning for a week is invisible. The car that showed up once and sat for three hours is a report.
- Vehicle choice: common make and muted color, local plates, maybe a contractor magnet or a kid's sports decal. Nothing that gets described later.
- Do not linger unnaturally. People in public are going somewhere. Give yourself somewhere to be going.
- Observe indirectly. Use window and mirror reflections, peripheral vision, and your camera screen instead of staring at the target. Repeated direct looks at the same point draw attention. Sweep naturally.
- Have a reason to be doing exactly what you are doing, every second, that a stranger would accept and forget.
- If you are spotted or challenged and the cover does not cleanly hold, act like you belong or leave. Do not improvise a worse story.

## Standoff and Remote Capture

The lowest-exposure surveillance is the kind where you are not there. Cameras you own and control can build pattern of life around the clock without a body on the X.

### Devices You Own and Control
- **Cellular trail/game cameras.** Battery or solar, motion or time-lapse, upload images or clips over LTE so you never return to retrieve a card. Built for concealment outdoors.
- **Dashcams in a vehicle you own.** Park a legally parked car with a front and cabin-facing camera running and you have a static observation post with a built-in cover (it is just a parked car). Many record on motion or run a parking mode.
- **Built-in vehicle cameras on your own vehicle.** Sentry-style multi-camera systems on a car you own capture a wide field while parked and read as nothing but a car.
- **Your own covert camera placed on authorized ground or a public vantage.** Only where the engagement permits.

### Placement and Framing
- Concealment and sightline first: clear view of the entrance, gate, or lot, with the camera itself hidden or unremarkable.
- Sun angle matters. A camera shooting into the rising or setting sun gives you a silhouette and nothing else. Scout which direction the light comes from at the hours you care about and place accordingly.
- Frame exteriors only: entrances, lots, gates, docks. Never into windows or private interiors.
- Choose capture mode for the question: motion-triggered for events, time-lapse or interval for building a daily rhythm cheaply.

### Power, Endurance, Detection
- Solar panels and external battery packs extend a deployment from days to weeks.
- At night, infrared illuminators glow visibly to anyone looking, and lenses glint. Assume a security sweep can find a camera, and assume the client may want it either deniable or attributable. Know which before you deploy.
- Retrieval is exposure. Cellular models that upload remotely let you avoid return trips. If you must retrieve, treat each visit as a fresh surveillance problem with its own cover.

## Methods: Static, Mobile, and Foot

- **Static post.** A vehicle, a building, or a fixed vantage point. A vehicle hide works if you sit out of the obvious sightline, keep the engine and your movement quiet, park legally, and rotate positions across visits. The same car in the same spot twice is how you get burned.
- **Vantage points.** Public parks, parking structures, adjacent businesses, cafes with the right window, high ground, and rural tree lines (with a cover that fits the setting). Pick positions that are cold and that the location already expects people to occupy.
- **Foot.** Move with the existing foot traffic, on the routes locals already use. Walk like you have a destination.
- **Mobile/vehicle following** is high exposure, easy to detect, and frequently out of scope. Default to not doing it unless the engagement specifically calls for it and it is authorized.

Rotate times and positions so the full pattern emerges and so no single observer (camera, guard, neighbor) sees you twice.

## Optics and Gear, Chosen for Deniability

Pick the tool that matches the cover, not just the one that sees best.

- A camera with a long lens reads as a photographer or birder and is far more deniable than binoculars, especially anywhere public.
- Binoculars are fine with a birder or sports cover and terrible from a parked car aimed at a window.
- A compact monocular is discreet for a quick look without committing to a cover prop.
- Thermal and night optics extend night observation but carry their own legal and "why do you have that" problems. Reserve for cold zones and clear them against the ROE.

Whatever you carry, it should be consistent with who you are pretending to be. Gear that contradicts your cover is worse than no gear.

## Logging What You See

Surveillance is worthless if you cannot turn it into a pattern. Log as you go, with enough metadata that a finding holds up later.

Capture per observation: date, day of week, time in and out, position, weather, and what you saw. Build the raw entries into a pattern-of-life matrix (by hour across days) so the windows and anomalies jump out.

| Date | Day | Time | Position / Zone | Observation |
|---|---|---|---|---|
| 2026-06-10 | Tue | 0615 | Cafe lot (cold) | Cleaning crew van arrives, props east door ~40 min |
| 2026-06-10 | Tue | 0720 | Drive-by (hot) | Guard shift change, post unmanned ~5 min |
| 2026-06-10 | Tue | 1205 | Park bench (cold) | Lunch exodus to north smoking area, badge held for group |

- A notebook often draws less suspicion than a phone for taking notes. A quick voice memo records your own observations without obvious filming. Keep that to your own notes, never target audio.
- Tag the timings that matter most: shift changes, patrol passes, high-traffic versus dead hours.
- Photograph and film with timestamps, note your cover for each session, and flag anything observed that is out of scope (neighbors, third parties) so it can be quarantined and discarded.

## Counter-Surveillance Awareness

While you watch them, assume something watches you.

- Map the cameras that can see your positions and rotate to stay out of repeat frames. Near the perimeter, assume you are on camera.
- Track roving patrols and nosy neighbors as threats to your cover, not just as data.
- Watch for signs you have been made: a second look from a guard, someone on a phone while watching you, the same face or vehicle appearing near your positions.
- Ask after each session: did anyone notice or approach me, was I likely captured by the site's cameras, did my cover hold.
- On departure, run a short counter-surveillance route to confirm you are not followed before returning to base or moving to another site.
- If you think you are burned, abort, change vehicle and appearance, and reset another day. Never let the desire for one more data point keep you in a position past the point it stays deniable.

## Handing Off to Recon and the Op

Surveillance exists to feed the next phases.

- Pattern of life identifies the **window**: the shift-change gap, the propped delivery door, the dead hour in the lot.
- The blending lessons define the **operator's look**: how to dress, what vehicle, what pace, which door, what pretext the site already accepts.
- Remote cameras provide **day-of confirmation**: is today normal, is the window still open, before anyone commits to the X.

Write the surveillance findings as a baseline plus the anomalies and windows it reveals, then point recon at the specific soft points to assess up close.

## Reporting

- Log sources, positions, covers, and timestamps for every session.
- Keep video and stills with provenance, and separate OSINT-derived from field-observed.
- Quarantine and document anything out of scope.
- Deliver pattern of life as actionable findings (windows, gaps, blend-in failures the site should fix), not just raw footage. The value is showing the client the routine an adversary would exploit.

© 2024-2026. Released under the Creative Commons Attribution 4.0 International License (CC BY 4.0). You may share and adapt this material for any purpose, even commercially, so long as attribution is provided.
