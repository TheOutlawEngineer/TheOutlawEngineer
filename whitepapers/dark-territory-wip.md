# Dark Territory
### Rail crew reductions as attack-surface transformation — work in progress

## Opening

When I was a teenager, boredom was a kind of accelerant. Inspired by a lethal combination of curiosity, a rudimentary understanding of physics, Cannon Films, and half-remembered MacGyver episodes, my friends and I designed—designed is a strong word for what we did—built, and implemented a remote-controlled rocket platform.

It was an improvised machine cobbled together from whatever we could scavenge: a Tamiya Midnight Pumpkin RC car frame mated with an aircraft transmitter that gave us just enough channels for steering, acceleration, tube azimuth, and an ignition circuit. It's amazing what you can do with a transistor or two.

We took our creation to an unmanned highway construction site, operating under the blissful immunity of boomer parents who pretty much left us to our own devices until an authority figure got directly involved. We launched homemade warheads—black powder, brass tubes, and a primer cap stuffed into an Estes model rocket—at whatever targets looked interesting, entirely convinced we were conducting harmless scientific experimentation. The only thing that stopped our R&D phase was the booming voice of an angry man explaining that the trailer we kept narrowly missing contained high-explosive materials capable of turning our amusing afternoon into a much more eventful evening.

Sixteen years later, in Łódź, Poland, another bored teenage boy found his own unsupervised system.

Armed with scavenged electronic components and a basic understanding of how the city's tram infrastructure communicated, a 14-year-old boy built a handheld transmitter—essentially modifying a household remote control unit—capable of switching track points. He treated the municipal transit network like a giant, real-world model train set.

His curiosity wasn't driven by malice, but by the sheer thrill of interaction. Yet, because the city's track-switching signals were completely unencrypted, entirely predictable, and operating without anyone actively monitoring the vulnerability, his remote inputs actually worked. He threw the switches mid-route, resulting in multiple tram derailments, emergency stops, and several injured passengers before authorities tracked him down.

Both incidents share the exact same root cause: bored teenage boys will test any system left unattended. And when that system is public-facing, high-energy, or safety-critical, the consequences scale fast.

Remove the human engineer from the cab, and you are actively building the exact conditions that made both incidents possible.

## The history

After World War II, an American freight train commonly carried seven people: an engineer, a conductor, a fireman, and up to four brakemen. Dieselization killed the fireman's actual job — no fire to tend — but the unions kept the position on crews for decades. By the 1970s the standard crew was five: engineer, fireman, conductor, two brakemen.

The 1980s took the rest. Two-way radios and electronic end-of-train devices replaced what the caboose did — rear-end observation, air-brake monitoring — and one by one the states repealed their caboose laws. Virginia, the last holdout, relented in July 1988. Labor agreements cut crews from five to three to two: an engineer and a conductor, both riding in the locomotive cab. By 1991 the two-person crew was the American standard.

The railroads didn't stop at two. Single-person crews were the next ask, and the unions spent two decades fighting it off. In April 2024 the FRA finalized a rule requiring two crew members on nearly all freight trains — and in 2026 a federal court upheld it against a challenge from six carriers and the AAR. The rule doesn't ban single-person operation outright; it forces railroads to petition for it, with risk assessments and public comment.

So the current state: two people in the cab, by federal rule, with the industry still pushing toward one — and past one, toward none. Every step of that history replaced a person with a device. The caboose became an EOT box. The brakemen became radios and trackside detectors. The question the rest of this analysis follows is what the conductor becomes — and what replaces the engineer after that.

## Thesis

Every crew member removed from the cab gets replaced by a network connection. That's the whole analysis in one sentence.

The attack surface doesn't just grow as crews shrink. It changes kind — from physical presence to remote reachability. A crew member can only be attacked physically. A data link can be attacked from anywhere.

This is a cyber-physical analysis, not an incentive analysis. The question isn't why the industry wanted the cuts. It's what the cuts built.

## Attack-surface transformation

Crew reduction is not metaphorical. It is architectural. Every crew member removed takes a local, embodied safety function with them, and something network-reachable gets installed in its place. The change runs in three directions at once.

Local becomes remote. A human engineer is a local actor — everything they sense, decide, and do happens inside the physical cab. Take them out and you have to put the cab's functions somewhere else: remote telemetry, remote braking authority, remote throttle authority, remote routing commands, remote safety interlocks. Every one of them reachable without standing anywhere near a track.

Implicit becomes explicit. A human reads a train through the body — vision, hearing, feel, the kind of intuition that comes from ten thousand hours in the seat. A machine reads it through interfaces: APIs, serial links, IP tunnels, radio protocols, satellite uplinks. And explicit interfaces can be spoofed, jammed, replayed, or manipulated in ways a person's senses can't.

