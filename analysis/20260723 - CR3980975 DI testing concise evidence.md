# CR 3980975 - DI Testing Scope (Concise Evidence Summary)

## Working conclusion
- Full DI application functional testing appears out of October 1 sample scope.
- Some DI/app-side testing activity still appears required before October 1.
- Scope boundaries were not fully closed in-meeting and need explicit confirmation.

## Evidence that DI testing is needed before October
1. DI-side test cases were still being worked and bug-tagged for review.
   - Transcript: Boris called out DI-side app serve/HAN test cases and committed to tag related bugs for review.
   - Source line: transcripts/20260723 - DI Electric Solution CTM.txt:126

2. DI-related app elements were explicitly named in scope discussions.
   - Transcript: Raji listed PVA and ATXM location awareness.
   - Source line: transcripts/20260723 - DI Electric Solution CTM.txt:131

3. End-of-August execution expectation was attached to those DI app elements.
   - Transcript: Srini asked Outcomes QA commitment to test them before end of August.
   - Source line: transcripts/20260723 - DI Electric Solution CTM.txt:132

4. Named follow-up action was assigned to drive app-side completion.
   - Transcript: Raji committed follow-up with Peter and David to ensure app-side testing completion by end of August.
   - Source lines: transcripts/20260723 - DI Electric Solution CTM.txt:133, transcripts/20260723 - DI Electric Solution CTM.txt:136

## Evidence that DI testing is not needed (or reduced) for October
1. Full DI application functional testing was stated out of scope.
   - Transcript: Esam said DI application functional testing is not in scope, with limited testing.
   - Source line: transcripts/20260723 - DI Electric Solution CTM.txt:149

2. CR scope was described as high-voltage plus basic-solution testing.
   - Transcript: Esam stated CR scope as high-voltage testing and basic solution testing.
   - Source line: transcripts/20260723 - DI Electric Solution CTM.txt:158

3. October exclusion was explicitly confirmed in discussion.
   - Transcript: Raji asked if it was not required for October; Esam replied "Exactly."
   - Source lines: transcripts/20260723 - DI Electric Solution CTM.txt:177, transcripts/20260723 - DI Electric Solution CTM.txt:178

4. Final-production-level coverage was deferred to a later milestone.
   - Transcript: Esam said final production is still required in January 2027.
   - Source line: transcripts/20260723 - DI Electric Solution CTM.txt:176

## Questions that must be answered to clarify DI needs
1. What exact DI test cases are included in "limited testing" for October 1?
2. Which DI app items are mandatory before October 1: PVA, ATXM, HAN/app-serve, or a subset?
3. Who owns each in-scope DI test item (Outcomes QA, DI team, System Test), and where is that ownership recorded?
4. Is end-of-August still the internal completion gate for DI sample readiness, and what exceptions are acceptable?
5. Which DI test items are explicitly deferred to January 2027 final-production testing?
6. What single internal artifact will map "October required" vs "deferred" sections from the customer attachment?
7. Who gives final approval for DI-related exceptions tied to October sample shipment?

## Recommended note wording
Per core-team discussion, full DI application functional testing is out of October 1 sample scope, but limited/basic DI-related testing and app-side follow-up actions remain in scope before October. Final-production coverage is deferred to January 2027.
