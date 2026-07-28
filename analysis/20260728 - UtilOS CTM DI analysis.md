# DI (Distributed Intelligence) Questions & Actions - UtilOS CTM (2026-07-28)

## Purpose
Extract and prioritize all DI-related (Distributed Intelligence) questions and action items discussed in the July 28, 2026 UtilOS core team meeting (CTM), using only transcript evidence.

## Key term note
In this transcript, DI functionality is discussed under the names "Outcomes," "the agent," and "Outcomes agent." This mapping is confirmed by cross-referencing the existing CR3980975 DI analysis in this repo, where "Outcomes QA," "PVA," "ATXM," and "DI application functional testing" are used interchangeably. References to "Outcomes" below are DI-related unless noted otherwise.

## Bottom line
- The single biggest open DI item is whether the AppServe layer needs changes to support the Outcomes/DI agent behavior introduced by the EPON pilot scheme change request (CR). This is unresolved and explicitly flagged as urgent.
- A second material DI item is a legacy ELG (embedded logic/gateway) behavior change required to support a new "in-between mode" for the DI agent, which raises an unaddressed scale/farm-testing risk.
- CT (Compatibility Test, formerly "CAT") support was debated at length and explicitly concluded to be unrelated to enabling DI/Outcomes functionality; it is a local troubleshooting tool only.
- Everything DI-related in this meeting traces back to one governing item: the EPON pilot scheme CR, which is still pending formal impact assessment and approval.

---

## P0 - Blocking CR / schedule (highest priority)

### 1. AppServe change impact from the Outcomes/DI agent (OPEN, unresolved)
- Status: Open. No owner has confirmed impact yet; deferred to Tommi upon his return.
- Evidence:
  - Dahm, Claus: "I am assuming... that there won't be any app serve changes for any entity whatsoever. Is that correct?"
  - Facker, Dan: "Not assuming that yet, no... that is another item that I need to break down on exactly what they're looking for for us, what the design should be."
  - Hardiman, Howard: "Now the question is... does something in App Serve need to change because of what y'all are doing on the Util OS endpoint?"
  - Dahm, Claus: "I'm thinking it's only a DI thing or a transport thing, right?" ... Hardiman, Howard: "The agent, the agent itself, you're saying only..." Dahm, Claus: "Yes, yes, yes, the agent, yeah."
  - Facker, Dan: "what I'm hearing is in M&T stuff, I don't have any work to do for AppServe, but there is a question about for Outcomes agents."
  - Hardiman, Howard: "how it impacts AppServe or the agents, we need to consult someone that would really know how you're using it... The way this decomp is looking right now in Mentity is that this is strictly a UtiloS activity. And I think we want to make sure that that's true."
  - Dahm, Claus: "we need to close this ASAP because if all of a sudden some new chunk of work shows up, things change dramatically."
- Owner / next step: Tommi (back from leave) to decompose the AppServe/agent question for Dan Facker; no committed date given.

### 2. EPON pilot scheme CR - impact assessment and approval (OPEN)
- Status: Open. Draft system requirement exists; formal impact-assessment/approval process not yet started.
- Evidence:
  - Hardiman, Howard: "that CR is ready for the impact assessment of the affected teams... we may need to go... back to that process... update the format of it... and add the approvers."
  - Hardiman, Howard: "the effective development leads have to be approvers, and we need impact assessment from them... also the test resources and the PLMs."
  - Dahm, Claus: "I think we need to take a step back on the CR and go and do some serious homework on that so we can bring it into the program as a CR, not make everything in the program that CR."
  - Hardiman, Howard: "I don't see a world where we would release it without this... it has to go into the plan or be rejected as not such."
- Owner / next step: Howard + Summer to finalize CR format and approvers list; Claus/Howard to set up a dedicated CR meeting with the right players (project management + scope discussion) ahead of planning exit. No committed date ("I can set a target date that the things that I am responsible for will be done by then... but getting the impacts and weaving it into the schedule... [no]").

