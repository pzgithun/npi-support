# UtilOS Activity Summary - NCIS, ePON, 2 Hop RF P2P (2026-07-17)

This summary is based on the 2026-07-16 kickoff transcript and supporting material from utilos_review.pptx.

## NCIS

### Status
- NCIS is the Outcomes-managed workstream within the broader UtilOS 58X release effort.
- Requirements are loaded in ADS and have already been reviewed, with feedback returned.
- Networks has already implemented the requested UtilOS firmware features, but end-to-end validation has not started because app services support is not yet ready.
- App services and DINA both depend on additional design definition before execution and schedule confidence can be improved.

### Schedule Info
- The supporting deck places NCIS app services design and development in Q3 2026.
- The deck and meeting align on Q4 2026 for integration work and bug fixing.
- The deck places end-to-end environment setup and testing in Q1 2027.
- The meeting notes that actual device testing cannot start until app services is ready, so later phases are gated by Q3 design and development progress.

### Decisions
- NCIS remains the Outcomes-managed project because most of the work sits with Outcomes.
- App services work for NCIS should proceed from formalized system features rather than directly from raw requirements.
- No functional agent change was identified; agent participation is through end-to-end solution testing.

### Risks / Issues / Open Points
- Tommi has not yet seen all of the new mandatory security requirements from the prior threat analysis.
- Some custom APIs are still missing from the current system design documentation.
- The HSM sub-certification authority work in Networks is required and does not yet have a committed timeframe.
- Dan could not yet commit to finishing all app services development by the end of Q3.
- Testing ownership is not fully settled between Outcomes system test and firmware-oriented teams.

## ePON

### Status
- ePON was discussed as a separate activity from NCIS, even though it appears in the broader UtilOS review picture.
- The meeting characterized the current ePON effort as similar to Tommi's earlier work, but this variant is focused on Gen5.
- App services changes are still expected for ePON.
- The prior implementation relied heavily on Tracy rather than on a clearly assigned standing team.

### Schedule Info
- The deck places ePON under the same broader 3.1.4 / UtilOS 58X support discussion, but no committed delivery dates were established in the meeting.
- The meeting did not produce a quarter-by-quarter ePON plan comparable to NCIS.
- Testing timing remains dependent on clarifying which development team owns end-to-end execution.

### Decisions
- ePON should not be treated as part of the NCIS Outcomes-managed scope in the same way as NCIS itself.
- Dev team ownership should cover ePON end-to-end testing once the responsible team is clarified.
- Logan's team is expected to cover coexistence testing and possibly scale testing rather than owning all ePON end-to-end testing.
- PowerMon was explicitly treated as out of scope for this group.

### Risks / Issues / Open Points
- The responsible development team for ePON end-to-end ownership was not identified in the meeting.
- The team still needs to resolve the "Tracy team" question and determine whether ePON now belongs to a formal colored team.
- It remains unclear whether ePON affects only PAC / Gen5 or has broader agent implications.
- The meeting described ePON as spanning multiple programs, which increases coordination risk and makes ownership less obvious.

## 2 Hop RF P2P

### Status
- 2 Hop RF P2P was explicitly framed as Networks-driven rather than Outcomes-managed.
- Outcomes is still expected to contribute app services support for the activity.
- The supporting deck states that app services must develop new APIs for this work and that Tommi must first create the feature.

### Schedule Info
- No committed delivery schedule was established in the meeting for 2 Hop RF P2P.
- The activity is tied to the broader end-of-year brownfield / UtilOS 58X bundle discussed by Terrence.
- Testing timing is dependent on feature definition, app services development, and confirmation of who owns end-to-end execution.

### Decisions
- 2 Hop RF P2P is Networks-owned from a program management perspective.
- Outcomes will provide the app services changes needed to support the capability.
- The working assumption at the end of the meeting was that Boris's team will perform end-to-end testing, pending verification with Boris and Logan.

### Risks / Issues / Open Points
- Tommi still needs to create the feature so app services can review scope, understand requirements, and estimate work.
- End-to-end test ownership is still an assumption and was left for follow-up confirmation with Boris and Logan.
- There was no firm conclusion from the earlier test coverage discussion involving Boris.
- The activity is easy to confuse with NCIS because it appears in the same broader release bundle, even though it is supposed to run under Networks ownership.

## Cross-Activity Notes
- The deck reinforces the meeting view that NCIS has the clearest phased timeline, while ePON and 2 Hop RF P2P still need ownership and testing clarification.
- Across all three activities, the main gating themes are incomplete design definition, unsettled testing ownership, and dependencies on teams outside Outcomes.