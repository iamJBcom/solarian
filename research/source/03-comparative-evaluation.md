# Solarian — Comparative Evaluation of Planetary Calendar Architectures

*A requirements-based assessment of shared Earth calendars, independent local calendars and a common multi-world grammar*

**Initial Public Issue 1.0 · October 2026 · Analytical comparison, not a scored scientific contest**

## 1. The comparison must start with the problem

Asking which planetary calendar is ‘best’ before specifying what it must do usually guarantees an argument about preferences. A timetable for a short Mars expedition does not need to solve the same problem as a calendar for a self-governing Martian city, and neither faces quite the same requirements as an archive or transport consortium operating simultaneously on Ceres, Mars and the moons of Saturn.

The purpose of this evaluation is narrower and more useful: **compare different calendar architectures against the ten design requirements explicitly established in Chapter 3 of *Solarian*.** The requirements are human-scale cadence; local astronomical identity; common chronology; cross-world interoperability; orbital legibility; continuous weekly structure; multi-scale scalability; bounded vocabulary; local cultural autonomy; and graceful failure. [S1]

No single set of weights is assumed. The same feature can be a strong advantage in one settlement scenario and a disadvantage in another. A local political community is entitled to value cultural continuity and astronomical meaning differently from an interplanetary standards organisation.

## 2. The alternatives being compared

**Architecture A — An Earth-derived common calendar everywhere.** Every settlement continues to use Gregorian dates, a UTC-derived common timeline and familiar terrestrial week/month/year nomenclature, supplementing it with local sol, phase or mission counters where necessary. This prioritises institutional continuity and interoperability. It need not be technologically primitive; modern precision timescales and location-specific astronomical information can accompany it.

**Architecture B — Fully independent locally designed calendars.** Each destination chooses its own civil year origin, month structure, day, week, intercalation, era and cultural vocabulary. Local communities can optimise their calendars for their own physical and social conditions. Conversion between calendars is an external software or institutional task rather than an inherent common grammar.

**Architecture C — Destination-specific local calendar plus shared chronology.** Each world has a local calendar, but all settlements also retain a precise common historical/event coordinate (for example a UTC-derived instant count). This is a credible hybrid and an important comparator: it delivers unambiguous date conversion without needing Solarian's shared mears or week structure. It is not the same as Architecture B if strong conversion rules are universally deployed.

**Architecture D — Synthetic common human years with local astronomical overlays.** Where a world’s orbit is very long, societies may preserve an Earth-like or otherwise chosen human-scale civil year, while treating the parent planet’s true orbit as a separate scientific or ceremonial cycle. This solves the ‘165-year year’ problem by reserving *year* for human recurrence. It is especially rational where local heliocentric phase does not govern everyday life.

**Architecture E — Solarian’s two-layer multi-world protocol.** Settlements share the day/week/minth/mear structural grammar, appropriate local orbital calendars, a fixed common astronomical orientation and deterministic conversion conventions. Synchronised worlds use integer R; short-orbit worlds can run the calendars independently; phase-proxy limitations are explicitly identified. This aims to retain the useful features of C and D while giving local dates additional shared structural meaning. [S1]

These are **architecture families**, not mutually exclusive historical products. In practice, the winning combination may use Earth chronology for records, a locally named civil calendar for residents, Solarian-like operating periods for organisations and an ephemeris for navigation. A fair evaluation must not treat hybrids as an illicit escape from a supposed competition.

## 3. Qualitative requirements matrix

In this matrix, **strong** means the architecture naturally addresses the requirement by design; **conditional** means it can with additional decisions, translation or overlays; **weak** means it has no intrinsic solution to that requirement. These are judgments under the multi-world design brief, **not empirical numerical scores**.

