# Solarian — Evidence, Prior Art & Claims

*What the proposal defines, what the calculations demonstrate, what earlier designers contributed, and what remains unverified*

**Initial Public Issue 1.0 · October 2026 · Evidence/claims audit, not a certification or priority ruling**

## Purpose and scope

A calendar can be mathematically coherent, useful as a framework and worthy of independent implementation without every statement about it having the same evidentiary status. Solarian is presented openly so others can inspect its definitions, reproduce its calculations, challenge its assumptions and decide whether its trade-offs suit their own requirements. That programme needs an equally open account of its sources and limits.

This document divides the claims associated with Solarian into five kinds: **(a) definitions chosen by the designer; (b) mathematical deductions from those definitions; (c) empirical results within an identified astronomical model and window; (d) comparative interpretations and recommendations; and (e) historical priority or adoption claims requiring further external evidence.** A definition may be perfectly precise without being ‘experimentally proven’; a numerical result may pass within a test window without predicting every future orbit; and a reasoned adoption recommendation is not an observed social outcome.

The reference baseline is the author-approved reconciled *Solarian* manuscript with Appendix G; the S2b2c DE440 planetary year-form release-candidate registry; and the expressly author-ratified PF, EJ, AP and DR records. The supporting W3 evidence register maps each assertion to these materials and identifies publication gates. [S1][T1]–[T5]

## 1. Prior art: substantial groundwork, not an empty field

Calendrics has a long technical and historical literature. The mismatch between cycles and integral civil units, intercalation, period naming, and the distinction between astronomical and administrative time are longstanding concerns. Foundational comparative treatments include Reingold and Dershowitz’s *Calendrical Calculations* and E. G. Richards’s *Mapping Time*. Neither ordinary leap correction nor the idea of an operating calendar is a Solarian invention. [R6]

**The Gregorian calendar** combines continuous seven-day weeks, twelve inherited months, leap-day intercalation and strong institutional entrenchment. It provides excellent continuity for Earth, but a Gregorian date alone is not a local orbital-year calendar for Mars or Titan. An Earth-derived date and precise scientific timescale will nevertheless remain compelling common chronological references, whatever new local civil calendars develop.

**Earth’s 4-4-5 / 4-5-4 / 5-4-4 fiscal calendars** show that weekly operating cadence can coexist with—and differ from—legal month boundaries. They are relevant precedents for a distinct human operating layer; they do not demonstrate planetary applicability or Solarian’s specific Repeat Factor. The US Internal Revenue Service recognises 52–53-week accounting years, a useful example of deliberate whole-week civil organisation. [R7]

**Mars-specific calendar designs** are numerous and materially different. I. M. Levitt preserved a twelve-month structure. Thomas Gangale’s Darian Calendar employs 24 Martian months of 27 or 28 sols and deliberately shortens the final weekday-position sequence in certain months to keep month starts aligned. Josef Šurán’s 1997 calendar preserves complete seven-sol weeks, using 672-sol years and selected 665-sol years; this is a direct precedent for week-level intercalation, not a discovery that Solarian can claim as its own. Robert Zubrin’s approach emphasised 30° sections of the orbit, with unequal elapsed-time months reflecting Mars’s eccentric motion. Dennis Silin’s more recent Exodus approach emphasises familiar names and a twelve-month structure. The record shows real optimisation alternatives, not failed attempts awaiting one right answer. [R1][R2][R3][R4][R5][S1]

**Outer-world calendar work** preceded Solarian. Gangale’s work on Galilean-moon and Titan calendars explored destination-specific adaptations of day, week, year and local astronomical cycles. It is especially relevant evidence that calendar architecture beyond Earth and Mars was already a live problem. [R3][S1]

**Marian**, the author’s separate Mars-specific calendar, independently develops the distinction between human-scale minths and twelve astronomical months. In its current canonical form Marian uses twelve months and two minths per month, with 27/28-sol minths and 668/669-sol years. It preserves recurring date–weekday relationships through designated shortened terminal civil weeks rather than maintaining an unbroken seven-position week. Marian is a distinct proposal with its own reasons and potential advantages, not an early version of Solarian and not a Solarian-compatible implementation by definition. [M1]

