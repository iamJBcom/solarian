# Solarian — A Long-Term Recommendation for Multi-World Civilisation

*Why a common calendar architecture may ultimately be preferable to a collection of unrelated planetary calendars—and what would justify choosing otherwise*

**Initial Public Issue 1.0 · October 2026 · Explicit author's policy case, not a neutral scientific verdict**

## The proposition

If future human civilisation remains concentrated on Earth with a handful of temporary stations elsewhere, there is no compelling reason to require an elaborate common planetary calendar architecture. Gregorian dates, scientific timestamps and local operational counters already solve many of those problems well.

But imagine a different future: multiple permanent societies, independent commercial systems, generations born on other worlds, movement between settlements and legal records that remain important for centuries. The question changes. Each world will possess its own environment, orbital year, community and calendar traditions, yet the wider civilisation will still need a shared language for planning and time-based identity.

**My recommendation is that a mature multi-world civilisation should seriously consider Solarian as its long-term common *calendar architecture*, while retaining local naming, cultural and implementation autonomy.** This is not a recommendation to abolish Gregorian chronology, impose identical dates on every world or compel current Martians to surrender a calendar they have legitimately adopted. It is a case for building future compatibility into the foundations before a landscape of incompatible local standards becomes costly to reconcile.

This position follows from the operating requirements developed in *Solarian*, not from a claim that the author has proved all future people will prefer its rhythms. It remains a proposal for independent evaluation, improvement and voluntary institutional acceptance. [S1]

## 1. Why ordinary custom planetary calendars may not be enough

A calendar designed solely for one destination can make excellent local choices. It can match that world’s day, annual origin, month structure, seasons, religious calendar, language or historical conventions. Indeed, Mars has already inspired coherent but substantially different designs, including Darian, Šurán, Zubrin, Exodus and Marian. Their differences are rational responses to different objectives. [R1]–[R5]

The coordination problem appears only when the local systems must coexist. Imagine contracts timed around a Martian sol-based month, maintenance programmes using a Cererian year, work on Ganymede planned against Jovian phases, and historical archives maintained on Earth. Precision timestamps can make their events mathematically comparable. They do not by themselves give ordinary staff, students, travellers or negotiators shared *calendar meaning*—a common understanding of a week, medium-sized operating period, orbital month, year boundary or recurrent planning cycle.

A completely custom local approach can add translation tables, shared document standards and scheduling software. That is a valid architecture, especially for a small interplanetary network. But if dozens of settlements develop unrelated conventions, a new calendar becomes not only a local civic decision but an interoperability project every time systems must connect. Solarian's proposition is to standardise a deliberately limited grammar in advance, leaving cultures free to name and celebrate it as they choose.

The core principle is **common structure; local culture**. That is a smaller and more realistic request than common dates and common names.

## 2. Why Solarian provides a plausible common grammar

Solarian's portability comes from four structural choices.

First, it provides a human **day → week → minth → mear** cadence that does not expand in proportion to the local heliocentric orbital year. A Saturnian orbit can contain 32 complete mears and a Neptunian one 179 without forcing schools, businesses and personal life to wait decades for an annual-sized recurring period.

Second, it preserves the right of each world to a locally meaningful astronomical **month → year** coordinate. The year belongs to the orbit. For Jupiter's moons or Saturn's moons, a system-wide heliocentric calendar may be the natural annual home, while their individual moon cycles remain useful operational data.

Third, where the two layers nest cleanly, the integer **Repeat Factor** expresses their relationship simply: R minths per orbital month and R mears per orbit. Where that nesting becomes unhelpful, the human and astronomical sequences remain independent. This is a controlled choice, not an exception invented after meeting Mercury and Venus.

Fourth, Solarian protects continuous local seven-position weeks and uses registered complete-week adjustments rather than silently interrupting weekday identity to satisfy astronomy. Standard-day worlds can share a common week coordinate; Mars uses its sol-based calendar locally and maps to that common chronology. [S1]

Together, these choices reduce the number of concepts a traveller or software implementer must relearn at every new destination. They also make it possible to say exactly which elements are globally agreed and which remain local.

## 3. The strongest Mars-specific objection: why not Marian?

