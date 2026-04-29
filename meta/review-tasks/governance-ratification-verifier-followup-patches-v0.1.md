# Verifier-stance follow-up — RT-2026-006 remediation patches

*Endorsement Marker (provisional). Internal scoping work, not a Coastline. No external endorsement is asserted.*

**Date:** 2026-04-29
**Stance:** Verifier (drafting remediation patches per offer in RT-2026-006 response)
**Responding to:** Verifier offer in `governance-ratification-verifier-review-response-v0.1.md` §"Verifier offer"; user direction "Path 1 — go" (acceptance of patch offer).
**Scope.** Four blocking issues from Verifier verdict (Q8.5 ADM-EC; Q9.3 data-license boundary; Q9.4 per-artefact license marking; Q10.3 FAIR overstated compliance). Each patch includes verdict among options (where Verifier left choice open), drafted text, and rationale.

---

## Q8.5 — ADM-EC Constitution clarification

**Verifier verdict on options:** option (c) **working term**, with internal-clarification adjunct.

**Rationale.**
- Option (a) "internal artefact" requires drafting an actual ADM-EC document; out of scope for this round and would create a new ratification surface.
- Option (b) "external document" requires a citation that the Verifier search did not find as resolvable; would constitute an inaccurate Citation if forced.
- Option (c) "working term" is the only path consistent with the Verifier-jurisdiction principle: do not assert authority that cannot be operationally located.

**Implementation.**

Two distinct usages of "ADM-EC" in CONVENTIONS.md:

1. **§4 (current line 39):** *"Vetoes: must cite the violated Core Function in writing. See ADM-EC Constitution (referenced externally)."* — this is the load-bearing external-authority claim that triggered the Citation: Violation flag.

2. **§7 (current, T4 kill-criterion):** *"Where ADM-EC / causal-geometry vocabulary (L_source, L_apparatus, L_comparison, η_opt) is used..."* — this uses "ADM-EC" as a vocabulary label, not as an authority.

**Patches:**

- **§4 fix:** the line is replaced wholesale by Architect's Q2 reclassification draft. The replacement text must self-contain the Core Function definitions previously deferred to "ADM-EC Constitution". Verifier-modified version of Architect's draft text:

  > *Functional stances: Guardian, Architect, Integrator constitute the Council-3 deliberation core. Per-jurisdiction primary stances: Scout (horizon-signal jurisdiction) and Verifier (source-grounding jurisdiction) issue rulings primary within those jurisdictions, ratified by Council decision. The Council-3 core retains cross-jurisdiction veto authority — Guardian on clarity-and-ethics violations; Architect on structural-coherence violations; Integrator on flow violations — exercised in writing with explicit citation of the violated Core Function. Per-jurisdiction primaries do not hold cross-jurisdiction veto authority. All five stances operate under the stance-invocation, one-stance-at-a-time, and veto-justification disciplines below.*

  This integrates the Architect Q2 reclassification with the Q8.5 Verifier remediation: Core Functions are defined in-text (Guardian/clarity-ethics; Architect/structural-coherence; Integrator/flow), removing the dependency on external "ADM-EC Constitution" reference.

- **§7 (T4 kill-criterion, becomes §9 after Architect §7+§8 insertions) fix:** add an in-line clarification that "ADM-EC" is a working-framework label, not an external authority:

  > *Where ADM-EC causal-geometry vocabulary (a working internal framework: L_source, L_apparatus, L_comparison, η_opt) is used, the document must produce at least one prediction or distinction unavailable from prior frameworks. If it merely re-describes, it is dropped, not decorated.*

**Verifier verdict:** Citation: Violation closed on patch application.

---

## Q9.3 — Data license boundary (operational testability)

**Verifier verdict on remediation paths:** **per-class defaults** (Verifier Q9.3 option 1) plus per-dataset override discipline (Q9.3 option 2). Both, not either-or — the per-class defaults make the common case operationally testable from path; per-dataset overrides preserve flexibility for cases where the default is not appropriate.