| Requirement | A. Earth everywhere | B. Independent local | C. Local + chronology | D. Synthetic year | E. Solarian |
|---|---|---|---|---|---|
| Human-scale cadence | Strong on Earth scale | Conditional | Conditional | Strong | Strong by design |
| Local astronomical identity | Weak without overlays | Strong if chosen | Strong if chosen | Secondary overlay | Strong where applicable |
| Common chronology | Strong | Conditional | Strong | Conditional | Strong with external chronology |
| Cross-world structural interoperability | Strong only because dates are the same | Weak without convention | Partial via conversion | Conditional | Strong by common grammar |
| Orbital legibility | Weak outside Earth | Conditional | Conditional | Weak unless overlaid | Tested; specialised limits |
| Unbroken local seven-position week | Strong if inherited | Conditional | Conditional | Conditional | Required |
| Multi-scale scalability | Stable but not local | One-off design burden | Scales via translation | Strong human-scale | Shared architecture scales with R |
| Bounded recurring vocabulary | Strong | Conditional | Conditional | Strong | Explicitly bounded |
| Local cultural autonomy | Limited in civil-date system | Strong | Strong | Conditional | Strong over structural identifiers |
| Graceful failure | Overlay-dependent | Case by case | Converter-dependent | Overlay-dependent | Explicit phase-applicability route |

The matrix illustrates trade-offs, not dominance. Architecture A’s uniformity gives a real advantage for existing Earth institutions. Architecture B has unbeatable latitude for local identity. Architecture C may be *quite sufficient* for a small network of worlds whose inhabitants rarely need to interpret each other’s operational periods. Architecture D solves recurring human-year needs elegantly, but may forfeit a locally astronomical meaning for the civil year. Architecture E attempts more simultaneous objectives and correspondingly imposes more shared definitions and implementation duties.

## 4. Comparing the architectures against practical scenarios

### Scenario 1 — A temporary scientific outpost

An expedition on Mars or an icy moon is controlled largely by an Earth-based agency, mission chronology dominates, and staff rotate through assignments. **Using Earth dates with local sol/shift counters (Architecture A) is often the sensible answer.** The overhead of adopting a novel local civil-year system may produce little benefit. Solarian has no automatic claim to be preferable merely because it is more systematic.

### Scenario 2 — A permanent, culturally distinctive Mars city

A self-governing Martian settlement may legitimately prefer a calendar whose years and seasonal divisions refer directly to Mars, while supporting familiar human operating periods. Architecture B or C can do this, including via a Mars-specific design such as Marian. Solarian also supplies Martian astronomical identity and portable minths, but it makes a specific trade: **665/672-sol whole-week civil years** in its idealised R2 structure rather than Marian's **668/669-sol years** with shortened terminal weekday-position sequences. A planet-specific choice is required; the comparison cannot be settled solely by calling one 'more accurate' or 'more regular'. [S1][M1]

### Scenario 3 — A network across Jupiter’s moons

Settlements on Europa, Ganymede, Callisto and artificial habitats need not share natural day lengths, daylight cycles or practical surface environments, yet share the same heliocentric orbital system. A Solarian Jovian **R13** calendar offers a common astronomical year and standard-day cadence without deriving civil days from any moon’s local orbital period. Architecture C can achieve unambiguous conversion but does not automatically supply a common Jovian operating language. The marginal benefit of E grows with the volume of intersettlement work and travel. [S1]

### Scenario 4 — Saturn or Neptune over generations

A Saturnian astronomical year lasts nearly thirty Earth years; a Neptunian one nearly 165. Architecture D can preserve a short synthetic *civil year* and keep the physical orbit outside everyday life. Solarian instead preserves the physical orbital year and lets an approximately 48-week *mear* carry human recurrence. Both approaches separate functions. The decision turns on whether local astronomical year identity and consistent terminology across other worlds are valued more than retaining the familiar social use of the word 'year'. [S1]

### Scenario 5 — A multi-world records and software ecosystem

A records service needs unequivocal timestamps, qualified calendar identities, conversion rules and version control. Architecture C may already provide all necessary machine interoperability. Solarian adds a shared weekly index, a finite structural A–L minth vocabulary and reusable world-profile semantics. The extra grammar may reduce ambiguity in collaborative planning, but it also requires implementers to adopt correct ephemeris versions, precise crossing rules and immutable year-form registries. A machine-only system should not be given credit for social advantages that have not been tested with users. [T1]

### Scenario 6 — A highly eccentric small body

