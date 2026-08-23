# NUTMEG — Twilio AI Startup Searchlight 2026
## Application Answer Bank

**Applicant entity:** `[FILL: entity name once formed — see 01-entity-structure-brief.md]`
**Status:** Interest registered. Awaiting Twilio follow-up.
**Prerequisite:** Twilio account must exist before applying (stated on their
eligibility page). If NUTMEG already has a live Twilio account for OTP and SMS,
**apply under that account** — an existing production integration is the single
strongest asset in this application.

---

## How to use this document

The exact form fields aren't known yet. Rather than guess the form, this is a
**bank of answers at three lengths** (short ~50 words, medium ~150, long ~300)
covering the questions these programs always ask. Paste the one that fits the box.

`[FILL: ...]` markers are facts only you have. **Do not estimate them.** An
inflated traction number in a startup program application is a representation to
a company you want a commercial relationship with.

---

## 1. Positioning — read this first

**The temptation:** describe NUTMEG as an AI transport platform.
**The better play:** describe NUTMEG as *communications infrastructure for a
market where data connectivity cannot be assumed*, with AI on top.

This matters because Searchlight is a Twilio program. Reviewers are looking for
companies whose use of Twilio is structural rather than decorative. NUTMEG has a
genuinely unusual answer here, and most applicants do not:

> In Grenada, mobile data coverage is inconsistent — particularly on the interior
> routes and outside the St. George's corridor. NUTMEG treats SMS not as a
> notification channel but as a **transport of last resort**. The DDIL subsystem
> (Disconnected, Degraded, Intermittent, Limited) explicitly assumes the data
> path will fail and degrades to Twilio SMS to keep bookings, boarding
> confirmations, and driver dispatch working.

That is a real engineering position, already built (Sprint S-08, S-14), and it is
the thing to lead with.

**Lead with:** DDIL / SMS-as-fallback.
**Support with:** the Trust Engine and intelligence pipeline.
**Do not lead with:** AI. Every applicant leads with AI.

---

## 2. One-liner

> NUTMEG is Grenada's first integrated mobility platform — bus booking, taxi
> dispatch, and driver payouts — engineered for a market where mobile data
> coverage fails, using SMS as a first-class transport rather than a fallback
> afterthought.

**Alternate, if the form is fintech-leaning:**
> NUTMEG moves people and money across Grenada's informal transport network:
> QR-boarded bus booking, taxi dispatch, school wallets, and driver payouts, on
> infrastructure built to survive intermittent connectivity.

---

## 3. What does your company do?

### Short (~50 words)
NUTMEG is Grenada's first integrated transport app. It connects passengers, bus
drivers, taxi operators, and schools through one platform: route booking with QR
boarding, GPS taxi dispatch, a passenger demand board, school wallets, and driver
payouts. Built for intermittent connectivity, with SMS as a first-class channel.

### Medium (~150 words)
Grenada's public transport runs on an informal minibus and taxi network. There
are no published schedules, no way to know if a bus is coming, no cashless
payment, and no record of a trip once it ends. Drivers are paid in cash and have
no earnings history they can take to a bank.

NUTMEG replaces that with one platform. Passengers book seats on routes and board
with a QR code. Taxis are dispatched with GPS tracking and negotiated fares. A
demand board lets passengers signal trips that don't yet exist, so operators can
see real demand instead of guessing. Parents top up school wallets with spending
limits for their children. Drivers get tracked earnings and scheduled payouts.

The whole system assumes connectivity will fail. Bookings, boarding, and dispatch
degrade gracefully to SMS rather than breaking — which is the difference between a
platform that works in Grenada and one that only demos well.

### Long (~300 words)
Use the Medium answer, then append:

> Underneath, NUTMEG runs a Trust Engine that scores every participant —
> passengers, drivers, conductors — into deterministic tiers (TRUSTED, VERIFIED,
> AT_RISK) from behavioural events: completed trips, no-shows, payment history,
> boarding anomalies, GPS inconsistencies. Trust tier drives real decisions:
> dispatch priority, payout timing, and fraud holds.
>
> A nightly intelligence pipeline turns the same event stream into operational
> output — driver coaching insights, fraud signals, and ETA accuracy measurement
> scored against actual arrival times.
>
> NUTMEG is built and operated by Sendall Holding under SAUTERA, our own
> infrastructure trust framework, which governs how every deployment is assessed
> before it reaches production. The platform has completed sixteen engineering
> sprints from authentication through school wallets, and is currently in the
> hardening and launch sequence: performance testing, security audit, app store
> submission, and beta cohort launch in Grenada.

---

## 4. How do you use AI? *(the make-or-break question)*

**Be precise and be honest.** These reviewers read hundreds of "we use AI"
answers. A specific, modest, true answer beats a vague ambitious one — and
NUTMEG's real position is genuinely interesting because of *why* it's
deterministic today.

### The answer
> NUTMEG's Trust Engine is deliberately **deterministic today, not
> probabilistic** — and that is an engineering decision, not a gap.
>
> Trust tiers govern consequential outcomes: whether a driver's payout is held,
> whether a passenger can book. In a market this small, a driver wrongly flagged
> AT_RISK by an unexplainable model is a driver who loses income and tells
> everyone. So every tier transition is currently rule-based, logged, and
> explainable to the person it affects — and overridable by an admin with an
> audit trail.
>
> What that produces is the asset: a growing, **labelled corpus** of behavioural
> events with known-good outcome labels and human override decisions attached.
> Every admin override is a training signal about where the rules are wrong.
>
> Phase 2 replaces the rule layer with learned models on top of that corpus:
> demand forecasting by route and time-of-day, ETA prediction against measured
> arrival error, and anomaly-based fraud detection on boarding and payment
> patterns. The deterministic engine stays in place as the explainability and
> guardrail layer.
>
> We're building the training data before we build the model, because in a
> 115,000-person market you only get to be wrong about someone's livelihood once.

**Why this answer works:** it demonstrates ML judgment rather than ML vocabulary,
it explains a real constraint, and it gives the reviewer a defensible reason the
AI is Phase 2. Claiming a live ML system that isn't live is checkable and fatal.

---

## 5. How do you use Twilio? *(your strongest section)*

### In production today
| Use | Twilio surface | Sprint |
|-----|---------------|--------|
| Phone-number authentication and OTP | Verify / Programmable Messaging | S-01 |
| Booking, boarding, and dispatch notifications | Programmable Messaging | S-14 |
| DDIL degraded-mode delivery when data fails | Programmable Messaging | S-08 |

### The narrative
> Most transport apps treat SMS as a notification channel. NUTMEG treats it as a
> **transport layer**.
>
> Grenada's mobile data coverage is uneven — it drops on interior routes, in the
> hills, and during weather events that are a routine part of hurricane-season
> operations. An app that requires a data connection to confirm a booking is an
> app that fails exactly when a passenger is standing at the roadside.
>
> Our DDIL subsystem detects degraded connectivity and re-routes the operation
> over SMS: the passenger still gets a boarding confirmation, the driver still
> gets the dispatch, and the queue reconciles when data returns. SMS is not a
> lesser path — it is the path that defines whether the product works in the
> market it was built for.
>
> Phone numbers are also the identity primitive. Smartphone penetration is high
> but app-store familiarity and email use are not universal among the driver and
> conductor population, so Twilio OTP is the entire onboarding funnel. There is
> no password.

### What we'd build with the award
List two or three concrete, credible expansions — this is where programs
differentiate applicants:

1. **Masked passenger-driver communication.** Taxi dispatch currently exchanges
   real phone numbers. Twilio-brokered masked calling and messaging removes that
   safety and privacy exposure — meaningful in an island community where a
   driver and passenger are often two degrees apart. Direct rider-safety impact.