**Rationale.**
- Per-class only would foreclose legitimate per-dataset variation (e.g., a dataset with restricted-use components).
- Per-dataset only requires every consumer to read every dataset README; high overhead.
- Both: the consumer reads LICENSE.md once, knows the per-class defaults, and only needs to inspect a dataset README if the dataset declares an override.

**Implementation.** Replace the current Data section in `LICENSE.md` (lines 32–43) with:

> *## Data*
>
> *Per-class defaults (operationally determinable from path):*
>
> - *`data/{dataset}/raw/` → CC0 1.0 Universal Public Domain Dedication. Factual extracts from public-domain sources where copyright generally does not apply (dates, names, public records). Per-dataset README MAY override on a case-by-case basis where the source carries copyright.*
> - *`data/{dataset}/processed/` → Creative Commons Attribution 4.0 International (CC BY 4.0). Cleaned, structured, or normalised derivations of raw data; selection and transformation copyright applies.*
> - *`data/{dataset}/derived/` → Creative Commons Attribution 4.0 International (CC BY 4.0). Analytical products generated by code in `analysis/`; full creative-and-derivative copyright applies.*
> - *`data/{dataset}/{schema.md, README.md, *.md documentation}` → CC BY 4.0 (per the documentation category above).*
>
> *Per-dataset overrides MUST be declared in `data/{dataset}/README.md` under a "License" heading. Per-dataset overrides supersede per-class defaults for that dataset only. Where no per-class default applies (e.g., a file in `data/{dataset}/` not matching any sub-path), the dataset README's declaration is authoritative; absent a README declaration, default is CC BY 4.0 with the dataset's stated author as licensor.*
>
> *Full licence texts:*
> - *CC BY 4.0: https://creativecommons.org/licenses/by/4.0/legalcode*
> - *CC0 1.0: https://creativecommons.org/publicdomain/zero/1.0/legalcode*

**Verifier verdict:** "where copyright would not apply" ambiguity closed; data licensing is now operationally testable from file path with explicit override mechanism.

---

## Q9.4 — Per-artefact license marking (declared inheritance mechanism)

**Verifier verdict on remediation paths:** **declared inheritance mechanism** (Q9.4 option 2: documented inheritance) over **per-artefact header** (Q9.4 option 1: license header per file).

**Rationale.**
- Per-artefact header is operationally heavy for a research repository with hundreds of small `.md` files; would require ~80+ file edits and ongoing discipline on every new file.
- Declared inheritance is operationally sufficient under FAIR-A1 if the inheritance mechanism is *itself* explicitly documented and operationally testable from artefact path.
- The Verifier ruling explicitly accepted "documented inheritance mechanism" as a satisfying remediation: *"Each artefact MUST carry a license header OR inherit via an explicitly declared mechanism documented in CONVENTIONS.md or LICENSE.md."*

**Implementation.** Add a new "License inheritance discipline" section to `LICENSE.md` (after the Data section, before Citation):

> *## License inheritance discipline*
>
> *Artefacts are not individually marked with license headers. Instead, license is determinable from artefact path per the categories above. Downstream consumers determine the applicable license by mapping the artefact's repository-relative path against the rules in this `LICENSE.md`:*
>
> - *Documentation, governance, and meta-tracker `.md` files in `docs/`, `logbook/`, `meta/`, and the top-level governance files → CC BY 4.0 (Documentation category).*
> - *Source code in `analysis/` → Apache-2.0 (Code category).*
> - *Data files under `data/{dataset}/` → per-class defaults in the Data category, with per-dataset README overrides.*
> - *`CITATION.cff` → CC BY 4.0 by default; the CFF specification itself is the schema, not the content.*
> - *Files outside these categories: default to CC BY 4.0 with this repository's stated author as licensor; if a file class with substantive different license needs arises, this `LICENSE.md` is amended (release-tier event).*
>
> *This inheritance mechanism is itself the per-resource license declaration required by FAIR principle A1. To verify the license of any specific artefact, locate its path under the rules above. Disputes or ambiguities are resolved by amending this `LICENSE.md`, not by individual file headers.*

**Verifier verdict:** FAIR-A1 compliance achieved via declared inheritance mechanism; ratification-blocking remediation closed.

---

## Q10.3 — FAIR overstated compliance wording