## 2. What Solarian claims to contribute

The strongest originality claim is **architectural integration**, not invention of any one ingredient. Solarian combines: a portable day/week/minth/mear operating layer; twelve locally astronomical months; the twelve-against-twelve identity that produces integer R where useful; a principled independent regime; uninterrupted seven-position local weeks; constrained and distributed whole-week expansion joints; a common 100° heliocentric orbital reference; a shared standard-day SWI coordinate with sol-based Mars mapping; explicit phase-applicability boundaries; and versionable machine-readable profile semantics. [S1]

The narrow, defensible historical formulation is: **this manuscript proposes and specifies this combined multi-world architecture, and identifies related earlier approaches where known.** That is not the same as asserting that no earlier work assembled an equivalent combination. An exhaustive global novelty or priority search has not been conducted. Claims of ‘first-ever universal calendar’, exclusive invention of leap weeks, or proven superiority to all alternatives should therefore not appear in the technical record. [S1]

The mathematical relation **R = minths per orbital month = mears per orbital year** follows directly from the selected twelve minths/mear and twelve months/orbital-year structure in synchronised implementations. The proof is elementary and reproducible. Its elegance does not prove that every inhabited world should choose these conventions, that all astronomy can be represented by standard months or that a calendar would be adopted without governance and cultural negotiation.

## 3. Evidence hierarchy and status labels

For clarity, W3 uses the following evidence statuses consistently:

| Status | Meaning | Examples |
|---|---|---|
| **DEFINED** | A rule or policy the architecture explicitly specifies; not an empirical discovery | Twelve minths/mear; Common = even weeks |
| **MATHEMATICALLY DERIVED** | Consequence proved from definitions or exact arithmetic | Integer R identity; 12R minths/year |
| **NUMERICALLY TESTED — BOUNDED** | Computed against named astronomical model, interval, conventions | Six DE440 planetary year-form profiles |
| **HISTORICAL DIAGNOSTIC** | Useful legacy-source calculation, not contemporary model-certified | Nineteen-asteroid CODES screen |
| **AUTHOR-RATIFIED POLICY** | Author has approved a methodological rule only | PF, EJ, AP and DR decision scopes |
| **UNVERIFIED / PENDING** | Evidence, formal sign-off or verification not yet present | Contemporary asteroid Horizons reconciliation, all-epoch claims, universal novelty |
| **NORMATIVE PUBLICATION HOLD** | Private technical record exists; unqualified public release not authorised | Solarian Protocol v1.0 launch / DOI |

A result may occupy multiple categories—for example, an author-ratified threshold can be mathematically well-defined while an individual asteroid’s ability to meet it remains unverified against contemporary trajectories.

## 4. Planetary calculations: strong within the declared envelope

The S2b2c technical registry uses a JPL DE440-based sequence of planetary reference-ray crossings, deterministic nearest-week quantisation, and registered year-form vector compilation. For the six synchronised planetary profiles actually evaluated, the candidate registry contains **28 distinct forms**: 22 book-canonical forms and six supplemental lengths. The supplementary lengths are Jupiter 620; Saturn 1,535, 1,538 and 1,539; Uranus 4,385; and Neptune 8,600 weeks. They are physically meaningful results of crossing-date differences and boundary rounding—not evidence that the underlying human calendar changes or that a weekday disappears. [T1]

For outer-planet perspective, the tested crossing intervals produced **83 Jupiter years, 33 Saturn years, 11 Uranus years and five Neptune years**, over the bounded approximately 1600–2600 interval. Saturn’s observed physical return duration spanned approximately **1,535.390–1,538.665 weeks**, and the quantised civil forms spanned **1,535–1,539 weeks**. The two-form textbook mean-period argument remains mathematically sound as an *idealisation* but is not an exhaustive implementation register. Appendix G states that distinction plainly. [S1][T1]

The planetary crossings and produced year forms underwent independent numerical agreement checks against official CSPICE in the earlier technical work. That is more meaningful than a spreadsheet-only consistency check, but it does not certify prediction indefinitely into the future, irreversibility of published dates against source changes, social usability or operational deployment. The source conventions and frozen hash-addressed data remain essential to reproducibility. [T1]

