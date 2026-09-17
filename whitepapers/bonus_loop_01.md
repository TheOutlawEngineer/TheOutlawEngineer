# Disclaimer — This Work Is a Warning, Not an Attack
***These papers are issued as operational warnings, not accusations or attacks. Their purpose is to highlight systemic drift, incentive-driven vulnerabilities, and structural blind spots that increase OT cyber risk. Nothing in these documents is intended to criticize personnel, departments, vendors, or plant leadership.***

***The analysis focuses on system behavior, organizational incentives, and infrastructure realities, not individual fault. These supplements should be understood as risk advisories, not hostile critiques.***

Now it's time to be in the loop:

# The Bonus Loop
## How Leadership Incentives Engineer Industrial Drift

## 1. Introduction: The Drift
A brand-new industrial facility has a smell — ozone, fresh paint, shrink-wrap off-gassing from machines that haven't run anything but commissioning tests. The lighting is bright and even. Motors hum with that steady, confident resonance you only get when everything is new and aligned. The place feels engineered.

Five years later, the shine is gone. A third of the high-bays flicker or sit dead. Temporary data drops snake overhead. Extension cords become permanent infrastructure. Low spots in the floor collect oil skinned water that never fully dries.

Ten years in, the temporary has become structural. Patch cables form rat's nests behind control panels. Skeletal machines and racks sit dead in the line because removing them costs more than ignoring them. Masking-tape labels fade into illegibility. Safety interlocks jumpered during a third-shift emergency remain bypassed for years. Entire sub-panels sit untouched because no one wants to throw the main disconnect and discover what dies.

In the utility corridor, a load-bearing concrete wall has a three-foot crater punched straight through it — a crew needed to run industrial Ethernet and didn't want to drill a proper sleeved penetration.

The facility isn't failing.

It's drifting.

And the drift isn't mysterious. It's engineered — not by the people turning wrenches, but by the bonus loop.

## 1.1 Industrial Decay Is an Incentive Problem

Industrial decay is not a maintenance problem, a training problem, or a cybersecurity problem. It is an incentive problem.

When leadership is rewarded for short-term optics instead of long-term reliability, the plant drifts — physically, culturally, and digitally — until the system becomes unmanageable.

The mechanism that makes this drift inevitable is the Rotating GM Loop.

## 2. The Mechanics of Decay: The Rotating GM Loop

The bonus structure reduces plant management to a brutal binary equation:

**Spend money → lose bonus.**
**Don't spend money → keep bonus.**

This equation becomes catastrophic when combined with the natural lifecycle of a plant and the career lifecycle of its leadership. Over a decade, the facility passes through three predictable acts.

**Act I: The New Plant (GM One)**
GM One arrives at a pristine facility. No backlog. No aging infrastructure. No expensive repairs. Overhead is minimal. The numbers look perfect. GM One collects a large bonus and rotates upward.

This is the only GM who ever sees the plant in its intended engineered state.

**Act II: The Aging Plant (GM Two)**
GM Two inherits a facility beginning to show wear. Real maintenance now requires capital and downtime. But downtime triggers regional scrutiny, and scrutiny kills bonuses.

GM Two learns the unwritten rule: push repairs into the next quarter, keep the line running, protect the bonus, rotate out.

This is where drift begins.

**Act III: The Wreckage (GM Three)**
GM Three inherits a plant held together by scavenged parts and improvisation. Deferred work orders have become structural failures. They must spend money, shut things down, and fix the rot just to keep product moving.

The moment they spend capital, the scoreboard tanks. When the scoreboard tanks, GM Three is rotated out.

The Loop Resets

A new GM arrives. The plant is "new" again — because the last GM finally spent the money. The cycle restarts.
The drift is baked into the leadership rotation itself.

**2.1 The Scavenger Phase**
When private equity owners or strict cost-cutting regimes freeze purchase orders entirely, the plant drops out of the GM loop and into something worse: the scavenger phase.