Unreachable becomes reachable. To attack a five-person crew you had to be physically there. To attack a remotely operated train you can be anywhere — behind a compromised dispatch workstation, inside a vendor's network, riding a hijacked cellular modem or satellite terminal, sitting on a maintenance laptop, living in a cloud integration nobody audits. Crew reduction doesn't just shrink the workforce. It converts physical attack surface into network attack surface, and networks are where the attackers already live.

## The mechanism

Start at five. Five people watch a train with their eyes: the hot box, the dragging strap, the misaligned switch. Cut to two, and that watching has to go somewhere — so it goes into instruments. Trackside detectors, instrumented bearings, electronic monitors. Human observation becomes instrumented observation, and the instruments report over a network. The crew is still on the train, but perception has started moving onto the wire.

Cut to one, and the remaining operator can't do the work of two — so the work goes into automation. Cab signaling, alerter systems, trip optimizers. The operator stops running the train and starts monitoring the systems that run the train. The human is still in the cab, but operation has moved into the software.

There's a second reason two matters, and it's the way the job is actually scheduled. Train crews work off the board: on call, ninety minutes to two hours to report, around the clock. There's no PTO in any normal sense — BNSF's Hi-Viz system runs on points, and being unavailable when called costs you. The law says ten hours of undisturbed rest between runs, but on-call rest isn't sleep. It's waiting to be called, at any hour, on a body clock that never settles. In that cab, the second person is the fatigue backstop: two sets of eyes when both sets are running on broken sleep. Cut to one, and the last human redundancy against exhaustion walks off with the conductor — which only deepens the dependence on the automation that's supposed to cover for him. There's only so much coffee and cigarettes or Monster and Zin can do.

Cut to zero, and the train becomes a networked endpoint. There's no one left to hand the work to except the network itself: continuous control links over cellular and satellite, centralized dispatch, automated safety overlays. None of this existed when five people ran a train by sight and radio. Every piece of it is reachable without ever standing near a track.

That's the mechanism. Each cut doesn't just remove a person — it installs a remote connection where the person was.

## Component enumeration

Name what replaced the humans and the list writes itself. The engineer's eyes became PTC radios, cellular modems, satellite terminals, and the locomotive control units that listen to them. The brakeman's walk-around became hot-box detectors, dragging-equipment detectors, wheel-impact load detectors, instrumented bearings — and the end-of-train device that replaced the caboose outright. The conductor's judgment became Trip Optimizer and LEADER, cab signaling receivers, alerter systems, automatic braking overlays, remote emergency-stop interfaces. The dispatcher's voice became remote consoles, wayside interface units, and distributed power radio links holding a two-mile train together over the air.

Every one of these is a component an attacker can reach without ever standing near a track. That's not a flaw in any single device. It's the architecture.

## Cyber-physical threat model

Start with who shows up. The opening of this analysis already introduced the first one: the bored teenager, because unattended systems get tested. After him come the disgruntled employee who knows where the bodies are buried, the opportunistic malware that doesn't care what it infects, the targeted adversary with a reason, and the supply-chain compromise that arrives pre-installed.

What they do hasn't changed in decades — only the address has. Spoofed control signals. Replayed braking commands. Falsified sensor telemetry telling dispatch everything is fine. Denial-of-service on the control links. A compromised dispatch workstation, a compromised wayside unit, a hijacked satellite link, an exploited cellular modem. Łódź was the proof of concept with a TV remote. The infrastructure since then has only gotten more connected.

What breaks: routing changes nobody ordered, switches thrown mid-route, brakes that don't answer, throttles with a mind of their own, "safe" indications on a screen while the physical world disagrees. And because dispatch is centralized, failures cascade — one compromised console doesn't threaten one train, it threatens the coordination of all of them.

What makes it worse is everything else in this analysis: longer trains, 44-second inspections, operators running on broken sleep leaning harder on the automation, vendor-managed subsystems nobody in-house fully understands. Each amplifier was a cost decision. Together they're a threat model.

## Deployment trajectory

This isn't a forecast. It's a history with the last chapter still being written.

The nineties and two-thousands were instrumentation: end-of-train devices, trackside detectors, cab signaling, the first automation overlays. The human stayed in the cab; the instruments started whispering in their ear.

The twenty-tens were optimization: Trip Optimizer, LEADER, distributed power automation, dispatch consolidated into centralized control rooms. The human was still there, but increasingly supervising rather than operating.

The twenty-twenties are remote operation. AutoHaul runs driverless heavy-haul trains across the Pilbara today — two thousand kilometers, no one in the cab, in production, right now. In the US the pieces are assembling: remote-assist pilot programs, deeper cellular and satellite integration into the control path, and FRA petitions stacking up for single-person crews. The direction of travel is the same on both continents.

Past remote operation sits the phase emerging now: full autonomy. Automated routing, automated braking, automated anomaly detection — systems that don't just assist the operator or carry out remote commands, but make the decisions themselves. Every phase moved control further from the rails. None of them moved it back.

