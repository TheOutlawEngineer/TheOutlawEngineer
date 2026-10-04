> **A NOTE BEFORE YOU READ**
>
> Nothing in this paper names a vendor, a product, or a plant you should rip out. We won't pretend there's a buy-and-deploy fix. Our target is the decay in the middle — the years when a system is too critical to replace and too old to protect — and the economic and organizational forces that keep it there. If you're looking for a vendor to blame or a box to buy, this paper will disappoint you. That part is intentional.
>
> For operators, engineers, and students still entering this field, especially through workforce programs like WIOA: you are not being told your industry is broken and your job is hopeless. You're being told the truth about the infrastructure you'll actually inherit, so you can do the work with your eyes open. The ghosts are real. They're also manageable. That's what this paper is about.

# Ghost Architecture: The Haunted Substrate Beneath Modern Industrial Systems

## 1. Introduction — The Moment the Ghost Reveals Itself

During COVID, we ended up living inside a hardware ecosystem that shouldn't have existed. Part of the product we shipped was an EWS — an Engineering Workstation sentenced to a slow death in the steam-dampened depths of industrial facilities across the world. Under normal conditions, these machines were disposable. You shipped them, they ran until they didn't, and then the customer replaced whatever bargain-bin box could still run the vendor-locked HMI.

Then COVID broke the supply chain. And when the supply chain broke, the ghosts came out.

We couldn't get PCIe Arcport cards. We couldn't get the right chipsets. We couldn't get hardware capable of running the legacy OS demanded by the plant's controllers. So we did something modern engineering teams shouldn't ever have to do: we hunted down failing PCs shipped back from the field.

Not for repair. Not for warranty. For cannibalization.

We tore them down for parts. We harvested boards. We cloned drives. We hacked config files. We refurbished machines that should have been buried years earlier, resurrecting hardware that had already lived one full industrial lifetime. Then we shipped them back out — into the hands of field techs who were dubious at best, and right to be so — because there was no other option. The modern supply chain couldn't produce what the legacy software required, so we became the supply chain. We became the spare-parts bin for systems that should have been buried decades ago.

That's when it clicked: we weren't maintaining equipment. We were mediums for digital ghosts.

Every box we resurrected was another dead OS shoved back onto the line — no path forward, no vendor coming back for it.

Ghost Architecture is the haunted substrate beneath modern industry — built from machines that persist not because they're robust, but because the process breaks without them.

## 2. Origins — How the Haunting Begins

HMIs remain locked to Windows XP, 7, or 8 because the vendor runtimes they depend on were never modernized. Drivers exist only for extinct hardware. Control logic remains frozen in early-2000s frameworks that no modern OS can run without breaking the process. Replacing them requires rewriting entire industrial workflows, so they stay.

That's temporal fragmentation: one plant ends up living in several decades at once. Logic from 2001, an HMI from 2010, an OS from 2013, a network from 2026 — none of it built to work together.

## 3. Supply-Chain Propagation — How Decay Spreads

Ghost Architecture is distributed, not isolated. Vendors ship legacy requirements en masse because their software was never updated. Customers deploy haunted systems because they have no alternative. The vendor keeps shipping it, the customer keeps installing it, and after enough years nobody calls it legacy anymore.

COVID made this visible. The inability to procure modern hardware revealed how deeply legacy requirements were embedded. The industrial ecosystem wasn't modern — it was fossilized.

The Oldsmar water facility incident proved this wasn't theoretical — a fossilized Windows 7 workstation, placed on the internet for operator convenience, doing exactly what it was left able to do. (Full writeup in Appendix B.) The attacker didn't breach a complex modern network. They walked through a door left open because operators needed quick access — and because the box couldn't be replaced, the door couldn't be closed.

Oldsmar wasn't a unique failure. When legacy systems can't be modernized, convenience stops being a shortcut and becomes the architecture.

This is Layer 4 of the model in Section 5 — propagated decay — and it's the layer that makes the other three everybody's problem: fragility doesn't stay at one plant, it ships.

## 4. The EWS — Where OT Touches IT

The Engineering Workstation is where the dead stuff and the live stuff meet. These machines sit at the intersection of OT and IT, bridging two worlds that were never meant to meet: dual NICs, multi-VLAN access, contractor laptops, vendor tunnels, and domain membership converging on a workstation never designed to be a security boundary.

The danger isn't that the box is hackable. It's that the box is there. A forgotten Windows 7 workstation sitting near a core switch isn't a vulnerability in the usual sense — it's a structural flaw. It's a floor plan problem.