## 5. Phase fidelity: a specified numerical test, not all-purpose ‘correctness’

The phase metric compares each actual civil orbital-month start with a theoretical twelve-position 100°-oriented angular dial. The registered rules are: **≤30°** maximum wrapped angular deviation satisfies the numerical standard-phase criterion; **>30° to ≤45°** requires individual marginal review; **>45°** requires specialised astronomical treatment. These bounds were **author-ratified as policy**, not derived uniquely from human perception, navigation performance or external consensus. [T2]

The bounded planetary tests yielded approximately 13.86° for Venus, 20.94° for Mars and 59.26° for Mercury. Venus can satisfy the numeric standard within the tested window despite being in the independent regime. Mercury’s chronological calendar and independent human cadence remain valid, but the standard twelve-month civil-start dial is unsuitable as a coarse phase proxy on the tested criterion. **Phase passing is necessary for standard-phase classification but never sufficient for a general conformance certificate**: it does not substitute for correct timestamps, profile versioning, verified input sources, complete layouts or acceptance of operational requirements. [T2]

Likewise, a highly eccentric orbit is not declared unacceptable solely from an eccentricity number. Orientation relative to the 100° ray and the actual computed monthly boundaries matter. The standard includes *graceful failure*: calendar functions not dependent on the failed phase proxy continue to work.

## 6. The asteroid diagnostic: what it does and does not establish

The historical Main-Belt screening evaluated 19 large bodies and identified **69 distinct body-specific week-length forms**, eight already represented by book-canonical examples and 61 additional candidate layouts. The candidate year-form compiler follows an **author-ratified method**: use existing book vectors first, exhaust primary Minth L positions, apply deterministic secondary positions if required, preserve 3/4/5-week minths, and test phase fidelity separately rather than tuning month layouts to pass the phase criterion. **Ratifying this method is not ratifying its 61 outputs.** [T3][T4]

The asteroid state vectors came from the archival **CODES 2010 / DE405-era** material. The executed historical diagnostic combined those asteroid trajectories with more recent planetary/Sun conventions; it is therefore a **mixed-model historical screen**, useful for candidate generation and identifying potential applicability trouble but not a contemporary, source-harmonised Horizons certification. The author expressly allowed an assumption of future source agreement *for workflow planning only*. That assumption must never be described as a performed test or positive result. [T3][T4]

Its governance routes comprise **11 standard-potential**, **six mandatory marginal reviews**, and **two requiring specialised astronomical-month treatment** (Juno and Bamberga). These are routing categories arising from the bounded diagnostic. The six marginal candidates are Pallas, Interamnia, Davida, Eunomia, Psyche and Thisbe; Eunomia retains a conservative provisional editorial description pending exact review. **All 19 asteroid profiles remain unratified**, and 61 supplemental forms still require individual source-appropriate and author approval. Numerical screening success does not elevate a candidate to a released profile. [T4][T5]

## 7. Claim ledger: claims we can and cannot make

| ID | Claim, stated at appropriate strength | Disposition |
|---|---|---|
| CL-01 | Solarian defines two interoperable calendar layers and three applicability routes | DEFINED; book/protocol architecture |
| CL-02 | Integer R follows from the twin twelve-position structures | MATHEMATICALLY DERIVED |
| CL-03 | Whole-week quantisation preserves unbroken weekday sequence | DERIVED under the specified rules |
| CL-04 | A Solarian mear always contains twelve minths, though not necessarily 48 weeks | DEFINED |
| CL-05 | Six DE440 synchronised planetary profiles have 28 known registered candidate forms | BOUNDED NUMERICAL RESULT |
| CL-06 | Standard monthly phase-proxy potential is measured with 30°/45° thresholds | AUTHOR-RATIFIED CRITERION; applicability conditional |
| CL-07 | Mercury’s ordinary month-start dial breaches the phase threshold in the tested window | BOUNDED NUMERICAL RESULT; specialised treatment |
| CL-08 | Historical asteroid screening routes 11/6/2 and produces 61 supplemental candidates | HISTORICAL DIAGNOSTIC ONLY |
| CL-09 | All asteroid profiles pass contemporary Horizons source-parity checks | **NOT ESTABLISHED — do not claim** |
| CL-10 | The 28-form planetary catalogue is exhaustive forever | **NOT ESTABLISHED — do not claim** |
| CL-11 | No earlier calendar had any of Solarian’s individual elements | **FALSE AS A GENERAL CLAIM — prior art exists** |
| CL-12 | Solarian is the best calendar for all settlements, including Mars | **VALUE JUDGMENT — not a demonstrated scientific result** |
| CL-13 | Solarian is a plausible candidate for an interoperable multi-world common grammar | REASONED DESIGN ASSESSMENT, not adoption evidence |
| CL-14 | Solarian Protocol v1.0 and DOI records have already been publicly issued | **PUBLICATION STATUS UNVERIFIED / RELEASE HOLD** |

