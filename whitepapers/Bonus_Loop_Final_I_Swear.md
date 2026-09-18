# Disclaimer — This Work Is a Warning, Not an Attack
***These papers are issued as operational warnings, not accusations or attacks. Their purpose is to highlight systemic drift, incentive-driven vulnerabilities, and structural blind spots that increase OT cyber risk. Nothing in these documents is intended to criticize personnel, departments, vendors, or plant leadership.
The analysis focuses on system behavior, organizational incentives, and infrastructure realities, not individual fault. These supplements should be understood as risk advisories, not hostile critiques.***

# The Bonus Loop
## How Financial Incentives Engineer Industrial Drift
## 1. Introduction: The Drift
A brand-new industrial facility has a smell — ozone, fresh paint, shrink-wrap off-gassing from machines that haven't run anything but commissioning tests. The lighting is bright and even. Motors hum with that steady, confident resonance you only get when everything is new and aligned. The place feels engineered.

Five years later, the shine is gone. A third of the high-bays flicker or sit dead. Temporary data drops snake overhead. Extension cords become permanent infrastructure. Low spots in the floor collect oil skinned water that never fully dries.

Ten years in, the temporary has become structural. Patch cables and control wires form rat's nests behind control panels. Ghost machines and skeletal racks sit dead in the line because removing them costs more than simply ignoring them. Masking-tape labels fade into illegibility. Safety interlocks jumpered during a third-shift emergency remain bypassed for years. Entire sub-panels sit untouched because no one wants to throw the main disconnect and discover what dies.

In the utility corridor, a load-bearing concrete wall has a three-foot crater punched straight through it — a crew needed to run industrial Ethernet and didn't want to drill a proper sleeved penetration.

**The facility isn't failing.**

**It's drifting.**

And the drift isn't mysterious. It's engineered — not by the people turning wrenches, but by the bonus loop.

### 1.1 Industrial Decay Is an Incentive Problem
Industrial decay is not a maintenance problem, a training problem, or a cybersecurity problem. It is an incentive problem.

When leadership is rewarded for short-term optics instead of long-term reliability, the plant drifts — physically, culturally, and digitally — until the system becomes unmanageable.

The mechanism that makes this drift inevitable is the Rotating GM Loop.

## 2. The Mechanics of Decay: The Rotating GM Loop
The bonus structure reduces plant management to a brutal binary equation:

**Spend money → lose bonus.**

**Don't spend money → keep bonus.**

This equation becomes catastrophic when combined with the natural lifecycle of a plant and the career lifecycle of its leadership. Over a decade, the facility passes through three predictable acts.

### Act I: The New Plant (GM One)
GM One arrives at a pristine facility. No backlog. No aging infrastructure. No expensive repairs. Overhead is minimal. The numbers look perfect. GM One collects a large bonus and rotates upward.

This is the only GM who ever sees the plant in its engineered state.

### Act II: The Aging Plant (GM Two)
GM Two inherits a facility beginning to show wear. Real maintenance now requires capital and downtime. But downtime triggers regional scrutiny, and scrutiny kills bonuses.

GM Two learns the unwritten rule: push repairs into the next quarter, keep the line running, protect the bonus, rotate out.

**This is where drift begins.**

### Act III: The Wreckage (GM Three)
GM Three inherits a plant held together by zip ties, scavenged parts, and improvisation. Deferred work orders have become structural failures. They must spend money, shut things down, and fix the rot just to keep product moving.

The moment they spend capital, the scoreboard tanks. When the scoreboard tanks, GM Three is rotated out.

**The Loop Resets**

A new GM arrives. The plant is "new" again — because the last GM finally spent the money. The cycle restarts.

**The drift is baked into the leadership rotation itself.**

*While severe market downturn can create triage, this paper is not about a single emergency  quarter or fiscal year. It describes a predictable and chronic systematic cycle.* 

*When survival forces defer maintenance and upgrading plant technology, leadership communicates it honestly as an emergency. When it is driven by the bonus loop, leadership will mask ot with "green" performance optics until the asset inevitably fails. That said it is not unheard of for leadership to be unable to do the right thing as they are genuinely trapped inside poorly designed corporate structures or hyper-competitive market pressures they cannot rewrite.*

