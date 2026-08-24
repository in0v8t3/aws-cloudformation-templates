# App Store Enrollment — What Is Verified, What Is Not

**Researched:** 2026-08-24
**Scope:** Can a Grenada-registered company enroll as an organization with Apple
and Google, and obtain the D-U-N-S Number Apple requires?

**Verdict up front:** Apple's *requirements* are fully confirmed from primary
sources. Neither Apple's nor Google's **per-country eligibility for Grenada**
could be confirmed to certainty — for different reasons, both explained below.
A prior statement of mine was more confident than the evidence supports; it is
corrected in §4.

---

## 1. CONFIRMED — Apple organization enrollment requirements

Quoted from Apple's own pages (developer.apple.com/help/account/membership/program-enrollment/,
/programs/enroll/, /support/enrollment/). All five are hard requirements:

| # | Requirement | Apple's wording |
|---|-------------|-----------------|
| 1 | **Legal entity** | "your organization must be a legal entity so that it can enter into contracts with Apple. We don't accept DBAs, fictitious businesses, trade names, or branches. The legal entity name will appear as the seller for apps you distribute." |
| 2 | **D-U-N-S Number** | "Your organization must have a D‑U‑N‑S Number so that we can verify your organization's identity and legal entity status… They're free in most jurisdictions." |
| 3 | **Legal binding authority** | "you must have the legal authority to bind your organization to legal agreements. You must be the organization's owner/founder, executive team member, senior project lead, or an employee with legal authority granted to you by a senior employee." |
| 4 | **Work email on your domain** | "Your work email address needs to be associated with your organization's domain name." |
| 5 | **Public, functional website** | "Your organization's website must be publicly available and functional, and its domain name must be associated with your organization. Links to social media webpages or websites that contain minimal content or display a message from a domain registrar won't be accepted." |

### 1.1 Two of these are new work, not paperwork

Requirements 4 and 5 are the ones that quietly add weeks:

- **A live website is a prerequisite, not a launch task.** A holding page or a
  registrar parking page is explicitly rejected. NUTMEG needs a real, functional
  site on its own domain *before* Apple enrollment — which means it also needs
  the domain registered first.
- **Email must be on that same domain.** A Gmail address fails. So: domain →
  website → mailbox → enrollment, in that order.

Both AWS Activate and the Twilio program also expect a live company website, so
this single item unblocks three things at once. **It is the highest-leverage
task on the list and depends on nothing else.** Start it now.

---

## 2. CONFIRMED — the D-U-N-S mechanics

From Apple's D-U-N-S page (developer.apple.com/support/D-U-N-S/):

> "Companies and educational institutions must provide a D‑U‑N‑S Number
> registered to their legal entity… If you're enrolling as an individual, you
> don't need a D‑U‑N‑S Number."

> "While many types of businesses can receive a D‑U‑N‑S Number, your business
> must be recognized as a legal entity (such as a corporation, limited
> partnership, or limited liability company)… DBAs, fictitious businesses, trade
> names, and branches are not accepted."

> "After requesting a D‑U‑N‑S Number, please allow up to 5 business days to
> receive your number from D&B. Expediting your D‑U‑N‑S Number creation process
> will not shorten this waiting period."

> "Once you receive your D‑U‑N‑S Number, please allow up to 2 business days for
> Apple to receive your information from D&B."

### 2.1 A timing conflict worth planning around

Apple says **up to 5 business days**. D&B's own general guidance describes
standard processing of roughly **20–30 business days** in many countries, with
paid expedite bringing it to around 8. Apple also says D-U-N-S numbers are free
"**in most jurisdictions**" — not all.

Apple's 5-day figure most likely reflects large markets where D&B has a direct
local presence. Grenada is not that.

**Plan for weeks, not days**, and check first whether a number already exists —
D&B may have assigned one already, which skips the wait entirely. Apple's page
notes: "D&B may have already assigned your organization a free D‑U‑N‑S Number."

---

## 3. CONFIRMED — Apple publishes no public country list

This is the important structural finding, and it means **nobody** can answer the
Grenada question from public sources — not me, not a consultant.

Three separate Apple pages were checked (`/programs/`, `/programs/enroll/`,
`/help/account/membership/program-enrollment/`, `/support/enrollment/`). None
contains a list of enrollment-eligible countries. The only geographic statement
Apple makes is:

> "Enrollment in India is only available through the Apple Developer app.
> Enrollment may not be supported in certain regions, for example due to
> sanctions or other restrictions."

Separately, `/programs/` states the App Store reaches users in **175 regions** —
but that is *distribution* reach, not *enrollment* eligibility. The two are
different lists and should not be conflated.

A figure of "more than 220 countries or regions" for enrollment circulates and is
attributed to Apple, but it could not be confirmed on any Apple page read
directly. **Treat it as unverified.**