Broken equipment is not repaired — it is harvested.

Technicians strip dead machines for motors, bolts, wire and controls. They fabricate crude cams out of scrap steel because ordering proper OEM components requires a signature that will never come. Crews raid decommissioned boiler buildings and abandoned  sections of the plant for legacy pneumatic controls.

Scavenging is not incompetence. It is rational behavior in a system where proper repair is financially punished.

And scavenging extends directly into the plant's digital infrastructure.

When an unmanaged switch fails, a hardened industrial replacement is rejected. Techs pull consumer-grade desktop switches out of abandoned offices, snip Ethernet cables from old PCs,  tape mystery Wi-Fi routers inside active enclosures, or make a run to Microcenter with a fist-full of their own cash.

Every scavenged device injects unpatched operating systems, unknown MAC addresses, and open ports straight into the OT environment.

The GM loop doesn't just create physical rot — it creates digital rot.

## 3. The Cultural Shift
The cultural erosion mirrors the GM cycle:
**"Fix it right." → "Fix it cheap." → "Fix it later." → "Don't fix it at all."**

Culture doesn't collapse all at once — it erodes one justified shortcut at a time.

Safety interlocks become "temporary bypasses" that stretch across years. Rigged machine guards remain in place purely for show. The building becomes a physical record of leadership incentives: color shifts on walls, widespread lighting decay, infrastructure scars, and tangled patch-cable nests.

## 4. Why Policy, Training, and Cybersecurity Fail
Corporate headquarters typically responds to decay with new policies, mandatory training modules, or heavy-handed cybersecurity frameworks. All three fail because they treat symptoms, not incentives.

Policy has no teeth. Policies only matter when leadership wants them enforced, and in a bonus-driven plant, leadership wants short-term numbers, not compliance.

Training misdiagnoses the problem. Technicians already know the correct procedures — they improvise because uptime is king, and doing the job correctly violates the unwritten rules of the budget.

Cybersecurity assumes stability. Cyber frameworks require a stable, predictable environment. They cannot function in a plant where configurations change on the fly and documentation bears no resemblance to physical reality.

## 5. The Cybersecurity Implications of a Decaying Plant
Operational Technology (OT) cybersecurity is fundamentally a physical reliability discipline. You cannot secure a digital network in a plant that cannot secure its own physical foundation.

Rot destroys baselines. Scavenged wiring and mystery switches erase the answer to the most fundamental security question: what is actually plugged into the network?

Improvisation creates shadow systems. Rogue patch cables, duct-taped desktop switches, scavenged routers, undocumented PLC logic branches, and donor controllers create invisible infrastructure attackers love.

Documentation is fiction. Blueprints, P&ID and network maps no longer match reality. Incident response is reduced to absolute guesswork.

Hero techs break cyber hygiene.

Midnight fixes introduce unverified wiring shifts, unauthorized reroutes, and unmanaged patches. Every hero fix creates a blind spot.

Fear suppresses reporting. Workers ignore anomalies to avoid stopping the line. Silence is an attacker's best friend.

Cyber-physical cascades follow. In a decaying plant, everything is already hanging by a thread. A minor malicious logic tweak or sensor spoof can trigger catastrophic physical destruction.

Cyber instability is never the root cause — it is the final symptom of physical neglect.

## 6. The Incentive Reset
**You do not fix decay by adding rules. You fix it by rewriting incentives.**

Link maintenance to sales. Maintenance is throughput protection. Healthy equipment produces more sellable units per hour.

Fund reliability. End the scavenger economy — mechanical and digital — by funding OEM parts, stocking critical spares, and replacing scavenged switches with hardened industrial hardware.

Restore documentation. Accurate documentation is the blueprint of physical and digital reality.
End fear as a management tool. Stopping the line to do the job correctly must be expected, supported, and rewarded.

Make decay unacceptable. Flickering lights, oily floors, bypassed interlocks, and duct-taped switches must become unacceptable from shop floor to corner office.