### 2.1 What Breaks the Loop
The loop isn't inevitable. It's contingent on one specific condition: nobody sticking around long enough to remember why the last GM did what they 
did.

I watched a private equity acquisition break that pattern once, by accident more than design. Private equity isn't inherently the villain here — the incentive structures it creates just tend to reward exactly the wrong behavior in practice. In this case, the new ownership installed a new CEO, but the board kept the existing CFO in place rather than clearing him out with everyone else. The new CEO, from what I could tell, wasn't particularly engaged in the day-to-day — by all appearances, checked out. But the CFO was the one who actually remembered what had been deferred, and why, and at what cost, and he was still in the room for the next round of decisions. There was no incoming leadership team who could plausibly claim the wreckage wasn't theirs to own, because the person who'd tracked the deferred maintenance bill the whole way was still sitting at the table.

Institutional memory is the actual thing the loop depends on erasing — and it doesn't require a functioning CEO to survive. It just requires one person who was there when the bill started running up, still being there when it comes due. A rotating GM isn't dangerous because they're a bad leader — they're dangerous because they're structurally incapable of being held accountable for decay they didn't personally cause and won't personally inherit the consequences of. Keep the one person who remembers, and that 
structural excuse disappears.

This is worth stating plainly, because most of the drift literature — including the rest of this paper — treats private equity as a uniform villain. It isn't. However, the scavenger phase described below is what happens when PE ownership pairs frozen capital with no institutional memory. What happened here is what happens when PE ownership pairs the same cost discipline with continuity instead. Same financial pressure. Very different outcome. The variable isn't who owns the plant. It's who remembers what was deferred, and whether they're still around to answer for it.

### 2.2 The Scavenger Phase
When private equity owners or strict cost-cutting regimes freeze purchase orders entirely, the plant drops out of the GM loop and into something worse: the scavenger phase.

**Broken equipment is not repaired — it is harvested.**

Technicians strip dead machines for motors, bolts, and wire. They fabricate crude cams out of scrap steel because ordering proper OEM components requires a signature that will never come. Crews raid decommissioned boiler buildings and abandoned parts of the plant floor for legacy controls.

Scavenging is not incompetence. It is rational behavior in a system where proper repair is financially punished.
And scavenging extends directly into the plant's digital infrastructure.

When an unmanaged switch fails, a hardened industrial replacement is rejected. Techs pull consumer-grade desktop switches out of abandoned offices, snip Ethernet cables from old PCs, and tape mystery Wi-Fi routers inside active enclosures. Or even, in some cases, a trip to ebay with a fist-full of their own cash.

Every scavenged device injects unpatched operating systems, unknown MAC addresses, and open ports straight into the OT environment.

The GM loop doesn't just create physical rot — it creates both digital rot and trust erosion.

### 2.3 The Scavanged Human
Equipment isn't the only thing that gets scavenged instead of replaced. People are too — and the mechanism is identical: it's cheaper to keep running something that already works than to invest in something that might work better.

The way it looks in practice: there's one person the field trusts completely. Techs know that if they get this person on the phone, they won't get berated for the mistake that caused the callout in the first place. This person will take a bad photo texted from a job site and turn it into a diagram anyone can actually follow. This person will sit on their own phone, on their own time, on a holiday, walking a crew through stopping a plant that's in freefall — because the alternative is a shutdown nobody wants to explain on Monday.

The job never once tested whether that person could turn a bolt. It tested whether they could hold a plant's institutional memory in their head, translate it for three different audiences at once — the tech on site, the GM on the phone, the vendor arguing about scope — and be trusted enough that people would rather call them than lie to their own manager. That's not an engineering skill. Nobody ever gave it a title, which is exactly the problem.

That person becomes infrastructure. Not a role. A load-bearing piece of the operation, same as a legacy PLC nobody can replace — except a PLC doesn't notice it's been priced out of its own advancement.