---

## 4. NOT CONFIRMED — Grenada specifically

### 4.1 Correction

An earlier statement of mine — that "Apple and Google both enroll organizations
from Grenada" and that this is "normal, not exotic" — was stated with more
confidence than the evidence supports. It remains the probable answer. It is not
an established one. The two claims fail verification for different reasons:

### 4.2 Apple — unverifiable from public sources, by design

Apple does not publish the list (§3). The country selector inside the enrollment
flow is the authoritative source, and it is only visible once you begin
enrolling. There is no document to check.

### 4.3 Google — the list exists but could not be read

Google **does** publish "Supported locations for developer and merchant
registration" (Play Console Help, answer 9306917), and it distinguishes two
separate lists: **developer** registration and **merchant** registration.
`support.google.com` and `web.archive.org` are both blocked by this
environment's network egress policy, so the table could not be read directly.

**Circumstantial evidence, not proof:** Google publishes per-country Developer
Verification requirement pages, and indexed pages exist for neighbouring OECS
states — **Antigua & Barbuda (AG)**, **St. Kitts & Nevis (KN)**, and
**St. Vincent & the Grenadines (VC)**. A Grenada (GD) page did not surface in
search, which is weak evidence either way — absence from search results is not
absence from the list.

### 4.4 Why the merchant/developer distinction probably doesn't matter here

Merchant registration governs selling through Google Play's billing system.
NUTMEG is a free app charging for **real-world transport services** through
WiPay, which falls outside Play's billing requirement. So developer registration
is the list that matters, and it is the broader of the two. If Grenada appears on
only one list, developer registration is the likelier one — and the one you need.

Verify this rather than assume it: an app holding stored-value balances (the
school wallet) is the kind of thing a reviewer may probe against billing policy.

---

## 5. NEW FINDING — Google Play Developer Verification

Google now runs a **Developer Verification** process with country-specific
document requirements for organization accounts, typically:

- personal identity documents for the account owner or authorized representative
- official organization documents — certificate of incorporation, or equivalent

This did not exist in earlier plans and adds a document-gathering step. Grenada's
certificate of incorporation from company registration should satisfy it, but
confirm the exact Grenada list once the account exists.

---

## 6. The 20-minute check that IS conclusive

Public research cannot close this. These two steps can, and cost nothing:

**Apple — begin enrollment and stop.**
Sign in at developer.apple.com/programs/enroll/ with an Apple Account and start
the organization flow. The entity-country selector appears before any payment.
If Grenada is in the dropdown, the question is answered definitively. Abandon the
flow at that point; nothing is charged and nothing is committed.

**Google — open the Play Console signup.**
Start the developer registration flow at play.google.com/console/signup and check
the country selector. Same logic: the list is authoritative, and you can stop
before the $25 registration fee.

**Also worth doing, in parallel:**
- Search the D&B D-U-N-S lookup for your entity name once registered — a number
  may already exist.
- Ask Apple Developer Support directly (developer.apple.com/contact/) whether
  Grenada-registered legal entities can enroll. A written answer beats inference.

---

## 7. What this does and doesn't change

**Doesn't change:** the Grenada-only recommendation. The reasons for it — WiPay
onboarding, ECCU regulatory footing, no Form 5472 exposure, no EIN bottleneck —
are unaffected by app store eligibility, and none depends on it.

**Does change:** the sequencing. Two items move to the front because they gate
everything and depend on nothing:

1. **Domain + live website + branded email.** Required by Apple, expected by AWS
   Activate and Twilio. Nothing else blocks it. Start immediately.
2. **The dropdown check above.** Ten minutes, and it converts the largest
   remaining unknown into a fact before you spend on registration.

**Adds a contingency worth knowing:** if Grenada turns out not to be supported
for organization enrollment, the fallback is not a US entity. Options in order of
preference are (a) enroll as an **individual** with Apple — no D-U-N-S required —
and migrate to an organization account later, or (b) look at a nearby OECS
jurisdiction that is confirmed supported. Both are cheaper than a Wyoming LLC and
its annual Form 5472 exposure.

---

## Sources

Primary, read directly:
- https://developer.apple.com/help/account/membership/program-enrollment/
- https://developer.apple.com/programs/enroll/
- https://developer.apple.com/support/enrollment/
- https://developer.apple.com/support/D-U-N-S/
- https://developer.apple.com/programs/

Identified but unreadable from this environment (egress-blocked):
- https://support.google.com/googleplay/android-developer/answer/9306917 — supported locations for developer and merchant registration
- https://support.google.com/googleplay/android-developer/answer/15633622 — developer verification documents by country
- https://www.dnb.com/utility-pages/international.html — D&B country selector
