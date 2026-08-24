# Entity Structure Brief — NUTMEG / Sendall Holding

**Status:** Revised 2026-08-24 — fundraising ruled out, recommendation changed
**Prepared:** 2026-08-23 · **Revised:** 2026-08-24
**Not legal or tax advice.** This is a structuring analysis to take *to* a
Caribbean-competent corporate lawyer, not a substitute for one.

---

## 1. Why this blocks everything else

Both programs on the table require a registered legal entity:

- **Twilio AI Startup Searchlight 2026** — startup programs verify incorporation
  and typically ask for entity name, jurisdiction, and incorporation date.
- **AWS Activate** — requires a company, a website, and (for the higher tiers) a
  provider/accelerator affiliation or funding evidence.

So does the distribution strategy. An Apple or Google **organization** developer
account cannot be opened by an individual — it needs a legal entity and a D-U-N-S
number. That chain is longer than most people plan for (§4).

The entity decision is therefore not a background task. It is the critical path.

---

## 2. The strategy as stated

> Register in Wyoming, distribute via App Store / Google Play to Grenada and the
> wider Caribbean, then the rest of the world.

Wyoming is a sound choice **for what it's good at**: cheap formation, no state
income tax, strong charging-order protection, minimal annual reporting, no
requirement for members to be US persons. For holding IP, signing cloud and
vendor contracts, owning the app store listings, and receiving credits, it works.

The problem is not Wyoming. The problem is that NUTMEG **moves and holds other
people's money**, and a US LLC is an awkward vehicle for doing that in the ECCU.

---

## 3. The money-movement problem (the real issue)

From the platform's own module list, NUTMEG:

- takes passenger top-ups via WiPay
- holds balances in **school wallets** (parent tops up, student spends)
- accrues and disburses **driver earnings and payouts**

That is stored value plus payment aggregation. Three consequences:

### 3.1 ECCU / ECCB exposure
Grenada is in the Eastern Caribbean Currency Union. Holding customer balances and
settling payouts to drivers is the kind of activity the ECCB and the Grenada
Authority for the Regulation of Financial Institutions take an interest in. This
is a question to put to local counsel **before** launch, not after — a soft launch
that quietly operates a wallet is still operating a wallet.

### 3.2 WiPay onboarding
WiPay is a Caribbean PSP. Merchant onboarding generally expects a locally
registered business, local directors' identification, and a local settlement
account. **Verify directly with WiPay whether they will onboard a Wyoming LLC for
Grenada-domiciled operations.** If the answer is no — which is plausible — the
Wyoming-only structure fails at the payments layer, which is the layer the entire
driver-payout and school-wallet product depends on.

> This single question is worth an email to WiPay this week. It can invalidate the
> structure before you spend anything on formation.

### 3.3 US money transmission
A US-domiciled entity that holds customer funds and remits them to third parties
can attract money-transmitter analysis, which in the US is licensed state by state
and is expensive. The usual answer is that the funds never touch the US entity —
but that only holds if the structure is deliberately built that way. If a Wyoming
LLC is the sole entity and it contracts with passengers and drivers directly, it
is much harder to argue.

---

## 4. The app store timeline

With no US entity, the chain shortens considerably — the EIN, previously the
bottleneck, drops out entirely:

```
Grenada company registration
        ↓
Domain + live website + branded email    ← START THIS FIRST, it blocks Apple
        ↓
D-U-N-S number            (Apple says ~5 business days; plan for weeks — see 04)
        ↓
Apple Developer Program, organization
Google Play Developer, organization + Developer Verification
        ↓
App review  ·  S-21
```

Apple's organization requirements and the D-U-N-S mechanics are quoted from
primary sources in `04-appstore-enrollment-verified.md`. Two of them are real
work rather than paperwork: Apple requires a **publicly available, functional
website** on your own domain, and a **work email on that domain**. A parking page
is explicitly rejected.

### 4.1 Two app store specifics worth knowing now

- **In-app purchase rules.** Fares for real-world transport are physical
  goods/services consumed outside the app, so Apple's IAP commission does not
  apply and WiPay can be used directly. **The school wallet is the risk.** A
  stored-value balance looks like digital currency to a reviewer even when it can
  only be spent on bus rides. Prepare the reviewer-facing explanation before
  submission rather than arguing it after rejection.
- **Territory restriction works in your favour.** Both stores let you ship to a
  selected list of countries, independent of where you are incorporated. Launch
  Grenada-only, expand by territory.

## 5. Fundraising: resolved — no raise

**Decision taken:** NUTMEG is not raising venture capital.

