# Reform-Event Definition and Sub-Typing Protocol

**Version:** v0.1
**Stance:** Architect (drafting). Reviewers: Guardian + domain consultant for whichever archive is being studied. Pending.
**Parent documents:** *Human-System Timescales: Scoping v0.2* (§5 M1, reform-event definition; Architect M1 second bullet); *Task Cards v0.1* (TC-07).
**Companion protocol:** `human-timescales-commensurability-protocol-v0.1.md` (TC-06). The two together gate TC-01.
**Feeds:** TC-01 (Catholic ecumenical councils pilot — gating prerequisite); TC-04 (T10 archive characterisation — recommended); TC-08 (defunct-archive feasibility — recommended).
**Date:** 2026-04-27

---

## 0. Endorsement Marker (provisional)

Internal methodological infrastructure. Not a Coastline. No external endorsement is asserted. This protocol carries no empirical claim of its own. Its function is to fix the conditions under which an event in an institutional archive is admitted as a reform event and how that event is typed.

## 0a. Non-prescription clause (inherited)

Per `CONVENTIONS.md` §6 and scoping v0.2 §0a. Classification of an event as a reform event under this protocol is descriptive. It carries no judgement that the reform was correct, beneficial, or legitimate; nor that its absence would have been incorrect, harmful, or illegitimate. **A floor is not a target.** The taxonomy serves measurement, not advocacy.

---

## 1. Purpose

Reform-cycle archaeology (M1) requires that two distinct measurement choices be settled before counting begins:

1. **What counts as a reform event** (inclusion).
2. **What kind of reform event it is** (sub-typing).

Both choices are contestable. Both must be operational enough that two independent coders, working from primary and secondary sources, agree in ≥80% of cases on inclusion and on sub-typing — the success criterion declared in the TC-07 card. This protocol fixes those two choices for TC-01 and any downstream M1-method work, and specifies a domain-equivalent mapping for non-ecclesial archives (TC-04, TC-08).

It is binding: any reform-event count or sub-type-stratified analysis issued without explicit invocation of this protocol (or a successor version) is inadmissible under v0.2 §5 M1.

---

## 2. Base definition (from scoping v0.2)

Per scoping v0.2 §5 M1 (binding, Scout signal 3, prerequisite):

> **Reform = structural change in decision rights or membership rules, evidenced by documentary ratification.**

This protocol does not modify the base definition. It operationalises it by specifying inclusion and exclusion tests, then sub-typing the included events.

---

## 3. Inclusion test (necessary conditions)

An event is admitted as a reform event if and only if **all three** of the following are satisfied. Each is a necessary condition; together they are sufficient.

### 3.1 Documentary ratification

The event produced a ratified, documentary artefact: canon, decree, constitution, charter revision, council acta, or formally adopted recommendation, traceable to a primary source. Drafts, proposals, and unratified working documents do not satisfy this condition. Verbal declarations later attested in secondary literature without primary documentary trace do not satisfy this condition.

### 3.2 Structural change in decision rights or membership rules

The artefact effects (or formally claims to effect) a change in *at least one* of:

- **Decision rights** — who is entitled to deliberate, to vote, to ratify, to overrule, to authorise, or to bind; under what procedural conditions; over what scope.
- **Membership rules** — who counts as a member of the institution, what the conditions of admission and exclusion are, what obligations and entitlements attach to membership.

A re-affirmation of an existing rule, with no change in scope, procedure, or class of bound parties, does not satisfy this condition. A re-statement in updated language without operative change does not satisfy this condition.

### 3.3 Multi-domain-legitimacy applicability

The event is applicable to an institution within the H₀ scope (multi-domain legitimacy, per scoping v0.2 §1). For TC-01 this is automatic. For TC-04 (T10 institutions), applicability is determined per the T10 archive schema's `multi_domain_legitimacy` field; events tagged `bounded-technical` are recorded but excluded from the reform-event count for H₀ tests, and are routed to the technical-event count instead. Events tagged `partial-multi-domain` are included with a flag.

---

## 4. Exclusion test (what does not count)

The following are explicitly excluded, even where condition 3.1 is satisfied:

- **Re-affirmation without operative change.** A council that re-states existing canon law in a new collection without changing decision rights or membership rules.
- **Administrative adjustment.** Changes to internal scheduling, document numbering, archival format, ceremonial protocol, or accounting procedure that do not bear on decision rights or membership.
- **Rebranding.** Renaming an office or body without changing its powers, scope, or selection. Architectural relabelling without architectural change. (R6 in scoping v0.2 — reform fashion as data — applies here; rebranding is itself a datapoint about fashion, but it is not a reform event.)
- **Personnel succession.** Routine election of a new pope, executive director, or council president under unchanged rules. (Contested successions that prompted rule changes are reform events under condition 3.2 via the rule change, not via the succession itself.)
- **Pastoral instruction without canonical force.** For TC-01, encyclicals, apostolic letters, or motu proprio actions that exhort but do not change canon law are excluded. (They may still appear in TC-04 as technical-layer events for analogous T10 institutions.)
- **Liturgical revision** in TC-01, *unless* the liturgical change effected a corresponding change in disciplinary obligations on members (e.g., Trent's Mass standardisation enforced via canon).

Boundary cases in any of these categories are flagged in the data record (`subtype_notes` for TC-01, `notes` for TC-04) and adjudicated by the inter-coder process specified in §7.

---

## 5. Sub-types

Three sub-types. Definitions are operational. Sub-types are not exclusive — multi-tagging is required where the event satisfies more than one (see §6).

### 5.1 Doctrinal

**Definition.** The reform changes what the institution authoritatively asserts to be true, or changes the institution's procedure for adjudicating truth-claims within its scope.

**Indicators.**
- Promulgation, modification, or anathematisation of a creed, dogma, or formal teaching.
- Definition of orthodoxy or heresy.
- Change in the procedure by which doctrinal questions are settled (e.g., conciliar versus papal definition).

**TC-01 examples.** Nicaea I (Nicene Creed against Arianism); Chalcedon (Christological two-natures definition); Trent (doctrinal reaffirmation against the Reformation); Vatican I (papal infallibility).

**Anti-examples.** Disciplinary canons of Trent are not doctrinal (they are disciplinary, §5.3). A council that does not promulgate or modify any teaching is not doctrinal even if it discusses doctrine.

**T10 / non-ecclesial mapping.** Doctrinal-equivalent reform in technical-coordination institutions is rare and consequential when it occurs: changes in what counts as authoritative knowledge or as a valid technical specification. Examples include changes to "rough consensus" criteria, formal adoption of new standards classes, or changes in the boundary between recommendation and binding specification.

### 5.2 Structural

**Definition.** The reform changes the institution's governance, hierarchy, jurisdiction, or constitutional architecture: who decides what, on whose behalf, under whose authority.

**Indicators.**
- Charter revision, mandate change, or sovereignty transition.
- Creation, abolition, or reassignment of offices or bodies.
- Change in jurisdictional scope or in inter-institutional accountability.
- Change in the procedure by which authority is transferred between cohorts.

**TC-01 examples.** Lateran IV (consolidation of papal authority over local episcopate); Constance (conciliarist resolution of the Western Schism); Vatican II (episcopal collegiality, role of the laity in governance).

**Anti-examples.** A purely doctrinal council that does not touch governance is not structural. A liturgical revision is not structural.

**T10 mapping.** This is the dominant category for T10 governance-layer events. ICANN/IANA stewardship transition (1998–2016) is the paradigmatic example; IETF Administration LLC formation (2018) is a clean second case; W3C 2023 reorganisation is a third.

### 5.3 Disciplinary

**Definition.** The reform changes what members are required to do or refrain from doing in their institutional role, including conduct, sacramental practice, or operational obligations.

**Indicators.**
- Canons on clerical conduct (celibacy, simony, residency).
- Sacramental practice rules.
- Lay obligations imposed or rescinded.
- Operational or procedural rules binding on members.

**TC-01 examples.** Many medieval councils on clerical conduct; Trent's disciplinary canons (alongside its doctrinal work — multi-tagged); Lateran reforms on simony.

**Anti-examples.** A doctrinal definition with no behavioural implication for members is not disciplinary. An administrative adjustment to internal scheduling (excluded under §4) is not disciplinary.

**T10 mapping.** Operational rules for participants: RFC publication requirements, contributor licence agreements, code-of-conduct adoptions or revisions, disclosure rules.

---

## 6. Multi-tagging procedure

A reform event may carry one, two, or three sub-type tags. Multi-tagging is required where the event satisfies more than one sub-type's indicators.

- **Required where evidence is positive.** If the event's documentary record evidences both a doctrinal definition and a disciplinary canon, it is tagged `subtype_doctrinal = TRUE` *and* `subtype_disciplinary = TRUE`. Single-tagging by judgement of "predominant" character is forbidden in v0.1; predominance assessments are too coder-dependent and would defeat the inter-coder reliability target.
- **Aggregation forbidden across sub-types.** L₅ may hold for one sub-type and not others (per scoping v0.2 §5 M1). Statistical analyses must report sub-type-stratified results separately. The sub-type-stratified analyses are the headline; any aggregate is supplementary, not primary.
- **At-least-one rule.** Every admitted reform event must carry at least one sub-type tag (the M1 schema validation enforces this in `data/m1-catholic-councils/schema.md`). If no sub-type fits, the event likely fails the inclusion test (§3) and should be re-examined.

---

## 7. Inter-coder reliability

The TC-07 success criterion is ≥80% agreement between two independent coders on (a) event inclusion and (b) sub-typing. This is an operational benchmark, not a statistical claim.

### 7.1 Procedure

1. **Sample.** Select a calibration sample of 6–8 councils (TC-01) or 6–8 candidate events (TC-04) that span the sub-types and the era range. Avoid hand-picking only the easy cases.
2. **Independent coding.** Each of two coders applies this protocol to the sample using primary and secondary sources, recording inclusion and sub-type tags per event. Coders work without communication during this phase.
3. **Compare.** Compute (a) inclusion agreement: percentage of events on which both coders agreed on inclusion/exclusion; (b) sub-typing agreement (conditional on both coders including the event): percentage of sub-type tags on which both coders agreed.
4. **Threshold.** Both percentages must reach ≥80%. If either falls short, the protocol is refined (with the disagreements as evidence) and the procedure is re-run on a fresh sample.
5. **Cohen's κ supplementary.** Cohen's κ is computed alongside the percentage measures. κ ≥ 0.6 is reported as additional evidence; below 0.6 with ≥80% raw agreement, the protocol is flagged for re-examination on grounds of chance-agreement risk.

### 7.2 Pilot before full archive

The calibration is run *before* the full archive (TC-01: all 21 ecumenical councils) is coded. Coding a 21-event archive only to discover at the end that inter-coder reliability fails is a wasted investment. The pilot is small, cheap, and protective.

---

## 8. Procedural falsification

None at the protocol level — this is methodological infrastructure, not an empirical claim. However: **any reform-event count or sub-type-stratified analysis that does not declare its protocol per this document, or declares this protocol but fails the §7 inter-coder reliability check, is inadmissible.** As with TC-06, the inadmissibility is procedural, not evidentiary; the underlying coding may be re-validated under a corrected invocation.

A second-order constraint: a reform-event count issued under this protocol but invoking only one coder is **provisional**, not admissible as evidence for or against H₀ until inter-coder validation has been performed.

---

## 9. Open questions

- **Q-RE1.** Encyclicals and motu proprio actions (TC-01) are excluded under §4 unless they effect canonical change. The boundary between "exhortative" and "canonically operative" papal acts is contested; some twentieth-century papal acts have arguably done canonical work without conciliar form. Domain consultant review requested.
- **Q-RE2.** The T10 doctrinal-equivalent category (§5.1) is thin. If TC-04 finds no T10 doctrinal events meeting the inclusion test, the sub-type may be dropped from the T10 analysis, with the absence itself reported as a finding (technical-coordination institutions may simply not do doctrinal reform). The protocol does not pre-judge this.
- **Q-RE3.** Multi-tagging strictness (§6) sets the bar at "evidence is positive" rather than "predominant character." This produces more multi-tags but tighter inter-coder reliability. Guardian invited to veto if the strictness produces excessive multi-tagging that defeats the sub-type-stratified analysis.
- **Q-RE4.** Defunct-institution archives (TC-08) may have asymmetric documentary survival that makes the inclusion test (especially §3.1, documentary ratification) systematically biased. The protocol does not yet specify how to handle systematically-degraded documentary states. TC-08 feasibility memo will inform v0.2.

---

## 10. Document control

- **v0.1** (2026-04-27): Initial draft under Architect invocation, in response to TC-07 authorisation. Operationalises the scoping-v0.2 reform-event definition into three-condition inclusion test, six-category exclusion test, and three sub-types with operational definitions and indicators. Multi-tagging required where evidence is positive; predominance-based single-tagging forbidden in v0.1. Inter-coder reliability procedure specified (≥80% raw agreement on inclusion and sub-typing, with κ supplementary). T10 / non-ecclesial mappings provided for each sub-type.
- **v0.2 horizon:** review pass by Guardian and (where applicable) domain consultant. Q-RE1–Q-RE4 to resolve. Possible promotion of multi-tagging strictness if the v0.1 setting produces excessive multi-tags. Possible defunct-archive sub-protocol if TC-08 finds systematic documentary asymmetry.

**Stance log.** Drafted Architect, in companion form to TC-06's commensurability protocol. The strictness of §3 (three necessary conditions, all required) consciously errs toward exclusion; the strictness of §6 (multi-tag where positive) consciously errs toward inclusion *within* the sub-type taxonomy. The combined effect is a smaller admitted-event count with denser tagging — a deliberate trade favouring inter-coder reliability over event-count maximisation.

**Linked.** `docs/scoping/human-timescales-scoping-v0.2.md` §5 M1, §1 (multi-domain-legitimacy scope); `docs/task-cards/human-timescales-task-cards-v0.1.md` TC-07, TC-01, TC-04, TC-06, TC-08; `docs/protocols/human-timescales-commensurability-protocol-v0.1.md`; `data/m1-catholic-councils/schema.md`; `data/t10-archive/schema.md`.
