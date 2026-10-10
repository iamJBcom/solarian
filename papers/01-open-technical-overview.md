# Solarian — Open Technical Overview

*The architecture, its operational choices, and what a real implementation must specify*

**Initial Public Issue 1.0 · October 2026 · Informative, not the normative Protocol v1.0**

## Executive overview

Solarian is a proposed common operating-calendar architecture for human communities living on different planets, moons, asteroids and artificial habitats. It does not argue that every settlement should share the same local dates. Instead, it identifies a small set of shared structural meanings that make locally different calendars understandable, comparable and implementable across a multi-world civilisation.

Its decisive move is to separate two jobs that the terrestrial year and month often perform together: organising ordinary human activity and describing the local astronomical orbit. The **human layer** supplies the continuous week, minth and mear. The **astronomical layer** supplies twelve orbital months and one local heliocentric year. Where the scales fit usefully together, an integer **Repeat Factor** (R) connects the layers. Where they do not, the layers continue independently.

Solarian also specifies what must not be sacrificed to make the arithmetic tidy: the weekly sequence does not break; intercalation occurs in complete weeks at declared expansion joints; and a planetary calendar should not falsely claim good orbital-phase fidelity where the standard astronomical-month representation has ceased to work.

This overview is a companion to the copyrighted explanatory book. It does **not** replace the normative specification, frozen year-form registry, dated conversion tables or executable conformance tests. Its examples are explanatory, not authority to implement an unregistered profile. [S1][T1]

## 1. Two simultaneous calendars

The **people/operating calendar** is the portable layer:

- A civil day is ordinarily 86,400 SI seconds. Mars deliberately retains its natural sol.
- A week contains seven uninterrupted local civil days.
- A normal minth contains four weeks, but a designated minth may contain three or five.
- A mear contains exactly twelve consecutive minths, identified structurally as A through L. An unadjusted mear is 48 weeks; its duration is not fixed by definition.

The **world/astronomical calendar** identifies one heliocentric orbit as the local orbital year and divides its civil representation into twelve orbital months. An orbital month is not supposed to provide the human planning interval. At Neptune its duration is many Earth years; ordinary operating recurrence continues through mears instead.

The distinction avoids asking the same unit to describe a world’s orbit and human routines simultaneously. It also allows local names, festivals, business periods and political decisions to sit above common machine-readable identifiers rather than being legislated by a present-day terrestrial designer. [S1]

## 2. Repeat Factor and operating regimes

In **synchronised** profiles, the integer relationship is:

**R = minths per orbital month = mears per orbital year.**

Because twelve minths form a mear and twelve orbital months form a year, the same integer connects both sides. The synchronised orbital year contains twelve R minths, partitioned into twelve months containing R minths each. Representative implementations include Mars R2, Ceres R5, Jupiter R13, Saturn R32, Uranus R91 and Neptune R179.

For example, Saturn R32 contains 32 mears and 384 minths during one approximately 29.5-Earth-year orbital year. The enormous astronomical year does not force an enormous human-scale ‘month’. Most of those 384 minths remain ordinary four-week periods.

In an **independent** profile, the operating calendar and astronomical calendar do not need to nest. Venus and Mercury are the book’s principal cases: a short orbital year should not shrink or fragment the useful approximately 48-week human operating cycle. The two calendars remain convertible against common chronology without imposing an artificial integer R.

A third **specialised astronomical treatment** is necessary when the standard twelve-month civil sequence poorly represents orbital position. The human week, minth and mear can remain useful even if a different astronomical display or additional scientific phase information is required. The threshold is an applicability decision, not a reason to discard the full calendar architecture. [S1][T2]

## 3. The week and the expansion joints

Solarian expresses civil month, mear and year boundaries in whole weeks. Designated **expansion joints** reconcile these boundaries with physical orbits: normal Minth L at the end of a mear is the primary adjustment location, and approved secondary A–K locations can be used where necessary. Each adjusted minth remains three, four or five complete weeks. The first day of a minth, mear, month or civil orbital year therefore remains the reference first weekday—Monday in the book’s terminology.

A Common Year means **an even number of civil weeks**; a Leap Year means **an odd number**. Leap therefore does not necessarily mean longer, and an implementation must not assume only one form of each parity. The year length is derived from the difference between two independently quantised astronomical crossing boundaries, then matched to the **exact registered year form**. An unregistered length is not silently assigned another form with the same parity. [S1][T1][T3]

The book’s adjacent two-form examples correctly explain how a *constant mean orbital period* can be represented with whole-week years. Real planetary crossing-to-crossing intervals vary because the Solar System is dynamically interacting, and independent endpoint rounding can create additional civil year lengths. A DE440-based bounded test of Saturn yielded five lengths—1,535 through 1,539 weeks—rather than only the nominal 1,536/1,537 pair. Appendix G explicitly explains that distinction without changing the main book’s teaching model. [S1][T1]

## 4. Astronomical orientation and phase fidelity