This has a name in the risk-management literature: key person risk, sometimes called key-man risk. It's considered one of the harder categories of risk to manage precisely because it doesn't show up on a balance sheet until the person is already gone — the industry writes entire playbooks about mitigating this risk at the executive level — succession plans, key-person insurance, cross-training, deferred compensation designed specifically to keep someone from walking. None of that machinery exists for the field-level version of the same risk. Nobody buys key-person insurance on the guy techs actually trust.

Here's what the loop actually pays for that kind of reliability: when the moment finally comes to ask for something back — the answer isn't no. It's worse than no. It's "I guess we have to think about your career trajectory," Years of work, and the company had never once gotten around to considering where it was supposed to lead.

The cost is real. And that kind of cost doesn't get asked about in an exit interview. At the end of the day, the employee leaves, the process falters and the likley-hood of the story being repeated to employment candidates researching a company is all but assured. 

The GM loop resets because a new GM arrives to a plant that looks new again. The human version doesn't reset the same way. There's no incoming replacement who gets a clean slate — the position just keeps failing to hold anyone the way it held the last person. That's not a coincidence. It's the same math, but wearing a name tag.

### 2.4 The Employee as Balance Sheet
There's a smaller, quieter version of this loop that doesn't require a bonus structure, a private equity owner, or a rotating GM. It just requires an expense report.

Field work runs on emergencies, and emergencies don't wait for a purchase order. A part has to ship overnight. A hotel has to be booked tonight, not after a three-day approval cycle. A tool has to be bought at the hardware store an hour from the plant because the one in the truck broke. In the moment, there's only one practical way to keep the job moving: the person on site pays for it. 

Look at what that arrangement actually assigns, and to whom. The employee supplies the capital — their own money, on their own card, sometimes running into thousands of dollars before a single dollar comes back. The employee assumes the risk — if a receipt doesn't survive an accounting policy nobody explained to them in advance, or gets lost somewhere between a job site and a back office, the loss lands on the person who can least afford to eat it, not the company that can. And the employee supplies the labor twice over — once doing the actual work, and again doing the unpaid administrative work of documenting, submitting, and chasing down their own reimbursement, sometimes for months.

Capital, risk, and labor, all supplied by the employee. The employer keeps the money until it's forced to let go of it, keeps the float that money represents, and keeps the built-in option to simply deny the claim if a receipt doesn't meet a standard it never bothered to communicate. Call it whatever the accounting department calls it — an interest-free loan is the polite version. What it actually is: the cost of doing business, quietly reassigned to the person with the least power to refuse it.

None of this requires anyone to have designed it maliciously. Nobody sits in a boardroom and decides to finance operations off their field staff's personal credit cards. Expense controls exist for a real reason — fraud is expensive, and receipts are how a company protects itself from being billed for things that never happened. The problem isn't that the controls exist. It's that when the process fails — a lost receipt, an ambiguous policy, a rejected claim — the loss defaults to the employee, every time, instead of being treated as a shared cost of doing business the same way a bad debt or a write-off would be.

Strip away the accounting language and there's one resource actually being spent here, and it isn't cash. It's trust. The employee has to trust the claim will be approved, trust the receipt won't get lost, trust that "we'll make it right" means what it sounds like — with no collateral, no enforcement mechanism, and no recourse if any of that trust turns out to be misplaced. A real lender can report a default, send collections, or sue. An employee who fronted the money has none of that leverage against the employer. The arrangement doesn't just extract capital and risk. It extracts trust, and it does so precisely because trust is the one thing that doesn't show up as a line item anywhere.

### 2.5 The Contractor's Loop
Everything so far has been about incentives inside a company — a GM protecting a bonus, an employee absorbing float. There's a mirror version of the same failure that runs the other direction, through the outside vendors and subcontractors a plant depends on to get anything built or fixed at all. Same disease. Opposite vector.

I've worked both sides of that relationship. Some vendors earned the trust they were given — reliable, straightforward, the kind of partner who actually wanted the job to end because a finished job is what gets you the next one. Others treated the contract itself as the product. I worked under one subcontractor whose paperwork was built to manufacture scope creep and penalize the honest billing of it at the same time — language buried in the contract that pushed work outside the agreed scope while separately penalizing time-and-materials billing for exactly that overrun. The practical effect was a project that never actually finished, because finishing was never the profitable outcome. We kept paying, on paper, for a job that was structurally designed not to conclude.