This settles what was previously the most consequential open question, and it
resolves it *against* the US entity. The Wyoming/Delaware analysis existed to
keep a future priced round clean. With no round coming, that entity is carrying
cost and risk with nothing left to justify it:

- **Form 5472 exposure.** A foreign-owned single-member US LLC must file Form
  5472 with a pro-forma 1120 annually, even with zero US income and zero US
  activity. The penalty for failure to file is **$25,000**. That is a permanent
  annual liability attached to an entity that would exist only for optics.
  *(Confirm specifics with a US tax advisor — but budget for it as real.)*
- **The money-transmission problem (§3.3) stops being worth solving.** The only
  reason to accept it was investor-readiness.
- Two registrations, two sets of books, an intercompany agreement, and transfer
  pricing hygiene — all for no remaining benefit.

**Revised recommendation: register in Grenada only. Do not form a US entity.**

---

## 6. Recommended structure — single Grenadian company

```
        NUTMEG (Grenada) Ltd.
        ├── owns IP, brand and source
        ├── holds the Apple + Google developer accounts
        ├── contracts AWS and Twilio; is the applicant on funding programs
        ├── contracts passengers, drivers and schools
        ├── holds the WiPay merchant relationship + local bank account
        ├── carries the ECCU / GARFIN regulatory footing
        └── is the data controller for Grenadian users
```

**What this wins:**

| | Effect |
|---|---|
| WiPay onboarding | Blocker disappears — a local company is what they expect |
| ECCU / GARFIN | Regulated activity sits under the regulator that governs it |
| EIN bottleneck | **Eliminated.** No US entity, no SS-4, no multi-week wait |
| Form 5472 | Not applicable |
| Data protection | Grenadian controller for Grenadian users — the clean answer |
| Books | One entity, one set |

**What it costs:** very little. App store distribution does not require a US
entity (see `04-appstore-enrollment-verified.md`), and territory targeting is
independent of where you incorporate — ship Grenada first, then the OECS, then
wherever the stores reach.

### 6.1 The one thing that could pull it back

If the Twilio Searchlight program turns out to be restricted to US-domiciled
companies, that is the only remaining argument for a US entity — and it is a weak
one. A credit program is not worth a $25,000 annual filing exposure. Ask them
(§8) before treating it as a constraint.

### 6.2 Adding a holding company later

If NUTMEG is ever sold, or you later decide to raise after all, inserting a
holding company above a Grenadian operating company is a normal, well-trodden
transaction. Doing it *then* costs less than carrying the structure for years
beforehand — and by then the entity will have revenue and history that make the
structuring straightforward.

## 7. Name clearance — check before spending on brand

"Nutmeg" is Grenada's national symbol and the naming is strong locally. But
**Nutmeg Saving and Investment (UK, now part of JPMorgan Chase)** is an
established financial-services brand under that exact name, and NUTMEG's wallet
and payout features sit in adjacent classes.

- Likely fine for Caribbean transport. Not automatically fine everywhere,
  especially as you move toward "rest of the world" and toward fintech framing.
- A basic trademark clearance search in your target classes and territories is
  cheap relative to a rebrand after launch. Do it before the app store listing,
  not after.
- Registering the Wyoming LLC under a name does **not** grant trademark rights.
  They are separate systems and the state will happily register a name that
  infringes.

---

## 8. Decision checklist

Revised for the Grenada-only structure. Items 1 and 2 are unchanged in
importance; items about the US entity are gone.

- [ ] **Domain + live website + branded email.** Gates Apple enrollment, and is
      expected by AWS Activate and Twilio. Depends on nothing else. **Start now.**
- [ ] **Check the country dropdowns** in Apple's and Google's signup flows —
      ten minutes, and it settles enrollment eligibility for certain. See
      `04-appstore-enrollment-verified.md` §6.
- [ ] **Email WiPay:** confirm onboarding requirements for a Grenadian company.
- [ ] **Local counsel:** does the school wallet / driver payout model require
      licensing or registration under ECCU/GARFIN rules?
- [ ] **Email twiliostartups@twilio.com:** does the applying entity's
      jurisdiction affect Searchlight eligibility, and what is the deadline?
- [ ] **Trademark clearance** on NUTMEG in target classes/territories (§7)
- [ ] Register the company in Grenada
- [ ] D-U-N-S Number — check whether one already exists before requesting
- [ ] Apple + Google organization developer accounts
- [ ] Then submit the applications in `02` and `03`

**No longer applicable:** US entity formation, EIN / SS-4, Form 5472, choosing
between Wyoming LLC and Delaware C-Corp, intercompany agreements.