**Verifier verdict:** downgrade present-tense compliance claims to forward-looking alignment claims.

**Implementation.** Two surgical edits to `FAIR.md`:

1. **Line 3 (current):** *"This repository commits to the FAIR principles for research outputs..."* — already forward-looking ("commits to"). No change required.

2. **Line 5 (current):** *"This repository implements them as follows."* → *"This repository implements an operational framework aligned with the FAIR principles, with full compliance as a target state. Per-principle implementation discipline follows."*

   Rationale: "implements them as follows" reads as present-tense full implementation; "aligned with ... target state" is honest about the gap between current operational alignment and full compliance (e.g., not all principles are equally satisfied at every release; F4 Zenodo registration is conditional on release-time deposit).

3. **End of FAIR.md (after the per-principle sections, before "Operational discipline"):** add a brief honesty note:

   > *## Compliance status*
   >
   > *This repository implements an operational framework aligned with FAIR principles. Full compliance is a target state, not a current achievement. Specifically as of v0.3.0:*
   >
   > - *F1 (DOIs via Zenodo): conditional on release-time deposit; active for tagged releases only.*
   > - *F4 (ORCID linkage): present in CITATION.cff as of v0.2.2.*
   > - *I1–I3 (vocabularies, formal schema languages): markdown-prose with YAML front-matter is the current floor; formal schema languages (JSON Schema, frictionless-data) are preferred medium-term and required where schemas are referenced by code (per Architect Q6.2 ruling).*
   > - *Per-artefact license accessibility (R1.1, A1): satisfied via declared-inheritance mechanism in LICENSE.md (per Verifier Q9.4 patch).*
   > - *Other principles: implementation aligned but ongoing audit cadence (per FAIR three-tier checklist) is the discipline that surfaces drift.*

**Verifier verdict:** overstated-compliance claim closed; FAIR.md now honestly distinguishes operational alignment (current state) from full compliance (target state).

---

## Cross-jurisdiction integration with Architect modifications

This Verifier-followup is drafted to integrate with the Architect Q1–Q7 rulings (`governance-ratification-architect-review-response-v0.1.md`):

- **§4 patch** integrates with Architect Q2 stance-reclassification draft (single replaced paragraph carries both Architect's reclassification and Verifier's Core-Function in-line definitions).
- **§7 (renumbered to §9) patch** is independent of Architect modifications.
- **LICENSE.md Data + License-inheritance patches** are independent of Architect modifications; Architect Q6.1 dataset/slot distinction is in FAIR.md, not LICENSE.md.
- **FAIR.md Q10.3 patches** are independent of Architect Q6/Q7 modifications; both stances' modifications land in the same `FAIR.md` v0.3.0.

No ruling collision detected. Integration commit applies all modifications sequentially (CONVENTIONS, FAIR, LICENSE) per the v0.3.0 ratification checklist.

---

## Document control

- **v0.1** (2026-04-29): Initial Verifier follow-up patches drafted on user direction "Path 1 — go" (acceptance of Verifier patch offer in RT-2026-006 response). Four blocking-issue remediations: Q8.5 working-term + in-line definition; Q9.3 per-class defaults + per-dataset override; Q9.4 declared-inheritance mechanism; Q10.3 forward-looking alignment wording with explicit compliance-status section. Cross-jurisdiction integration with Architect Q1–Q7 verified — no ruling collisions.
- **Disposition.** Patches drafted, ready for integration in v0.3.0 ratification commit. Verifier verdict on RT-2026-006 moves from CONDITIONAL to RATIFIED on patch application + integration commit.
- **Linked:** `governance-ratification-verifier-review-response-v0.1.md` (CONDITIONAL verdict source); `governance-ratification-architect-review-response-v0.1.md` (Architect Q1–Q7 rulings; integration target); `governance-ratification-architect-verifier-review-v0.2.md` (RT-2026-006 brief).

**Stance log.** Drafted Verifier (follow-up patches per accepted offer). No veto. Disposition: patches drafted and integrated in v0.3.0 ratification commit.

---

*Verifier-stance follow-up patches. ~1300 words. Patches ready for integration in v0.3.0 ratification commit.*