That's the GM Loop's mirror image. A GM defers cost because their bonus rewards deferral. A predatory contractor manufactures cost because their revenue rewards continuation. Different direction, same underlying failure: somebody's compensation is tied to an outcome that has nothing to do with the plant actually working, and the contract — like the bonus formula — quietly optimizes for that instead.

It's also a reminder that the incentive problem this paper describes isn't unique to leadership, or to private equity, or to any one seat in the org chart. Wherever a contract, a bonus, or a billing structure rewards something other than the plant's actual reliability, the plant will eventually get exactly what it's paying for — which is never what it thinks it's paying for.

## 3. The Cultural Shift
The cultural erosion mirrors the GM cycle:

**"Fix it right." → "Fix it cheap." → "Fix it later." → "Don't fix it at all."**

Culture doesn't collapse all at once — it erodes one shortcut at a time.

Safety interlocks become "temporary bypasses" that stretch across years. Rigged machine guards remain in place purely for show. The building becomes a physical record of leadership incentives: color shifts on walls, widespread lighting decay, infrastructure scars, and tangled patch-cable nests.

## 4. Why Policy, Training, and Cybersecurity Fail
Corporate headquarters typically responds to decay with new policies, mandatory training modules, or heavy-handed cybersecurity frameworks. All three fail for the same reason: they're aimed at symptoms, and the disease is upstream of all of them.
Policy has no teeth in a plant like this, because policy only matters when leadership actually wants it enforced — and leadership here is being paid to protect a number. 

Training misdiagnoses the problem entirely; the technicians already know the correct way to do the job, they just also know that doing it correctly, on the clock, violates the unwritten rules of the budget they're actually being measured against. And cybersecurity frameworks assume a stable, predictable environment to secure in the first place — an assumption that quietly falls apart the moment configurations change on the fly and the documentation stops resembling the plant it's supposed to describe. You can't harden a system whose actual shape bares no resemblance to the one on paper.

## 5. The Cybersecurity Implications of a Decaying Plant
Operational Technology (OT) cybersecurity is fundamentally a physical reliability discipline. You cannot secure a digital network in a plant that cannot secure its own physical foundation.

Rot destroys baselines. Scavenged wiring and mystery switches erase the answer to the most fundamental security question: what is actually plugged into the network?

Improvisation creates shadow systems. Rogue patch cables, duct-taped desktop switches, scavenged routers, undocumented PLC logic branches, and donor controllers create invisible infrastructure attackers love.

Documentation becomes fictional. Prints and network maps no longer match reality. Incident response becomes guesswork.

Hero techs break cyber hygiene. Midnight fixes introduce unverified wiring shifts, unauthorized reroutes, and unmanaged patches. Every hero fix creates a blind spot.

Fear suppresses reporting. Workers ignore anomalies to avoid stopping the line. A line down brings scrutiny. scrutiny assigns blame. Fix it quickly then the bypass is forgotten. Silence is an attacker's best friend.

Cyber-physical cascades follow. In a decaying plant, everything is already hanging by a thread. A minor malicious logic tweak or a sensor spoof can trigger catastrophic physical destruction.

Cyber instability is never the root cause it is the final symptom of physical neglect.

## 6. The Incentive Reset
You cannot hope fix decay by adding rules. You fix it by rewriting the incentives.

Link maintenance to sales. Maintenance is throughput protection. Healthy equipment produces more sellable units per hour.

Fund reliability. End the scavenger economy — mechanical, digital, and human — by funding OEM parts, stocking critical spares, replacing scavenged switches with hardened industrial hardware, and building a real advancement path for the people who are quietly holding the operation together. A region, a title, a raise — whatever the actual ask is — costs less than what it takes to replace that person once they finally leave, and far less than what it costs to keep them until they break.

Stop financing operations off employees' personal capital. Issue an auditable company payment method for field expenses, or pay something close to an unsecured lending rate on unavoidable personal outlays. Keep the fraud controls. Stop defaulting the loss to whoever's holding the receipt.

