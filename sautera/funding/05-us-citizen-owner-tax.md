# US Citizen Owner — What Actually Applies

**Established 2026-08-24:** the owner is a **US citizen**.
**Not tax advice.** This is a map for a conversation with a US international tax
specialist. Every figure here is from practitioner secondary sources — irs.gov,
Cornell's US Code, eCFR and govinfo are all blocked by this environment's
network policy — so confirm before relying on any number.

---

## 1. Correction to `01` §5

The entity brief argued against a US entity partly on **Form 5472** exposure —
$25,000 annually for a foreign-owned single-member LLC. **That does not apply
here.**

Form 5472 requires a **25% *foreign* shareholder**:

> "A reporting corporation is either a 25% foreign-owned U.S. corporation
> (including a foreign-owned U.S. disregarded entity), or a foreign corporation
> engaged in a trade or business within the United States."

A Wyoming LLC owned by a US citizen is not foreign-owned. No Form 5472, no
$25,000 exposure. The reasoning in `01` §5 was built on an assumption about the
owner's status that turned out to be wrong, and that specific argument is
withdrawn.

**The conclusion still holds — for different reasons.** See §4.

---

## 2. The governing fact: obligations follow the person

The US taxes citizens on **worldwide income**, wherever they live and wherever
the company sits. This reframes everything in the earlier documents:

> **Choosing Grenada does not reduce US tax exposure. It never could.**

The earlier framing — Grenada as a way to keep clear of the US regime — was
wrong on its premise. Grenada is the right jurisdiction for **operational**
reasons: WiPay onboarding, ECCU regulatory footing, app store enrollment, being
the correct data controller. Not for US tax reasons.

The real US question is not *where* the company sits. It is **how the Grenadian
entity is classified for US tax purposes**, and that is a choice — if it is
preserved (§3.1).

---

## 3. The classification fork

### Option A — Disregarded entity (Form 8832 "check the box")

The Grenadian company is transparent for US tax. Its income and expenses land
directly on the owner's Form 1040.

| | |
|---|---|
| CFC status | None |
| GILTI | Does not apply |
| Form 5471 | Not required |
| Instead | **Form 8858** (foreign disregarded entity) — simpler, but still carries a $10,000 non-filing penalty |
| Losses | **Flow through** and can offset other income |

**This is usually the better answer pre-profitability.** NUTMEG is pre-revenue
with real costs — AWS, Twilio, development. Under Option A those losses are
usable now. Under Option B they are trapped inside the CFC and do nothing for
you until the company has income to absorb them.

### Option B — Corporation (the default for many foreign entities)

| | |
|---|---|
| CFC status | Yes — a foreign corporation >50% owned by 10%+ US shareholders |
| Form 5471 | Required. **$10,000 per year**, per corporation, even with zero income; +$10,000 per 30 days after a 90-day notice, capped at $50,000 |
| Statute of limitations | Failure to file can hold the SOL open on the **entire return**, not just the foreign portion |
| GILTI | Profits taxed currently, **whether or not distributed** |
| Relief | **§962 election** — elect to be taxed as a domestic corporation on the inclusion, unlocking the §250 deduction and indirect foreign tax credits |

A February 2026 Second Circuit decision went against the *Farhy* defense
taxpayers had used against 5471 penalty assessment, so the IRS can assess and
collect these directly.

**GILTI in 2026 is worse than it was.** The OBBBA cut the §250 deduction from
50% to 40% (corporate effective rate roughly 10.5% → 12.6%), and the **QBAI
deduction is gone from 1 January 2026**. QBAI exempted a 10% return on tangible
assets — close to worthless for a software company anyway, and now absent
entirely. Effectively all of NUTMEG's profit becomes GILTI. Without a §962
election an individual pays ordinary rates, up to 37%.

**§962 must be made annually, applies to all your CFCs for that year — no
cherry-picking — and can trigger a second layer of tax on actual distributions
under §962(d).** It is a real tool, not a free one.

### 3.1 ⚠ The irreversible bit — decide BEFORE registering

**Not every foreign entity can check the box.** Treas. Reg. §301.7701-2(b)(8)
lists foreign entity types that are **per se corporations** — permanently
classified as corporations, with Form 8832 unavailable forever.

Commonwealth Caribbean jurisdictions **do** appear on that list, and the entity
type named varies by country:

- Barbados — **Limited Company**
- Belize — **Public Limited Company**
- Australia — **Public Limited Company**