The Solarian orbital year is indexed to a fixed common **100° heliocentric reference ray**. The technical convention uses geometric Sun-to-planetary-barycentre positions in the **ECLIPJ2000** reference frame and a declared JPL ephemeris; each reference-ray crossing is independently quantised to the nearest local civil-week boundary, with a defined tie rule. Civil orbital months are then allocated according to the registered month/minth layout for that exact year form. The resulting date is a discrete *representation* of the real continuous orbit—not a replacement for an astronomical ephemeris. [S1][T1]

A separately ratified phase-fidelity criterion compares the actual heliocentric longitude at each civil orbital-month start to the ideal 100° + 30° × month-index reference. Maximum wrapped angular error at or below **30°** meets the numeric standard-phase threshold; above 30° through **45°** requires explicit marginal review; above 45° requires specialised astronomical treatment. A passing phase score is **not** by itself a fully certified calendar profile. [T2]

The bounded DE440 screens reported approximately 13.86° for Venus, 20.94° for Mars and 59.26° for Mercury. Accordingly, Mercury retains its independent operating calendar and chronological month/year sequence, but its ordinary twelve-month starts are not approved as a standard angular-position proxy. All such figures have finite model/window qualifications. [T2]

## 5. Shared chronology and the Solarian Week Index

Solarian does not require a common local year number across all inhabited worlds. Historical and machine interoperability instead requires a common precise chronology together with date conversion. For standard-day settlements, the **Solarian Week Index (SWI)** is a monotonically increasing counter of the common seven-day week, anchored to the frozen reference epoch. An orbital-month boundary in one world need not coincide with one in another; their standard-day weeks nonetheless lie on the same underlying grid.

Mars is different. Seven Martian sols take longer than seven standard days, so Mars cannot share the standard-week *physical phase* indefinitely. A Solarian Mars implementation retains uninterrupted local seven-sol weeks but maps them deterministically to common chronology and SWI. **A mapping is not permanent weekday identity across the two physical timescales.** [S1]

Precision event identifiers, ephemeris-model provenance, human-readable date syntax, time zone treatment and conversion APIs belong in the normative technical record. This overview intentionally does not improvise encodings or claim that a narrative example is a formal schema.

## 6. Evidence and status: what has actually been tested

The six synchronised planetary profiles assessed using the DE440 crossing methodology have a **28-form frozen release-candidate registry**, comprising 22 original book forms plus six supplemental forms. The extra forms occur at Jupiter (620 weeks), Saturn (1,535, 1,538 and 1,539), Uranus (4,385), and Neptune (8,600). The tested intervals are bounded; the catalogue is not an all-time guarantee. An unknown future length requires an immutable, source-supported versioned extension, not an improvised correction. [T1]

A separate **historical** asteroid diagnostic examined 19 Main Belt bodies using an archival CODES 2010 / DE405-era asteroid solution in a mixed-model analytical setup. It detected 69 body-specific forms: eight previously book-canonical and 61 generated supplemental candidate vectors. The author has ratified the **candidate-generation rule**, not those 61 results or the 19 asteroid profiles. The historical phase-review routes currently stand at **11 standard-potential, six marginal-review and two specialised-treatment** cases. No contemporary 19-body Horizons source-concordance or all-epoch certification has been executed. [T3][T4]

That evidentiary distinction is essential. Solarian can have a coherent and demonstrably useful mathematical structure without every future implementation, epoch or asteroid profile already being certified.

## 7. What a conforming implementation would still need

An implementation intended for operational use needs an exact technical release—not just this overview or the explanatory book. It must identify its calendar version and supported world, timescale and day model; the target, ephemeris and frame conventions; the frozen crossing and rounding rules; a versioned month/minth vector for every supported civil-year length; the official common-chronology and SWI transforms; deterministic parsing and formatting; and independently reproducible test fixtures.

It must also distinguish numerical phase applicability from broader scientific source qualification and author/governance acceptance. New astronomical data or newly encountered year forms must advance through versioned review without silently altering previously issued dates. Cultural naming is a separate local choice, not a source of ambiguity in machine identities. [T1][T2][T3][T4][T5]

## 8. Publication boundary

Solarian’s **book** is copyrighted explanatory work. Its **open protocol**, **reference tables**, **code** and **supporting data** have separately proposed or approved licensing policies that attach only to specifically identified files on authorised release. This standalone informative companion is issued under CC BY 4.0. It does not promise conformance, announce a normative-protocol DOI or constitute publication of the standalone normative Solarian Protocol v1.0.

**In one sentence:** Solarian keeps human operating time portable, the orbital year local, and the whole-week interface between them deterministic—while treating real astronomy, edge cases and the evidence needed to certify a calendar seriously.

## Sources and traceability

This overview is grounded in the author-approved *Solarian* manuscript (including Appendix G), and the frozen technical records identified in the accompanying **W3 Evidence Register** as [S1], [T1]–[T5]. Full registry filenames, authority status and SHA-256 identifiers are supplied there. Statements about asteroids are intentionally limited to the archival diagnostic; no modern source-validation claim is made.