### 3. Hardware team (Waykun/James) pilot-scheme date, gated by firmware (OPEN)
- Status: Open, in progress. Blocked by both requirement finalization and firmware availability for testing.
- Evidence:
  - Hardiman, Howard: "the mature draft that I have now... Waykun knows what we're asking of them... he's had some other thing crop up... some kind of MPU change."
  - Hardiman, Howard: "the part where they actually may test it and... want to verify with measurements, they would need the firmware, and I think that's what he's listing as the dependency."
  - Bernas, Jason: "it needs firmware and firmware drop date... which team is providing him this firmware?"
  - Hardiman, Howard: "there are really two things we're looking for from Waykun... One is a pin and pad... And then the second is... development and test where he's probably going to want to take the firmware and have the outcomes agent on it and do its thing and then measure."
- Owner / next step: Howard meeting with Waykun same afternoon (July 28); no committed date, gated on CR approval and firmware delivery.

---

## P1 - Needed for near-term schedule build

### 4. Firmware porting for DI/EPON testing (Dan Facker)
- Status: In progress, date committed.
- Evidence:
  - Facker, Dan: "Provide the minimum EPUN port on block testing... that's underway, and we're should have something early next week."
  - Bernas, Jason: confirmed target date of August 3, 2026.
  - Hardiman, Howard: asked if "enabler stuff" was removed; Facker, Dan: "Not yet, no... it was a request to port it as is, so we could have something to work with... I don't think it'll take very long to undo the enabler stuff, but it's not in this particular deliverable."
- Owner / next step: Dan Facker, target date August 3, 2026 (initial port, enabler code still present).

### 5. Legacy ELG change for new DI "in-between mode" - scale/farm-testing risk (OPEN, needs dedicated meeting)
- Status: Open, flagged risk, not yet scheduled.
- Evidence:
  - Hardiman, Howard: "the reason I brought it up, Claus, reluctantly is because with this change, we are ultimately kind of making a change to the legacy ELG at this time... with this in-between mode that we're asking."
  - Dahm, Claus: "I did hear... I'm getting a little nervous when we talk about this in the context of farm testing and in the same sentence using the word scale... as we all know, the scale [testing capacity] is very low."
  - Hardiman, Howard: "I agree with you, but that's the conversation we need to have offline. And Bill needs to be there and the team needs to determine."
- Owner / next step: Dedicated offline conversation needed with Howard, Claus, and Bill (IST); no date set.

### 6. Outcomes (Peter) dates for two subsystem requirements + Sajeev/logins dependency
- Status: Open, expected next week.
- Evidence:
  - Bernas, Jason: "these are outcomes that Peter will get back to us with dates next week."
  - Bernas, Jason: "I thought logins also in this [formless] last week that Sajeev was dependent on Outcomes delivery date, so that's pending [on] the previous [item]."
  - Bernas, Jason (later): "The next one also Outcomes [Peter] will get back to us next week."
- Owner / next step: Peter, target next week (week of August 3-7, 2026).

---

## P2 - Resourcing / process (medium term)

### 7. IST solution-testing resourcing for UtilOS DI work (Bill Greytock)
- Status: Open. No 2026 resources currently allocated; proposal in progress.
- Evidence:
  - Bernas, Jason: "Bill's IST... you're dependent on Outcomes dates right before for phase one and two... at least phase one dates [needed], we have less dependency on them."
  - Greytock, William: "Claus and I started a collaboration session talking about phase one... there are no resources allocated to this from an IST perspective... less util OS to do the solution testing. I'm starting the discussions with Nathan and Steve on this and how this gets prioritized over other MPI programs."
  - Dahm, Claus: "What do we need as escalation goes? Is this a PLM [escalation]?"
  - Greytock, William: "once we come back with a proposal... this is what we could potentially do in 2026 to cover off the solution side... that proposal goes to PLM to make sure that they're in agreement."
- Owner / next step: Bill Greytock proposing to Nathan (same day, July 28 afternoon); potential PLM escalation pending proposal outcome.

---

## P3 - Clarified / low risk (informational, closed or low-priority follow-up)