In December 2015, attackers didn't break Ukraine's SCADA — they hijacked it. After months inside the utility networks via spear-phished BlackEnergy implants, they used the operators' own remote-desktop sessions and HMI commands to open breakers at roughly 30 substations: ~230,000 customers dark for 1–6 hours, then KillDisk wipers and bricked serial-to-Ethernet converters to slow recovery. A year later they came back with Industroyer — malware that spoke the grid's own control protocols (IEC 101/104, IEC 61850, OPC DA) directly, no human operator needed, tripping a transmission substation near Kyiv in about an hour. The 2015 attack stole the operators' hands. The 2016 attack replaced them.

The Triton attack revealed the same pattern in safety systems. In the summer of 2017, attackers reached the engineering workstation that programmed the Schneider Electric Triconex safety controllers at a Saudi petrochemical plant and deployed the first malware ever built to target Safety Instrumented Systems — speaking the proprietary, undocumented TriStation protocol, exploiting a zero-day in the controller firmware, aiming to rewrite the safety logic itself. They got in because the controllers' physical key-switch had been left in PROGRAM mode during normal operation — a maintenance position, left engaged. A bypassed interlock by another name. They were caught only because their own code faulted and tripped the controller fail-safe.

These cases mirror the reality we lived during COVID. Many of the machines we shipped weren't just tied into front-end networks — they were tied directly to the internet because it made remote monitoring possible during travel restrictions and staff shortages. The fastest route won. A public IP slapped onto an EWS meant you could remote in from home. It wasn't secure, but it was real. Once online, they stayed online. Convenience became architecture; architecture became exposure.

## 5. The Ghost Architecture Model

Ghost Architecture operates as a layered physical-digital stack:

**Layer 1 — Legacy Systems.** Fossilized OSes, vendor-locked HMIs, outdated drivers, frozen control logic. The stuff from Section 2 that can't be replaced. These systems aren't old because nobody noticed — they're old because replacing them means rewriting the process they run. The Windows XP box driving the HMI isn't a computer anymore. It's a load-bearing part of the machine, same as a gearbox. Nobody specs a twenty-year-old OS. They inherit it the way you inherit a foundation: it's under everything, and touching it risks the whole structure.

**Layer 2 — Shadow Networks.** Forgotten VLANs, abandoned switches, flat segments nobody's allowed to unplug. Not the pathways anyone uses — the infrastructure nobody remembers, still powered, still forwarding. Every plant has a switch nobody will touch, because the last time someone did, something three buildings over stopped working and nobody could say why. The diagram says it doesn't exist. The blinking link lights say otherwise. Shadow networks are what the drift machine leaves behind after the crisis is over — the connectivity equivalent of scar tissue.

**Layer 3 — Spectral Adjacency.** The contact nobody designed and nobody owns. A dual-homed EWS, a contractor laptop, a vendor VPN tunnel left up after commissioning. Layer 2 is what got forgotten; Layer 3 is what everyone can see but nobody manages, because managing it means approving downtime nobody will sign off on. It's the most dangerous layer precisely because it's visible — visibility creates the assumption that someone is handling it. Nobody is. The EWS sits at the seam between OT and IT with a foot in each network, and both sides assume the other one secured it.

**Layer 4 — Propagated Decay.** Section 3's vendor-to-customer fragility export, at industry scale. The same frozen requirements shipping to every plant in the sector. One plant's ghost is a local problem; a vendor shipping the same dead runtime to every customer is an industry problem. The buyer can't demand modernization because the vendor has no modern product. The vendor has no modern product because no buyer will pay for the rewrite. COVID proved it at scale — when the supply chain broke, every plant reached for the same dead hardware, because the whole sector had standardized on the ghost.

Stack all four and you get the emergent risk fabric: the plant as it actually is once fossilized systems, shadow networks, and unmanaged OT/IT contact are piled together — risk that can't be patched out, only contained.

These are the cases where the ghost did the work: no zero-days required at the moment of impact, just legacy systems sitting where they shouldn't. That's not three incidents. That's one pattern with three addresses.

## 6. Impact and Mitigation

Ghost Architecture piles up security debt over decades, rots the OT/IT boundary, and turns one plant's problem into a grid problem. The same adjacency is now forming around GPU clusters and cloud-fed analytics — same doorways, new tenants.

You can't patch your way out of Ghost Architecture. You can only shrink it — and shrinking it means doing the things the last five sections just explained nobody does.

None of what follows is new. Every item below has been recommended for a decade. The reason it doesn't happen is that doing any of it breaks the process or the budget — which is the entire subject of this paper. Each one fails for a specific reason, and the reasons are the thesis:

**Pressure vendors to modernize.** The buyer has no leverage. The vendor's whole product line is built on the frozen runtime, and the one customer demanding a rewrite is bidding against ten who just want the cheap quote. Modernization happens when a vendor's largest customers move together. They never do.

**Harden the EWS baseline.** The EWS is the box everyone touches and nobody owns — IT won't manage it because it's OT, OT won't manage it because it's a PC. Hardening it means taking it away from the engineers during the outage they're working, which is exactly when they need it most.

**Segment the OT network.** Segmentation is downtime with a project plan. Every trust boundary crosses a cable somebody's process depends on, and the first time the new firewall blocks a legitimate control packet at 3:00 a.m., the rule gets an exception that never expires.

**Audit the supply chain.** The audit finds what this paper already documented: the vendor ships frozen requirements because that is the product. The audit doesn't create a modern alternative. It just prices the ghost.

**Quarantine the legacy runtimes.** Quarantine means wrapping the dead OS in enough controls that it can't hurt anything — jump hosts, one-way diodes, monitored access. It works, technically. It also costs real money every year to protect a box whose entire value is that it was already paid for.

The goal isn't to eliminate the ghosts. It's to keep them from wandering.

---

## Appendix A — Protocol Weakness Tables

Industrial protocols carry their own ghosts. Modbus was never designed for adversaries. It has no authentication, no encryption, and no concept of identity. Any device that can speak Modbus can impersonate any other device. In these environments, Modbus becomes an open command channel — commands go in without resistance because the protocol itself assumes trust.

DNP3 inherits the same assumptions. Even with secure extensions available, most deployments still run the legacy version because upgrading requires rewriting SCADA logic. The protocol's trust model assumes physical isolation, an assumption these environments break by default.

OPC Classic is a COM/DCOM artifact from the Windows NT era. It inherits unauthenticated calls, trust-by-hostname, and brittle RPC channels. Here, OPC becomes a bridge — legacy HMIs reach deep into controllers through mechanisms modern systems can't inspect.

Vendor-locked serial protocols behave similarly. Many controllers still rely on proprietary serial formats that assume physical access equals trust. When serial-to-Ethernet converters are added for convenience, the protocol's assumptions collapse across both domains.

## Appendix B — Documented Ghost Architecture Incidents

### Oldsmar Water Treatment Facility, Florida (February 5, 2021)

On February 5, 2021, an intruder remotely accessed the SCADA system at the water treatment plant in Oldsmar, Florida and raised the sodium hydroxide (lye) dosing setpoint from 100 parts per million to roughly 11,100 ppm — a hundredfold increase. An operator watching the screen saw the cursor moving on its own and reversed the change immediately; plant safeguards and the 24–36 hour transit time to the distribution system meant the public was never at risk. The FBI's private industry notification attributed the access to "poor password security, and an outdated Windows 7 operating system," adding that the intruder "likely" used TeamViewer. A state advisory added the sharper details: the plant's computers ran 32-bit Windows 7, shared a single TeamViewer password across operators, and appeared to be connected directly to the internet with no firewall installed.

**Why it fits:** the fossilized OS, the abandoned remote-access tool, the absent firewall — none of it was a compromise of a defended system. It was the architecture itself, built for operator convenience across years of deferred modernization, sitting on the internet. The ghost wasn't hiding. It had the equivalent of a public IP.

**Sources:**
- https://www.tampabay28.com/news/local-news/i-team-investigates/fbi-water-system-hack-likely-caused-by-remote-access-program-old-software-and-poor-password-security
- https://www.techtarget.com/cybersecurity/news/252496259/Oldsmar-water-plant-computers-shared-TeamViewer-password
- https://www.lexology.com/library/detail.aspx?g=883c74f0-87ff-43b7-8a06-d11c31fd4349

### Ukraine Power Grid Attacks (December 2015 and December 2016)

**December 23, 2015.** After roughly six months inside the networks via spear-phished BlackEnergy implants, attackers used the operators' own stolen VPN and remote-desktop credentials to open breakers at about 30 substations across three regional utilities. Roughly 230,000 customers lost power for one to six hours. Then KillDisk wipers bricked the operator workstations, and a telephone denial-of-service attack flooded customer call centers to slow recovery. The first publicly confirmed cyberattack to black out a civilian power grid.

**December 17, 2016.** The Pivnichna transmission substation near Kyiv went dark for about an hour. The cause was Industroyer (also called CrashOverride) — the first malware built to speak grid protocols natively: IEC 60870-5-101/104, IEC 61850, OPC DA. No operator in the loop; a relay-bypass component blocked automatic reclosure. Dragos later assessed the design intent included physical damage that could have stretched the outage to weeks.