**Marian is a serious competing answer for Mars, not a straw man.** It is a purpose-built Martian calendar with twelve months per year and two minths per month, making 24 minths. The year contains 668 or 669 sols rather than the 665/672-sol whole-week forms of a synchronised Solarian Mars implementation. Marian’s 27/28-sol minths preserve a familiar operating size; its designated shortened terminal civil weeks allow years, months and minths to begin in the same weekday position. The price is that the ordinary seven-position weekday sequence is occasionally shortened. No physical sol disappears. [M1]

That is a legitimate design choice. Marian’s shorter per-year differences from Mars’s mean orbital sol count are an advantage for applications that prioritise close annual duration and recurring date–weekday relationships over uninterrupted weekly continuity. Solarian cannot claim to be superior on those dimensions merely by pointing to a neat Repeat Factor.

**Solarian makes a different choice.** It insists that the local week remain a continuous seven-position sequence. If the true year lies between whole-week lengths, the closest week-aligned astronomical boundary can be several sols away in a particular year. The structural loss is calendrical annual granularity, not necessarily unbounded long-term drift: the dated reference-ray crossing rule determines and periodically readjusts the boundaries. Appendix G explains why implementation must respect real crossings rather than assume a fixed two-form cycle. [S1][T1]

Whether the trade is worthwhile depends on the purpose. For an **independent, overwhelmingly Mars-focused society**, Marian might reasonably be preferred. For a **Mars that expects sustained institutional interaction with Ceres, the giant-planet systems and artificial habitats**, Solarian's intact weekly grammar and common structural identities have a stronger network argument. The recommendation for Solarian is therefore **long-term and multi-world**, not a categorical rejection of Marian.

## 4. Why a shared continuous week matters

A week is a surprisingly consequential civil convention. Work schedules, rest and worship, education, healthcare rosters, maintenance, reporting, subscriptions and family recurrence all rest on its repeated structure. Solarian chooses to keep that seven-position sequence intact locally, even when it means changing an orbital-year length by a complete week relative to an idealised duration.

This does not imply that every future community must use today's terrestrial weekday names or identical working days. Nor does it make seven Martian sols physically equal to seven Earth days. Solarian expressly distinguishes the local seven-sol week from the standard-day SWI sequence. The recommendation is simpler: do not require an ordinary settlement to interrupt its local sequence of weekday *positions* merely to repair a higher-level orbital mismatch.

That principle is especially attractive in a multi-world environment, where the week can serve as common operating syntax while local solar days, astronomical years and languages differ.

## 5. Astronomy is not an argument against the architecture

A common calendar must be scientifically honest. Actual planetary crossing intervals are not perfectly uniform, and rounding the two ends of an orbit independently can produce more civil year lengths than an idealised constant-period model suggests. For Saturn, the bounded DE440 calculation found 1,535-, 1,536-, 1,537-, 1,538- and 1,539-week civil years; the main book's two adjacent examples remain a teaching model, not the complete empirical form set. [T1]

Solarian's answer is **not** to force astronomical events into the two convenient lengths. It calculates the real year boundaries, selects an exact registered whole-week year form and distributes corrections through approved expansion joints. Most minths remain normal. In a 384-minth Saturnian year, even an adjustment of three weeks is small relative to the total, and Saturnian orbital years themselves are almost thirty Earth years long.

Any civil calendar wishing to reflect real orbital events must deal with natural variation through intercalation, astronomical calculation, recalibration or accepted drift. It is more credible to declare where variation is absorbed than to claim that a clean idealised mean period is the complete physics. A uniform mean model has a proper explanatory role; astronomical reality has the final implementation role.

There is a boundary. Solarian's twelve approximately time-regular orbital months may become a poor proxy for geometric orbital phase on eccentric worlds. The ratified phase-fidelity standard specifies 30° and 45° review boundaries. Mercury requires specialised phase representation in the tested window; two historically screened asteroids, Juno and Bamberga, are routed for specialised treatment, but their final contemporary profiles are **not certified**. The recommendation is for a framework with an honest applicability test, not a false guarantee of a perfect twelve-month dial everywhere. [T2][T4]

## 6. Objections a future standards body should take seriously

### ‘Why not simply retain Gregorian everywhere?’

It may be the best near-term practical choice. Gregorian has enormous cultural, legal and software incumbency, and a shared historical coordinate remains valuable indefinitely. But it does not by itself give a permanent settlement a calendar whose orbital year belongs to that settlement. Solarian is compatible with a separate Gregorian or scientific common chronology rather than attempting to replace it.