This ledger intentionally includes **negative and constrained claims**. A scientifically credible open proposal identifies where not to extrapolate.

## 8. Outstanding evidence and governance work

The main certification gate remains *source-matched contemporary* asteroid trajectories and independent crossing verification, followed by profile-by-profile phase review, exact-vector hash-addressed sign-off and separately reviewed specialised representations where necessary. Broader time-window robustness, ephemeris uncertainty around nearest-week boundaries, and independent implementation conformance require documented limits rather than boilerplate confidence.

Separate release gates govern (i) astronomical and year-form certification, (ii) exact book/editorial text, figures and licensing, and (iii) GitHub, Zenodo, DOI and public-web deployment. Completing one does not silently satisfy another. The final site must verify claims such as ‘first published’ or ‘DOI issued’ against reality when it is actually released. [T5]

## 9. Historical-priority and impact discipline

Solarian should claim neither the invention of leap-week correction (Šurán is a direct counterexample) nor the discovery of dual time systems (many civil and fiscal calendars layer different functions). Its defensible intellectual claim is a **newly articulated integrated architecture** built around shared meaning beneath locally different astronomical calendars.

The complete novelty of that combination is a topic for an explicit, systematic prior-art review—especially beyond English-language journals, technical reports and informal proposed calendars. Likewise, whether future people find A–L naming intuitive, whether a multi-world polity accepts one 100° reference, and whether software teams adopt the protocol are human and institutional questions that cannot be inferred from year-form arithmetic. [S1]

Scientific legitimacy improves when design authors allow reproducible criticism. Solarian’s most credible path is therefore to make rules, data, failure cases and source boundaries independently inspectable, to maintain immutable versioned records, and to welcome tests that expose necessary corrections. A carefully limited claim is not a weaker publication; it is one capable of surviving scrutiny.

## Bibliographic and technical source key

**Technical primary evidence:** [S1] author-approved *Solarian* manuscript and Appendix G; [T1] S2b2c canonical planetary year forms and crossing evidence; [T2] author-ratified Solarian Phase Fidelity Standard v1.0.0; [T3] author-ratified asteroid expansion-joint candidate generator v1.0.0; [T4] author-ratified asteroid profile governance v1.0.0; [T5] author-ratified DR procedures v1.0.0. Full frozen file hashes are in the W3 evidence register.

**Independent prior art:** [R1] J. Šurán, “A Calendar for Mars,” *Planetary and Space Science* 45 (1997), 705–708, DOI: 10.1016/S0032-0633(97)00033-0; [R2] T. Gangale, “Martian Standard Time,” *JBIS* 39 (1986), 282–288; [R3] T. Gangale and M. Dudley-Rowley, “Issues and Options for a Martian Calendar,” *Planetary and Space Science* 53 (2005), 1483–1495, DOI: 10.1016/j.pss.2005.07.012; [R4] R. Zubrin with R. Wagner, *The Case for Mars* (1996); [R5] D. V. Silin, “The Exodus Calendar,” *JBIS* 78 (2025), 305–307, DOI: 10.59332/jbis-078-09-0305; [R6] N. Dershowitz and E. M. Reingold, *Calendrical Calculations* (2018), E. G. Richards, *Mapping Time* (1998); [R7] US IRS, Publication 538, 52–53-week tax-year rules; [M1] JB Bullock, separately authored Marian Calendar manuscript and specification, distinct Mars-only architecture. The references are works of record, not claims that all have been independently re-read for W3.