## 7. Conclusion
A bonus-driven plant is not just inefficient — it is dangerous. It builds its own cyber-physical kill chain one deferred repair at a time. The only question is when it finally snaps.

When executive incentives reward long-term reliability over quarterly margin games, the rot reverses itself.
You cannot patch a firewall when the physical wall has a hole blown through it.

## Appendices

### Appendix A — Documented Incentive-Driven Failures

These aren't cyber incidents. They're the mechanism this paper describes, playing out in the real world at a scale big enough to make the news — proof that the bonus loop isn't a rhetorical device, it's a documented pattern across industries that have nothing else in common.

**PG&E and the Wildfires (2015–2019)**
PG&E paid its top five executives roughly $17 million in safety-linked bonuses between 2012 and 2017 — including a payout in 2015, the year of the Butte Fire, which killed two people and was later tied to poorly maintained equipment.

State regulators identified a years-long pattern of deferred vegetation and equipment maintenance that culminated in the 2018 Camp Fire, the deadliest wildfire in California history, killing 85 people. A federal bankruptcy judge later rejected a proposed $16 million executive incentive plan, stating there was "no justification for diverting additional estate funds to incentivize them to do what they should already be doing."

**NBC News investigation:** https://www.nbcnews.com/business/corporations/pacific-gas-electric-execs-got-big-bonuses-meeting-safety-goals-n1102681

**Bankruptcy Court bonus rejection:** https://dev.abi.org/node/279424


**Boeing 737 MAX (2018–2024)**
The House Transportation Committee's
238-page investigation into the two fatal 737 MAX crashes found "tremendous financial pressure" to compete with Airbus led Boeing to cut costs and protect the production schedule at the expense of engineering scrutiny — including the flawed MCAS system implicated in both crashes. A 2024 internal Boeing survey, obtained after the Alaska Airlines door-plug incident, found only 47% of employees agreed that "schedule pressures do not cause my team to lower our standards" — evidence the incentive structure hadn't meaningfully changed even after 346 deaths and years of scrutiny.

**House Committee final report:** https://democrats-transportation.house.gov/news/press-releases/after-18-month-investigation-chairs-defazio-and-larsen-release-final-committee-report-on-boeing-737-max

**Senate PSI 2024 findings:** https://www.blumenthal.senate.gov/newsroom/press/release/senate-permanent-subcommittee-on-investigations-releases-new-details-of-boeings-safety-failures-ahead-of-hearing-with-faa-administrator

**Norfolk Southern / East Palestine, Ohio (2023)**
The NTSB's investigation into the East Palestine derailment found an overheating wheel bearing wasn't caught before failure, in an industry where "Precision Scheduled Railroading" had cut roughly a third of the workforce over the prior decade and compressed railcar inspections to under two minutes per car. The specific car that derailed had sat stationary for months at a time — bearings degrade faster sitting still than running — and was never re-inspected across the multiple railyards it passed through before the crash. 

This is Section 2.1's scavenger phase at national scale: maintenance treated as a cost to be minimized rather than a function to be funded.

**NTSB hearing coverage:** https://www.wvxu.org/2023-06-24/ntsb-east-palestine-hearings-highlight-norfolk-southerns-safety-culture

**Congressional hearing on inspection cuts:** https://www.fortune.com/2024/07/24/hearing-norfolk-southern-derailment-ohio-rushed-inspections-job-cuts

### Appendix B — The Math of the Loop
The bonus loop isn't a metaphor. It's arithmetic, and it rewards exactly the behavior this paper describes.
Say a GM's annual bonus is calculated as 40% base salary, weighted 60% on plant uptime/output and 40% on capital spend staying under budget. A GM facing $2M in deferred maintenance has two options:

Spend it. Uptime dips during the work. Capex blows the budget line. Bonus for the year: minimal, maybe zero.

Defer it. Uptime holds. Budget line stays green. Bonus for the year: near-maximum.

