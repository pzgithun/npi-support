# Executive Summary - UtilOS / NCIS (2026-07-17)

## Current Status
- The kickoff aligned the team on NCIS as the Outcomes-managed workstream within the broader UtilOS 58X release effort.
- Requirements are in ADS and have already been reviewed with feedback, but several items still need to be converted into system features before the team can size work and commit to a schedule.
- Networks has already built the requested UtilOS firmware features, but they have not been end-to-end validated because app services support is not yet complete.
- Delivery confidence is currently constrained by dependencies on Tommi's system design work, incomplete custom API definitions, and HSM work in Networks that does not yet have a committed timeline.
- Testing scope, ownership, and timing are still being clarified across Outcomes, Networks, and firmware-related teams, so schedule commitments are not yet stable.

## Decisions Made
- NCIS will remain the Outcomes-managed project because the majority of the required work is Outcomes content.
- Two-hop RF peer-to-peer and EPON should be managed by Networks, with Outcomes contributing the required support work.
- HPP is outside the scope of this group and is coordinated by Phyllis Stevenson.
- Agent participation is through end-to-end solution testing; no functional agent change was identified in this meeting.

## 14-Day Plan
| Topic | Action | Owner |
| --- | --- | --- |
| App services feature definition | Convert approved requirements into system features and use them to assess app services scope and schedule confidence. | Tommi / Dan Facker |
| Mandatory security requirements | Review the new security requirements from the prior threat analysis and capture the required system features. | Tommi |
| Requirements alignment | Review ADS feedback and requirements updates across product management, engineering, and Networks to confirm alignment before execution proceeds further. | Terrence Van Valkenhoef |
| HSM dependency | Confirm the plan and timing for the Networks HSM sub-certification authority work needed for certificate signing support. | Peter Hunt |
| Testing ownership | Hold the follow-up discussion with Logan, Boris, and the relevant teams to clarify who owns firmware-related testing versus Outcomes system testing. | Peter Zimanyi |
| Schedule pressure on test dates | Route open requests for target test dates through Logan until dependencies, ownership, and readiness are defined well enough to commit. | Logan Modahala |
| Solution readiness for test planning | Share the solution and system design documents so test planning and environment preparation can begin where feasible. | Terrence Van Valkenhoef |