# Entity Structure Brief — NUTMEG / Sendall Holding

**Status:** Decision required before either funding application is submitted
**Prepared:** 2026-08-23
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

## 4. The app store timeline nobody budgets for

The chain to a live listing is serial, and two links are slow:

```
Wyoming LLC formation        ~1-3 business days (expedited)
        ↓
EIN from IRS                 ← THE BOTTLENECK
        ↓
D-U-N-S number               ~1-5 business days (free; paid "expedite" exists)
        ↓
Apple Developer Program      ~1-4 weeks verification for organizations
Google Play Developer        ~2-5 days, plus org verification
        ↓
App review (S-21)            days, plus rejection cycles
```

**The EIN is the bottleneck if no member has a US SSN or ITIN.** The online
instant-EIN path requires one. Without it, Form SS-4 goes by fax or mail and
realistically takes several weeks — historically much longer at times. Everything
downstream waits on it.

**Action:** start the EIN the same week the LLC is formed. Do not sequence it
after other setup work. If any founder or officer holds a US SSN/ITIN, use that
person as the responsible party and take the same-day path instead.

### 4.1 Two app store specifics worth knowing now

- **In-app purchase rules.** Fares for real-world transport are physical
  goods/services consumed outside the app, so Apple's IAP commission does not
  apply and WiPay can be used directly. **The school wallet is the risk.** A
  stored-value balance looks like digital currency to a reviewer even when it can
  only be spent on bus rides. Prepare the reviewer-facing explanation before
  submission rather than arguing it after rejection.
- **Territory restriction works in your favour.** Both stores let you ship to a
  selected list of countries. Launch Grenada-only, expand by territory. Every
  additional territory adds tax forms and, eventually, local consumer and data
  obligations — so let the entity structure catch up before widening the list.

---

## 5. Wyoming LLC vs. Delaware C-Corp — the fundraising fork

Applying to startup accelerator programs signals an intent to raise. If that
intent is real, note that:

- US venture investors almost universally require a **Delaware C-corporation**.
  Priced rounds and standard SAFEs assume it.
- Converting an LLC to a Delaware C-corp later is routine but not free — legal
  fees, and potentially a taxable event depending on how appreciated the entity
  is by then.
- An LLC's pass-through treatment can create personal filing obligations for
  members in their own jurisdictions.

**Decide now which of these you are:**

| If you intend to… | Form |
|---|---|
| Bootstrap, keep control, no institutional raise | Wyoming LLC |
| Raise from US VCs or accelerators within ~24 months | Delaware C-Corp from the start |

Neither is wrong. Choosing Wyoming LLC *by default* and discovering the mismatch
during a term sheet is the expensive outcome.

---

## 6. Recommended structure

Subject to counsel, the structure that fits what NUTMEG actually does:

```
        Sendall Holding  (US — Wyoming LLC or Delaware C-Corp)
        ├── owns IP, brand, source code
        ├── holds app store developer accounts
        ├── contracts AWS, Twilio, and receives program credits
        └── is the entity named on funding applications
                    │
                    │ IP licence + services agreement
                    ▼
        NUTMEG (Grenada) Ltd.  (operating subsidiary)
        ├── contracts passengers, drivers, schools
        ├── holds the WiPay merchant relationship + local bank account
        ├── carries ECCU/GARFIN regulatory exposure
        └── is the data controller for Grenada residents
```

**Why this shape:**
- Funds never touch the US entity → the §3.3 problem largely disappears.
- WiPay onboards a local company → the §3.2 blocker disappears.
- IP and equity stay in a jurisdiction investors and acquirers understand.
- Data protection obligations for Grenadian users sit with a Grenadian controller,
  which is the cleaner answer under Grenada's data protection regime and aligns
  with the OECS compliance posture already assumed in `data-governance`.

**Costs to accept:** two formations, two sets of books, an intercompany
agreement, and transfer-pricing hygiene between them. Meaningful but ordinary.

### If cash is tight — the phased path

1. **Now:** form the US entity only. It is enough to open both funding
   applications and to start the EIN → D-U-N-S → developer account chain.
2. **Before any real money moves** (before S-23 soft launch, and definitely
   before school wallets go live with real parent funds): form the Grenada
   operating company and move the customer-facing contracts and WiPay
   relationship into it.

The hard line: **do not take custody of a parent's money in a school wallet
through a Wyoming LLC with no local regulatory footing.** That is the one
sequencing error here that is genuinely difficult to unwind.

---

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

Settle these in order. Items 1 and 2 can invalidate the rest.

- [ ] **Email WiPay:** will you onboard a US (Wyoming) entity for Grenada
      operations, or is a local company required?
- [ ] **Local counsel:** does the school wallet / driver payout model require
      licensing or registration under ECCU/GARFIN rules?
- [ ] **Fundraise intent:** Wyoming LLC or Delaware C-Corp? (§5)
- [ ] **Responsible party for the EIN:** does anyone hold a US SSN/ITIN?
- [ ] **Trademark clearance** on NUTMEG in target classes/territories
- [ ] Form the entity
- [ ] EIN → D-U-N-S → Apple + Google organization accounts (start immediately)
- [ ] Then, and only then, submit the applications in `02` and `03`