**Why they fit:** 2015 is the convenience-pathway attack in pure form — the weapon was the operators' own remote access, and the legacy architecture couldn't tell a legitimate session from a hostile one. 2016 removed the human entirely: malware speaking the native tongue of a control layer that never learned a new one.

**Sources:**
- https://www.congress.gov/crs_external_products/R/PDF/R48067/R48067.12.pdf
- https://en.wikipedia.org/wiki/2015_Ukraine_power_grid_hack
- https://www.darkreading.com/threat-intelligence/first-malware-designed-solely-for-electric-grids-caused-2016-ukraine-outage

### TRITON/Trisis — Schneider Electric Triconex Safety System Attack (2017)

In the summer of 2017, a Saudi petrochemical plant tripped into an unplanned safety shutdown. Investigators found TRITON (FireEye's name; Dragos called it TRISIS, ICS-CERT HatMan) — the first malware ever built to target Safety Instrumented Systems. It went after Schneider Electric Triconex SIS controllers: the last line of defense, whose entire job is shutting the plant down before a process excursion becomes an explosion or a toxic release. The attackers had reverse-engineered Schneider's proprietary, undocumented TriStation protocol, exploited a zero-day in the Triconex firmware, and implanted code capable of reading and rewriting the safety logic. They were caught only because their own code faulted and tripped the controller into fail-safe — the safety system doing its job against the people trying to neuter it. Two enabling details: the controllers ran a firmware version carrying the flaw, and the physical key-switch sat in PROGRAM mode — the maintenance position — during steady-state operation. In 2020 the U.S. attributed the operation to TsNIIKhM, a Russian state research institute, and sanctioned it.

**Why it fits:** a safety controller is supposed to outlive everything — frozen logic is its design, not its decay. TRITON's authors attacked the frozen layer itself, through a vendor-proprietary protocol never documented, audited, or replaced. The key-switch in PROGRAM mode is the whole thesis in miniature: a convenience position, left engaged, on the last line of defense.

**Sources:**
- https://WWW.IC3.GOV/CSA/2022/220325-2.pdf
- https://www.technologyreview.com/2019/03/05/103328/cybersecurity-critical-infrastructure-triton-malware/
- https://icscsi.org/library/Documents/Cyber_Events/Nozomi%20-%20TRITON%20-%20The%20First%20SIS%20Cyberattack.pdf

## Appendix C — OT Incident Response Reality Checklist

Incident response teams cannot patch legacy controllers, modernize vendor-locked HMIs, or rewrite process logic. Their role is containment, not correction.

Operators must stabilize the physical process before IR can act. This means verifying setpoints, checking interlocks, confirming controller states, and ensuring equipment is not in a runaway condition. These environments hide failures behind frozen HMIs and outdated runtimes, so physical verification becomes mandatory.

Before digital triage occurs, the plant must confirm valves are in expected positions, pumps are not cycling abnormally, controllers are not in fallback modes, and HMIs are showing live data rather than stale screens. Modern IR playbooks fail because they assume modern systems. This one requires a different doctrine entirely.

## Appendix D — Glossary

- **Ghost Architecture** — Obsolete OT systems and legacy software that persist because the process breaks without them.
- **Fossilized System** — A legacy machine or software component that remains operational long past its intended lifespan because upgrading it would break the industrial workflow.
- **EWS** — Engineering Workstation. The PC used to configure, program, and maintain controllers, HMIs, and safety systems. Sits at the seam between OT and IT, usually with one foot in each network.
- **Temporal Fragmentation** — One industrial environment running decades of incompatible technology at once: 2001 logic next to a 2026 network.
- **Spectral Adjacency** — Unmanaged contact between OT and IT environments — the dual-homed EWS, the contractor laptop, the vendor VPN nobody closed. Contact everyone can see and nobody owns.
- **Shadow Network** — Forgotten VLANs, abandoned switches, flat segments, and undocumented pathways that persist because removing them risks breaking the industrial process.
- **Propagated Decay** — Fragility exported across an industry: buyers who can't or won't pay for modernization keep buying what vendors keep shipping, so the same frozen requirements land at every plant in the sector.
- **Emergent Risk Fabric** — What the plant actually is once fossilized systems, shadow networks, and unmanaged OT/IT contact are stacked together: risk you can't patch out, only contain.
- **Convenience Architecture** — Informal, undocumented network pathways created because operators need fast access. The mechanism by which spectral adjacency forms.

---

*This is Paper 03 of 3. [Paper 01 — The Bonus Loop](01-the-bonus-loop.md) · [Paper 02 — The Drift Machine](02-the-drift-machine.md)*