### 8. CT (Compatibility Test) PD device requirements - confirmed NOT a DI/Outcomes enabler
- Status: Resolved in-meeting; delivery date committed.
- Evidence:
  - Hardiman, Howard: "the way you administer DI on the RIVA meter itself is through FDM Electric, right?"
  - Monier, Fabrice: rationale for including CT was template-driven ("I used other template that was thinking about, okay, you had something you need to think about CT if you need that or not").
  - Dahm, Claus: "Having CT support does not enable any outcomes feature, right? It enables being able to debug something in a very narrow and very specific use case." / "Outcomes is not involved in any way, shape, or form." / "It is a use case in search of a problem... CT for this is pretty useless."
  - Monier, Fabrice: "On development test, we will plan a job IP... it's fairly a non-fin[al] things for customers and not R&D guys. I mean, I won't never use CT to troubleshoot myself in that one."
  - Hardiman, Howard (conclusion): "our response here is what we are offering in terms of any kind of local customer level type debugging for this is via CT, period." Confirmed scoped to field/on-site troubleshooting via Net Manager / Net Manager Lite, not DI feature enablement.
  - Nallam, Prasad (dev lead): "we are good actually. We started our dev activities... we had communicated the schedule also by November 15th... we will try to deliver all the 26 new commands and three existing commands update."
- Owner / next step: Prasad's team, committed delivery November 15, 2026. No further DI action needed; CT explicitly excluded from DI/Outcomes scope.

### 9. EPON scope-alignment action item - stale, needs owner correction
- Status: Needs cleanup, not a DI technical question, but affects DI/CR scope conversations.
- Evidence:
  - Monier, Fabrice: "why are we talking about Yacine for Iqbal [EPON] scope alignment in this program?... we don't have any footing in this right now... you can remove [his] name."
  - Monier, Fabrice: "the architect for the [POC] is Jiangyang... it needs to go through Jiangyang."
  - Dahm, Claus: "this AI is out of date and out of scope and out of alignment."
- Owner / next step: Remove Yacine from the action item; route EPON/POC+ architecture questions to Jiangyang instead. No date given.

---

## Consolidated Open Questions (DI-specific)

1. Does the Outcomes/DI agent itself require AppServe changes as a result of the EPON pilot scheme CR? (P0 - unresolved, owner Tommi)
2. What exactly needs to change on the Riva meter endpoint/legacy ELG to accommodate the new DI "in-between mode," and what is the scale/farm-testing risk? (P1 - unresolved, needs dedicated meeting with Bill)
3. When will the hardware team (Waykun) have a firm date for the DI pilot-scheme pin-and-pad exercise and dev/test measurement work, and is that date contingent on CR approval, firmware delivery, or both? (P0 - open)
4. When will Peter/Outcomes provide dates for the two outstanding subsystem requirements (and, by extension, the Sajeev/logins dependency)? (P1 - expected next week)
5. Will IST (Bill) get 2026 resourcing for UtilOS DI solution testing, and is PLM escalation required? (P2 - open, proposal in progress)

## Consolidated Action Items (DI-specific)

| # | Action | Owner | Target date | Priority |
|---|--------|-------|--------------|----------|
| 1 | Decompose whether AppServe/agent needs changes for DI/Outcomes work | Tommi (via Dan Facker) | Not set | P0 |
| 2 | Finalize CR format and approvers (dev leads, test resources, PLMs); drive impact assessment | Howard + Summer | Not set ("top priority" once back) | P0 |
| 3 | Set up dedicated CR scoping meeting with all affected players | Claus / Howard | Not set | P0 |
| 4 | Finalize pilot-scheme requirement discussion with Waykun/James | Howard | Meeting same day (July 28 PM) | P0 |
| 5 | Deliver minimum EPON firmware port for bench testing | Dan Facker | August 3, 2026 | P1 |
| 6 | Hold dedicated conversation on legacy ELG "in-between mode" scale/farm-testing risk | Howard / Claus / Bill | Not set | P1 |
| 7 | Provide dates for two outstanding Outcomes subsystem requirements | Peter | Week of Aug 3-7, 2026 | P1 |
| 8 | Propose 2026 IST resourcing plan for UtilOS solution testing; escalate to PLM if needed | Bill Greytock (with Nathan/Steve) | Proposal same day (July 28 PM) | P2 |
| 9 | Deliver 26 new + 3 updated net manager commands (CT support, not DI-enabling) | Prasad's dev team | November 15, 2026 | P3 |
| 10 | Remove Yacine from EPON scope-alignment action item; route to Jiangyang | Claus / Howard | Not set | P3 |

## Source
- Transcript reviewed: transcripts/20260728 - UtilOS CTM.txt