Restore documentation. Accurate documentation is the blueprint of physical and digital reality.
End fear as a management tool. Stopping the line to do the job correctly must be expected, supported, and rewarded.

Make decay unacceptable. Flickering lights, oily floors, bypassed interlocks, and duct-taped switches must become unacceptable from shop floor to corner office.

## 7. Conclusion
A bonus-driven plant is not just inefficient — it is dangerous. It builds its own cyber-physical kill chain one deferred repair at a time. The only question is when it snaps.
When executive incentives reward long-term reliability over quarterly margin games, the rot reverses itself.
You cannot patch a firewall when the physical wall has a hole blown through it.

Look closely at every failure mode in this series and it's the same resource running out each time, just wearing a different tag. A field tech trusts the diagram matches the real network. An operator trusts the HMI is showing the truth. A GM trusts the deferred maintenance won't catch up on their rotation. An employee trusts the receipt gets approved. Drift isn't really entropy, and it isn't really neglect. It's trust extended past the point where anything is actually verifying it was warranted — and a system that keeps spending trust without ever replenishing it is running the exact same overdraft as a plant that keeps deferring maintenance it never intends to pay for.

## Appendices
### Appendix A — Documented Incentive-Driven Failures
These aren't cyber incidents. They're the mechanism this paper describes, playing out in the real world at a scale big enough to make the news — proof that the bonus loop isn't a rhetorical device, it's a documented pattern across industries that have nothing else in common.

**PG&E and the Wildfires (2015–2019)**
PG&E paid its top five executives roughly $17 million in safety-linked bonuses between 2012 and 2017 — including a payout in 2015, the year of the Butte Fire, which killed two people and was later tied to poorly maintained equipment. State regulators identified a years-long pattern of deferred vegetation and equipment maintenance that culminated in the 2018 Camp Fire, the deadliest wildfire in California history, killing 85 people. A federal bankruptcy judge later rejected a proposed $16 million executive incentive plan, stating there was "no justification for diverting additional estate funds to incentivize them to do what they should already be doing."

### NBC News investigation:
https://www.nbcnews.com/business/corporations/pacific-gas-electric-execs-got-big-bonuses-meeting-safety-goals-n1102681

### Bankruptcy Court bonus rejection:
https://dev.abi.org/node/279424

### Boeing 737 MAX (2018–2024)
The House Transportation Committee's 238-page investigation into the two fatal 737 MAX crashes found "tremendous financial pressure" to compete with Airbus led Boeing to cut costs and protect the production schedule at the expense of engineering scrutiny — including the flawed MCAS system implicated in both crashes. A 2024 internal Boeing survey, obtained after the Alaska Airlines door-plug incident, found only 47% of employees agreed that "schedule pressures do not cause my team to lower our standards" — evidence the incentive structure hadn't meaningfully changed even after 346 deaths and years of scrutiny.

### House Committee final report: 
https://democrats-transportation.house.gov/news/press-releases/after-18-month-investigation-chairs-defazio-and-larsen-release-final-committee-report-on-boeing-737-max

### Senate PSI 2024 findings: 
https://www.blumenthal.senate.gov/newsroom/press/release/senate-permanent-subcommittee-on-investigations-releases-new-details-of-boeings-safety-failures-ahead-of-hearing-with-faa-administrator

### Norfolk Southern / East Palestine, Ohio (2023)
The NTSB's investigation into the East Palestine derailment found an overheating wheel bearing wasn't caught before failure, in an industry where "Precision Scheduled Railroading" had cut roughly a third of the workforce over the prior decade and compressed railcar inspections to under two minutes per car. The specific car that derailed had sat stationary for months at a time — bearings degrade faster sitting still than running — and was never re-inspected across the multiple railyards it passed through before the crash. This is Section 2.2's scavenger phase at railroad scale: maintenance treated as a cost to be minimized rather than a function to be funded.

### NTSB hearing coverage:
https://www.wvxu.org/2023-06-24/ntsb-east-palestine-hearings-highlight-norfolk-southerns-safety-culture

### Congressional hearing on inspection cuts: 
https://www.fortune.com/2024/07/24/hearing-norfolk-southern-derailment-ohio-rushed-inspections-job-cuts