## The evidence

It's already happened, in pieces. In 2003 the Sobig worm got into CSX's signaling and dispatch systems — not a targeted rail attack, just commodity malware that found the OT because the OT was reachable. The shape of the thing, two decades early.

Łódź is the cleaner case, and it's told above: unencrypted, predictable, unmonitored. A kid with a modified remote treated the municipal tram network like a model train set, and it worked — because nothing in the design assumed anyone would try.

And the endpoint exists in production. Rio Tinto's AutoHaul runs autonomous heavy-haul trains across the Pilbara: two thousand kilometers of track, no one in the cab. It proves the capability and the exposure at the same time. The thesis isn't a prediction. It's a description of something already running.

## The objections

The serious one first: automation improves safety, and human error dominates the accident statistics. Both true on their own terms. But the statistic needs interrogation — because the human is the only thing in the system that can hit the oh-shit button. Which means the human is structurally always the last link, and structurally always the one available to blame.

East Palestine is the case. The NTSB found the failed bearing car was never inspected after Norfolk Southern picked it up in St. Louis, despite crossing several railyards. An FRA study found the big railroads allowed about 44 seconds per car for inspections when no federal inspector was watching — against 90 inspection points per side of each car. More than a quarter of the cars on that train had defects despite being "inspected." The crew got the blame. However, the conditions were built upstream, by the company, on a schedule.

Anyone who's sat through accident reports knows the pattern: the corporation will do anything to blame the operator. "Human error" as a statistical category counts every incident where the human was the last one touching the controls — and the human is always the last one touching the controls, because they're the only ones who can. The category launders corporate decisions into operator failures.

So concede the narrow point — automation can reduce accident rates — then draw the line the industry won't: fewer accidents and more cyber risk are different categories, and the "human error" numbers the industry cites are already carrying water for the company. The industry will talk about the first and hope you don't notice the second. This analysis exists to document the second. Don't let either side conflate them.

The second objection is about the present: full remote freight operation in the US is still limited. Trip Optimizer and LEADER are driver-assist, not autonomy. Correct — and the analysis shouldn't overclaim it, because overclaiming the present makes the whole thing dismissible. AutoHaul is the honest anchor. It exists, it runs, it's the proof.

The third is a strawman worth killing early: this isn't "fewer people means more hackers." It's specific. Remote operation requires networked components that replace physical presence, and each component is remotely reachable in a way a crew member never was. Name the components or the claim floats.

## The money

From 2010 to 2021, the Class I railroads spent $136 billion buying back their own stock and $47 billion paying dividends. That's $183 billion to make the share price go up. In the same period they spent $138 billion on capital expenditure — the actual railroad. They spent more pumping the stock than keeping the machine running.

The crew cuts are where some of that $183 billion came from. So are the 44-second inspections, the longer trains, the points-based attendance systems. Every cost taken out of the operation is a dollar available for the buyback. The money explains why the cuts happened. It doesn't explain what the cuts built — that's the rest of this analysis.

## Policy implications

Crew reduction isn't a labor issue. It's a national-infrastructure security issue, and the policy follows from everything above.

Crew minimums are security controls. A two-person crew isn't just a safety measure — it's cyber-physical redundancy. The second person is the backup when the first is exhausted, the witness when the automation lies, the only one who can hit the oh-shit button when the network can't.

If remote operation is allowed, it has to be hardened like the target it is: encrypted control paths, authenticated switch commands, tamper-evident telemetry, redundant communication channels, and mandatory human-override authority that no software update can quietly remove.

Vendor systems have to be regulated as what they are. Half the components enumerated above are vendor-managed, which means vendor compromise is rail compromise — and right now that relationship runs on contracts, not security requirements.

Accident statistics have to be reinterpreted. "Human error" needs to be separated from operator exhaustion, operator dependence on automation, and upstream corporate decisions — because as long as the category launders all three into one, the numbers will keep justifying the cuts that produce them.

And cyber-physical incidents have to be reportable as infrastructure failures. Łódź gets told as a curiosity, a weird story about a kid with a remote. It was a successful attack on municipal transit infrastructure by an unauthenticated transmitter. Treat it like one.

## Closing synthesis

The bored teenage boys in the opening aren't outliers. They're the baseline adversary: curious, unsupervised, and willing to interact with any exposed system. Łódź proves the pattern at municipal scale — and crew reduction builds the exact conditions for it at national scale: unattended systems, predictable signals, remotely reachable control paths.

The transformation isn't theoretical. It's already underway. The question was never whether trains can run without engineers. It's whether the systems replacing those engineers can withstand the kinds of interactions engineers once absorbed.

## Verdict

The transformation claim holds. What kills it is imprecision: fudging the deployment state, or blurring the line between accident rates and cyber risk. Keep both sharp and it's airtight.

A crew member can only be attacked physically. A data link can be attacked from anywhere. Everything else is commentary.