A local calendar with equal elapsed-time months may give a misleading angular-phase impression near perihelion. This problem affects many calendar designs; it is not solved by choosing Solarian or independent local calendars as a label. Architecture B could deliberately use equal-angle months. Solarian explicitly identifies numerical phase failure and calls for specialised astronomical representation while retaining its human cadence and chronology. That is a defined route, **not yet a certified solved display for Juno, Bamberga or all trans-Neptunian objects**. [T2][T4]

## 5. Distinct trade-offs worth treating honestly

**Astronomical fidelity versus civil regularity.** A calendar built from whole uninterrupted weeks must quantise physical year boundaries. The difference between the physical crossing and the chosen week boundary can approach half a local week at an individual endpoint. Solarian manages this transparently, but another Mars-specific calendar can track the sol count more finely. Long-run fidelity and close *per-year* agreement are different attributes.

**Shared semantics versus local discretion.** A common A–L minth grammar, 100° origin and SWI coordinate help interoperability only if communities adopt them. They are deliberately small constraints compared with a uniform calendar, but they are real constraints. A future polity might reject a universal 100° direction on cultural or scientific grounds.

**Readable dates versus scientific precision.** Neither Solarian nor a customised planetary calendar replaces accurate ephemerides, location-sensitive solar times, mission times or a continuous precision timescale. Good civil representation is a different engineering objective from spacecraft navigation.

**Software ease versus specification scope.** Gregorian date libraries and UTC handling have enormous real installed bases. Solarian requires new libraries, reference fixtures, governance and migration interfaces. A beautifully regular local calendar that lacks dependable conversion and upgrade rules is not ready for commercial or legal use.

**Design coverage versus empirical confirmation.** Solarian’s bounded DE440 planet profiles and historical asteroid candidate classifications are encouraging; their scientific evidence is not equivalent to certified contemporary support for every possible world and year. Every rival proposal should be asked for equivalent evidence rather than judged by different standards. [T1][T4]

## 6. Findings by question, not an arbitrary winner

If the question is **'what should the next small Mars outpost use?'**, Earth dates plus sol counters may be the pragmatic answer. If it is **'which calendar best supports a particular Mars civilisation’s chosen notion of fidelity and recurring dates?'**, a specialised calendar such as Marian deserves serious consideration. If it is **'how can a civilisation across many astronomical homes share a calendar grammar while maintaining local orbital identity?'**, Solarian is a coherent and promising architectural candidate.

The distinction between the third and first two cases is the essence of the proposal. Solarian does not need to beat Gregorian at Gregorian’s existing job, or defeat Marian within every exclusively Martian design requirement, in order to contribute a useful multi-world standard.

## 7. Evaluation questions for independent adopters

A serious adopter should ask: Does the settlement actually need locally meaningful orbital months? Is a continuous weekday sequence a hard requirement? Are the public astronomical conventions and versioned year forms fully specified? Is the receiving organisation able to round-trip every civil date against a common timestamp? Are unknown year forms handled by a fail-closed update procedure? Do the proposed cultural names and operating cycles pass user testing? Is the standard phase proxy demonstrably adequate for that world, or is specialised phase information more honest? Can the institution migrate without destroying the historical meaning of existing records?

A final adoption decision must weigh costs, governance and local legitimacy, not merely the attractiveness of the Repeat Factor arithmetic. That is a strength of an open protocol approach: the claims and tests can be debated separately from the preference to adopt.

## Conclusion

**Solarian's primary comparative advantage is not that it makes every local calendar better. It is that it offers one recognisable structure for many different local calendars while retaining a useful distinction between human cadence and the orbit.** That advantage becomes more compelling as settlements and institutions span several astronomical homes. The same comparison reveals reasons to use other calendars in other circumstances. A credible evaluation should retain both findings.

## Evidence and method note

Requirements and systems architecture derive from the approved *Solarian* Chapters 3–9, 15–25 and Appendix E [S1]. The exact planetary year-form and phase limits derive from frozen technical records [T1]–[T4]. Marian descriptions reflect its current separately defined 12-month, 24-minth, 668/669-sol architecture [M1]; its comparative merits are analytic judgments, not externally tested human preferences. This evaluation used a qualitative requirements matrix; **no scientific ranking scores or adoption surveys were created**.