2. **SMS-only booking for feature phones and low-data users.** A full booking
   flow over SMS keyboard shortcodes, extending the platform to passengers who
   cannot or will not install an app. This widens the addressable market rather
   than just improving the existing one.
3. **Multi-territory OTP and messaging as the platform expands** across the OECS
   — each territory adds carrier, sender-ID, and compliance work.
4. `[OPTIONAL: WhatsApp via Twilio, if messaging behaviour in-market justifies it
   — verify actual local usage before claiming this]`

---

## 6. Market

> **Grenada is the proving ground, not the market.**
>
> Grenada is a nation of roughly 115,000 people `[VERIFY current figure]` where
> the minibus network carries a large share of daily commuters and there is no
> digital layer over any of it. That's small enough to reach meaningful coverage
> and large enough that the operational problems are real.
>
> The market is the OECS and the wider Caribbean, where the same conditions
> repeat almost exactly: informal transport networks, cash-based driver
> economies, high mobile penetration with unreliable data, small populations that
> global mobility platforms have never found worth serving. A platform that works
> in Grenada is not a platform that needs rebuilding for Dominica, St. Vincent,
> or St. Lucia — the roadmap already carries multi-currency and regional
> expansion as planned work, along with Carriacou and Petite Martinique.
>
> The moat is not technology. It's that the incumbents' unit economics don't work
> at island scale, and that operating here requires relationships with driver
> associations and school administrations that can't be bought remotely.

---

## 7. Traction — fill honestly, leave blank if unknown

Do not estimate any of these.

- Stage: `[FILL: pre-launch / beta / live]`
- Current sprint position: `[FILL: e.g. S-17, hardening toward launch]`
- Registered drivers / operators: `[FILL or omit]`
- Beta cohort size: `[FILL or omit]`
- Trips completed: `[FILL or omit]`
- LOIs or agreements with driver associations, schools, or government:
  `[FILL — these are worth more than user numbers at this stage; name them]`
- Funding raised to date: `[FILL: bootstrapped / amount]`
- Team size and composition: `[FILL]`
- Founded: `[FILL: incorporation date once registered]`

**If pre-launch, say so plainly.** Sixteen completed engineering sprints, a
defined launch sequence, and a working product are a stronger story than a vague
implication of traction that doesn't exist. Pre-launch is not a disqualifier;
being caught inflating is.

---

## 8. Why now

> Three things converged. Mobile penetration in Grenada crossed the point where a
> phone-first transport product is viable for drivers, not just passengers.
> WiPay and regional payment rails matured enough to move money without a bank
> integration per island. And the cost of building this collapsed — a platform
> that would have needed a twenty-person team five years ago has been built by
> `[FILL: team size]` using AI-assisted development throughout.
>
> That last point is the reason a Grenadian mobility platform is fundable now and
> wasn't before. The addressable market didn't grow. The cost of serving it fell
> below the threshold.

---

## 9. Pre-submission checklist

- [ ] Entity registered; name, jurisdiction, and incorporation date available
- [ ] Twilio account exists (apply under the **production** account if one exists)
- [ ] Website live at a real domain `[FILL: URL]` — programs check this
- [ ] Every `[FILL]` resolved or the claim removed entirely
- [ ] Population and market figures verified against a current source
- [ ] Deadline confirmed `[FILL/VERIFY: Searchlight 2026 closing date]`
- [ ] Founder LinkedIn profiles current — reviewers look
- [ ] Demo video or screenshots ready if the form allows attachments

**Questions to Twilio** (twiliostartups@twilio.com — they invited contact):
1. Is the program open to companies headquartered outside the US, and does the
   applying entity's jurisdiction affect eligibility?
2. What is the closing date, and is there a required stage or funding threshold?
3. Does an existing production Twilio integration factor into evaluation?

Question 1 is worth asking **before** finalising the entity decision in `01` —
the answer could influence which jurisdiction you form in.