**Grenada's entry could not be verified** (eCFR, govinfo and Cornell all blocked
here). If Grenada is listed, the named entity form is locked into Option B
permanently — CFC, Form 5471, GILTI, no way back.

> **Have the specialist read §301.7701-2(b)(8) for Grenada and pick the entity
> form accordingly, before the company is registered.** This is the single most
> consequential irreversible decision in the whole plan, it costs nothing to get
> right, and it cannot be undone afterwards.

---

## 4. So: does NUTMEG sit under Sendall Holding LLC?

**Still no — but not for the reason given in `01`.**

The original argument (US entity imports US exposure) collapses: as a US citizen
the owner has that exposure regardless. The surviving arguments:

1. **It solves nothing.** WiPay onboarding and ECCU regulatory footing require a
   Grenadian entity. A US parent above it does not help with either.
2. **If Sendall Holding is a single-member LLC, it is disregarded** — the owner
   is treated as holding NUTMEG directly. The layer is invisible for tax and adds
   only administration.
3. **If it is multi-member or elects corporate treatment**, it becomes a US
   corporation in the chain — a second layer of tax on distributions, and more
   complexity, for no operational gain.
4. **Liability isolation argues against it.** Common ownership links NUTMEG,
   SAUTERA and CLIVE. Separate ownership keeps a problem in one from reaching
   the others.

**Recommendation:** own NUTMEG (Grenada) directly. Use "Sendall Holding" as a
**brand umbrella across ventures, not an ownership chain.** That costs nothing,
carries no cross-border reporting, and keeps the ventures legally separate.

If Sendall Holding LLC has genuine US-facing business — SAUTERA contracts, US
customers — let it keep doing that. Just don't put the Grenadian operating
company underneath it.

---

## 5. What applies regardless of structure

These attach to the owner as a US citizen and cannot be structured away:

- **FBAR (FinCEN 114).** Required if foreign accounts total more than $10,000 at
  any point in the year — aggregate, not per account — including accounts held
  through **signature authority**. NUTMEG's Grenadian bank account will trigger
  this. 2026 penalties: roughly $16,536 non-willful; willful the greater of about
  $165,353 or 50% of the balance, per year, per account.
- **Form 8938 (FATCA)** at the individual level; thresholds depend on residence.
- **Worldwide income** reported on Form 1040 every year.

---

## 6. The next question that matters

**Where is the owner tax-resident — Grenada or the US?** It determines:

- **FEIE (Form 2555).** Can shelter *earned income* (a salary from NUTMEG) for a
  bona fide resident abroad. It does **not** shelter GILTI or Subpart F
  inclusions — a common and expensive misunderstanding.
- **Foreign tax credits.** Depends on what Grenada actually charges; if the
  effective Grenadian rate is low, there is little credit to claim.
- **State tax.** Some US states do not follow the federal foreign provisions and
  tax differently. If the owner remains resident in a state, that is a separate
  layer nobody remembers until it arrives.

---

## 7. Finding the right advisor

**A general accountant is not sufficient here.** Forms 5471 and 8858, GILTI, and
§962 are routinely missed by competent generalists who don't work cross-border,
and the penalties start at $10,000 before any tax is owed.

Screening question: *"Do you prepare Forms 5471 and 8858, and have you made §962
elections for clients?"* A vague answer means keep looking.

Take these to the first meeting:

1. Is Grenada on the §301.7701-2(b)(8) per se list, and which entity form should
   we register to preserve the check-the-box option? **(Before registration.)**
2. Given pre-revenue losses, does disregarded treatment beat CFC treatment now,
   and what is the trigger to switch later?
3. What does the FBAR/8938 picture look like once the Grenadian account opens?
4. Does the school wallet — holding customer funds — change any of the above?

---

## Sources

Primary sources for this topic (irs.gov, law.cornell.edu, ecfr.gov, govinfo.gov)
are all blocked by this environment's network egress policy. Everything above is
drawn from tax-practitioner secondary sources that corroborate one another.
**Have the figures confirmed before relying on them.**

Points to re-verify against the statute and regulations:
- 26 U.S.C. §6038 / Form 5471 penalty amounts
- 26 U.S.C. §957 (CFC definition), §951A (GILTI), §962 (election)
- 26 U.S.C. §6038A / Form 5472 — the 25% foreign ownership test
- **Treas. Reg. §301.7701-2(b)(8) — the per se list, for Grenada specifically**
- FinCEN 114 thresholds and current penalty amounts