### Key Person Risk (ongoing, documented pattern)
Risk-management and HR literature treats the loss of an irreplaceable individual as a distinct, hard-to-mitigate risk category — the field-level version of what Section 2.3 calls the scavanged human. A 2018 Morgan Stanley Research analysis found S&P 500 companies that lost a key executive underperformed the market by an average of 11% in the following year.

### FM Magazine coverage of the Morgan Stanley findings: 
https://www.fm-magazine.com/news/2019/jan/how-to-manage-key-person-risk-201819925/

### Appendix B — The Math of the Loop
The bonus loop isn't a metaphor. It's arithmetic, and it rewards exactly the behavior this paper describes.

Say a GM's annual bonus is calculated as 40% base salary, weighted 60% on plant uptime/output and 40% on capital spend staying under budget. A GM facing $2M in deferred maintenance has two options:

Spend it. Uptime dips during the work. Capex blows the budget line. Bonus for the year: minimal, maybe zero.
Defer it. Uptime holds. Budget line stays green. Bonus for the year: near-maximum.

Multiply by a typical 2–4 year rotation before promotion or transfer, and deferring is the only individually rational choice — the GM captures the full bonus upside and is gone before the deferred cost compounds into a forced shutdown. The next GM inherits the bill. This is a well-known category of problem in economics — a principal-agent problem, where the agent's incentives (the GM's bonus, tied to a short tenure) diverge from the principal's actual interest (the company's, over the life of the asset) — dressed up here as a maintenance schedule.

The fix isn't a bigger stick. It's changing what the formula rewards: multi-year vesting tied to asset condition at handoff, not just performance during tenure, closes the loop instead of resetting it with every rotation.

### Appendix C — Glossary of Financial  Incentives 
**Capex / Opex** — Capital expenditure (a major, often depreciated purchase — new equipment, a rebuild) versus operating expenditure (routine, expensed costs — parts, labor, utilities). Deferred maintenance frequently means deferred capex specifically, since large fixes get classified as capital projects requiring separate approval that a GM's discretionary budget doesn't cover.

**EBITDA** — Earnings before interest, taxes, depreciation, and amortization. A common basis for executive bonus formulas precisely because it excludes the capital spending that would otherwise show the cost of deferred maintenance.

**NCF (National Critical Function)** — A CISA designation for functions so vital that their disruption would degrade national security, economic security, or public health — many industrial and utility operations qualify.

**Clawback** — A contractual provision letting a company reclaim already-paid bonus compensation if it's later found to have been based on false, fraudulent, or since-reversed performance metrics. Rare in practice, and essentially never triggered by "the plant fell apart three years after I left."

**Rotation / GM rotation** — The corporate practice of moving general managers or plant leadership between facilities on a fixed cycle, ostensibly for development and cross-pollination — but which, absent asset-condition accountability, also has the side effect this paper describes.

**Roll-up** — A private-equity strategy of acquiring multiple smaller companies in the same industry and merging them, typically financed with debt and optimized for near-term cash flow to service that debt — the conditions under which Section 2.2's "scavenger phase" is most likely to appear.

**Throughput** — The rate at which a process or line actually produces sellable output, as distinct from uptime (which only measures whether the line is running, not how well).

### Appendix D — Field Signs of a Plant in the Loop
None of these prove which act a plant is in on their own. Together, they're a reasonably reliable read — useful for anyone touring a facility without access to its P&L.

*Lighting that flickers or has visibly mismatched replacement fixtures across different sections of the same floor*

*Extension cords or temporary cable runs that have clearly been in place for years, not weeks*

*Visible physical damage (wall penetrations, structural cuts) that were never properly finished or sleeved*

*Masking-tape or handwritten labels replacing manufacturer nameplates or proper engraved labels*

*Safety interlocks, guards, or e-stops that are visibly bypassed, taped over, or jumpered*

*Maintenance staff who can immediately point out "the bad one" — a specific problem machine everyone already knows about and works around*

*A parts room or cabinet full of components that don't match any current equipment on the floor — evidence of a prior scavenging phase*

*Network diagrams or as-built drawings that staff themselves describe as "not accurate anymore" without being asked*