### ‘Why should a civilisation impose a human-scale mear of roughly 48 weeks?’

It should not impose it without consent. The choice builds on existing whole-week operating practice and a deliberate separation of human cadence from astronomy. Its usability, naming and recurrence need human-factors validation. The proposed advantage is cross-world portability and intelligibility, not a theorem that every culture will find a mear optimal.

### ‘Why not let every world choose its own calendar, and let software convert?’

That may suffice for precise event timestamps. The stronger Solarian argument concerns **shared structural interpretation** for people and institutions, not mere machine conversion. A converter can say two dates represent the same instant; it does not automatically make their operating periods comparable or memorable. Solarian offers one option for that extra human coordination layer.

### ‘Why should Mars accept less precise year-length steps?’

It might not. Marian's 668/669-sol years offer a real Mars-specific advantage in closer annual granularity. Solarian instead optimises uninterrupted weeks and cross-world syntax. If the settlement's priorities favour Marian, choosing Marian can be rational. The case for an interoperable long-term ecosystem should be made with explicit trade-offs, not by disparaging the local alternative.

### ‘What if a planet has the wrong orbit for standard twelve-month phase labels?’

Then Solarian should say so. An independent human calendar and physical chronology can continue while a specialised astronomical phase display is developed and tested. Graceful failure is a feature only if the limitation is recorded openly and no unvalidated specialised profile is presented as ready.

### ‘Isn't this premature standardisation?’

Potentially. Standards can fossilise assumptions before users exist. The remedy is to publish a versioned open proposal now, invite third-party implementations and preserve future local governance, **not** to demand universal adoption immediately. Naming rights, cultural decisions and many operational conventions should remain local.

### ‘Are the tests complete enough to recommend it?’

Complete enough to recommend independent evaluation—not yet complete enough to claim scientific certification of every destination. Bounded planetary ephemeris tests, a ratified phase criterion and a candidate generator establish substantive technical groundwork. Contemporary asteroid source matching, individual profile certification, uncertainty handling, independent code conformance and human-factors evidence remain open. [T1]–[T5]

## 7. A prudent adoption pathway

A sensible future progression would start with **non-authoritative parallel trials**: publish the specification and selected certified demonstration profiles; provide reference converters alongside Gregorian/UTC or successor chronology; run independent implementation and test-fixture comparisons; and ask future settlement stakeholders to evaluate cultural and operational usefulness rather than treating the present author's preferences as binding.

Once there is evidence of interoperability, communities could choose to adopt the Solarian structural grammar while retaining local names, holidays, business periods and civil traditions. Existing date records should remain anchored to explicitly versioned calendars and common timestamps; a future transition must never silently reinterpret historical dates. Decisions affecting real civil life require local governance rather than unilateral software upgrades.

The long-term objective is **compatibility by shared grammar**, not uniformity by administrative decree. It is a standard that settlements could own collectively, scrutinise independently and extend deliberately as the Solar System's human geography develops.

## Conclusion: what I recommend—and what I do not

I recommend Solarian as a **serious long-term common architecture** for a world of many permanent, interacting settlements. Its strongest reason is not the beauty of any single numerical example. It is the separation of responsibilities: stable human operating time, truthful local astronomical time, and an intentionally small shared structure connecting them.

I do **not** recommend treating that architecture as proven inevitable, declaring Marian wrong for Mars, suppressing other workable calendars, certifying untested asteroid profiles, or asking settlements to abandon local cultural authority. The proposal should remain publicly testable and capable of revision.

A reliable operating architecture is not one that makes reality obey a neat diagram. It is one whose structure can remain intelligible when reality becomes complicated. **Solarian is worthy of serious consideration because it was designed to absorb that complication without losing the underlying grammar.**

## Authority and source note

This document is intentionally a **recommendation by the proposer**, not an independent endorsement. The architecture and requirements derive from the author's Solarian book [S1]; the planetary tests and applicability constraints are [T1]–[T5]; the distinct Marian architecture is [M1]. The prospective benefits to workers, settlers, institutions and cultures are design hypotheses requiring evaluation. Publication requires separate author approval, and public adoption would require substantially broader evidence and legitimacy.
