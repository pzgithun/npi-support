# UtilOS Activity Summary - NCIS, ePON, 2 Hop RF P2P (2026-07-17)

This summary captures current status, schedule, decisions, and open points for NCIS, ePON, and 2 Hop RF P2P.

## NCIS

### Status
- NCIS is the Outcomes-managed workstream within the broader UtilOS 5.x release effort.
- Requirements are loaded in ADS and have already been reviewed, with feedback returned.
- Networks has already implemented the requested UtilOS firmware features, but end-to-end validation has not started because AppServ support is not yet ready.
- AppServ and DINA both depend on additional design definition before execution and schedule confidence can be improved.

### Schedule Info
- NCIS AppServ design and development are planned for Q3 2026.
- Integration work and bug fixing are targeted for Q4 2026.
- End-to-end environment setup and testing are planned for Q1 2027.
- Device testing cannot begin until AppServ is ready, so later phases remain gated by Q3 design and development progress.

### Decisions
- NCIS remains the Outcomes-managed project because most of the work sits with Outcomes.
- AppServ work for NCIS should proceed from formalized system features rather than directly from raw requirements.
- No functional agent change was identified; agent participation is through end-to-end solution testing.

### Risks / Issues / Open Points
- Tommi has not yet seen all of the new mandatory security requirements from the prior threat analysis.
- Some custom APIs are still missing from the current system design documentation.
- The HSM sub-certification authority work in Networks is required and does not yet have a committed timeframe.
- Dan could not yet commit to finishing all AppServ development by the end of Q3.
- Testing ownership is not fully settled between Outcomes system test and firmware-oriented teams.

### Actions
- Finalize and publish missing system design details, including custom APIs, to unblock AppServ and DINA execution planning.
- Confirm NCIS testing ownership across Outcomes system test and firmware-oriented teams.
- Align on a committed Q3 AppServ completion plan and communicate schedule confidence updates.
- Confirm timing and ownership for HSM sub-certification authority work in Networks.

## ePON

### Status
- ePON is treated as a separate activity from NCIS, even though it appears in the broader UtilOS review picture.
- The current ePON effort is similar to Tommi's earlier work, but this variant is focused on Gen5.
- AppServ changes are still expected for ePON.
- The prior implementation relied heavily on Tracy rather than on a clearly assigned standing team.

### Schedule Info
- ePON sits under the same broader 3.1.4 / UtilOS 5.x support discussion, but no committed delivery dates are established.
- A quarter-by-quarter ePON plan comparable to NCIS is not yet defined.
- Testing timing remains dependent on clarifying which development team owns end-to-end execution.

### Decisions
- ePON should not be treated as part of the NCIS Outcomes-managed scope in the same way as NCIS itself.
- Dev team ownership should cover ePON end-to-end testing once the responsible team is clarified.
- Logan's team is expected to cover coexistence testing and possibly scale testing rather than owning all ePON end-to-end testing.
- PowerMon was explicitly treated as out of scope for this group.

### Risks / Issues / Open Points
- The responsible development team for ePON end-to-end ownership has not been identified.
- The team still needs to resolve the "Tracy team" question and determine whether ePON now belongs to a formal colored team.
- It remains unclear whether ePON affects only PAC / Gen5 or has broader agent implications.
- ePON spans multiple programs, which increases coordination risk and makes ownership less obvious.

### Actions
- Assign a responsible development team for ePON end-to-end ownership.
- Resolve the "Tracy team" ownership question and document formal team alignment.
- Define and publish a quarter-by-quarter ePON delivery plan.
- Confirm intended scope impact (PAC/Gen5-only versus broader agent impact).

## 2 Hop RF P2P

### Status
- 2 Hop RF P2P was explicitly framed as Networks-driven rather than Outcomes-managed.
- Outcomes is still expected to contribute AppServ support for the activity.
- The current scope indicates that AppServ must develop new APIs for this work and that Tommi must first create the feature.

### Schedule Info
- No committed delivery schedule is established for 2 Hop RF P2P.
- The activity is tied to the broader end-of-year brownfield / UtilOS 5.x bundle.
- Testing timing is dependent on feature definition, AppServ development, and confirmation of who owns end-to-end execution.

### Decisions
- 2 Hop RF P2P is Networks-owned from a program management perspective.
- Outcomes will provide the AppServ changes needed to support the capability.
- The current working assumption is that Boris's team will perform end-to-end testing, pending verification with Boris and Logan.

### Risks / Issues / Open Points
- Tommi still needs to create the feature so AppServ can review scope, understand requirements, and estimate work.
- End-to-end test ownership is still an assumption and was left for follow-up confirmation with Boris and Logan.
- There was no firm conclusion from the earlier test coverage discussion involving Boris.
- The activity is easy to confuse with NCIS because it appears in the same broader release bundle, even though it is supposed to run under Networks ownership.

### Actions
- Have Tommi complete feature definition so AppServ can finalize scope review and effort estimates.
- Confirm end-to-end test ownership with Boris and Logan and document the decision.
- Establish a committed delivery timeline tied to feature definition and AppServ/API readiness.
- Clarify and communicate separation of 2 Hop RF P2P from NCIS ownership to avoid execution confusion.

## Cross-Activity Notes
- NCIS has the clearest phased timeline, while ePON and 2 Hop RF P2P still need ownership and testing clarification.
- Across all three activities, the main gating themes are incomplete design definition, unsettled testing ownership, and dependencies on teams outside Outcomes.

### Actions
- Create a single owner-tracking view covering development owner, test owner, and status for NCIS, ePON, and 2 Hop RF P2P.
- Set a recurring cross-team checkpoint to close ownership decisions and surface dependency risks early.
- Track design-completeness milestones and tie them to AppServ execution and test-readiness gates.