Multiply by a typical 2–4 year rotation before promotion or transfer, and deferring is the only individually rational choice — the GM captures the full bonus upside and is gone before the deferred cost compounds into a forced shutdown. 

The next GM inherits the bill. This is a well-known category of problem in economics — a principal-agent problem, where the agent's incentives (the GM's bonus, tied to a short tenure) diverge from the principal's actual interest (the company's, over the life of the asset) — dressed up here as a maintenance schedule.

The fix isn't a bigger stick. It's changing what the formula rewards: multi-year vesting tied to asset condition at handoff, not just performance during tenure, closes the loop instead of resetting it with every rotation.

### Appendix C — Glossary of Related Buisness Terms and Concepts
**Capex / Opex** — Capital expenditure (a major, often depreciated purchase — new equipment, a rebuild) versus operating expenditure (routine, expensed costs — parts, labor, utilities). Deferred maintenance frequently means deferred capex specifically, since large fixes get classified as capital projects requiring separate approval that a GM's discretionary budget doesn't cover.

**EBITDA** — Earnings before interest, taxes, depreciation, and amortization. A common basis for executive bonus formulas precisely because it excludes the capital spending that would otherwise show the cost of deferred maintenance.

**NCF (National Critical Function)** — A CISA designation for functions so vital that their disruption would degrade national security, economic security, or public health — many industrial and utility operations qualify.

**Clawback** — A contractual provision letting a company reclaim already-paid bonus compensation if it's later found to have been based on false, fraudulent, or since-reversed performance metrics. Rare in practice, and essentially never triggered by "the plant fell apart three years after I left."

**Rotation / GM rotation** — The corporate practice of moving general managers or plant leadership between facilities on a fixed cycle, ostensibly for development and cross-pollination — but which, absent asset-condition accountability, also has the side effect this paper describes.

**Roll-up** — A private-equity strategy of acquiring multiple smaller companies in the same industry and merging them, typically financed with debt and optimized for near-term cash flow to service that debt — the conditions under which Section 2.1's "scavenger phase" is most likely to appear.

**Throughput** — The rate at which a process or line actually produces sellable output, as distinct from uptime (which only measures whether the line is running, not how well).

### Appendix D — Field Signs of a Plant in the Loop
None of these prove which act a plant is in on their own. Together, they're a reasonably reliable read — useful for anyone touring a facility without access to its P&L.

* Lighting that flickers or has visibly mismatched replacement fixtures across different sections of the same floor

* Extension cords or temporary cable runs that have clearly been in place for years, not weeks

* Visible physical damage (wall penetrations, structural cuts) that were never properly finished or sleeved

* Masking-tape or handwritten labels replacing manufacturer nameplates or proper engraved labels

* Safety interlocks, guards, or e-stops that are visibly bypassed, taped over, or jumpered

* Maintenance staff who can immediately point out "the bad one" — a specific problem machine everyone already knows about and works around

* A parts room or cabinet full of components that don't match any current equipment on the floor — evidence of a prior scavenging phase

* Network diagrams or as-built drawings that staff themselves describe as "not accurate anymore" without being asked
Next in The Ecology of Drift Series...

***Thank you for walking the drift with me.***

***None of this was meant to be comforting. Plants don’t offer comfort. They offer lessons, usually late, usually expensive. Drift isn’t fiction. It’s the part of the plant that no one swems to acknowledge. So thank you for paying attention.***

***If you recognized pieces of your own facility in these pages — the flickering lights, the scavenged switches, the quiet shortcuts that became permanent — then the work did what it needed to do. These documents were issued as “operational warnings, not accusations or attacks,” a way to make the invisible visible before it becomes irreversible.***

***Industrial drift is slow, silent, and entirely rational inside the bonus loop. None of this collapses overnight. It erodes one incentive at a time. And the only defense is paying attention — to the culture andto the infrastructure.***

***So thank you for paying attention.
That’s how the next crew stands a chance***
