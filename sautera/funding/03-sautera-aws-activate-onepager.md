# SAUTERA — AWS Activate One-Pager

**Applicant entity:** `[FILL: entity name — see 01-entity-structure-brief.md]`
**Website:** `[FILL: URL — Activate requires a live company site]`
**Stage:** `[FILL]`   **Founded:** `[FILL]`   **Team:** `[FILL]`

---

## Part A — The one-pager

*(This is the pitch. Everything below Part A is supporting material for you, not
for AWS.)*

### What SAUTERA is

SAUTERA is an **infrastructure trust platform**. It answers a question Zero Trust
does not: *is the environment itself fit for use?*

Zero Trust governs **who** may access a system. It assumes the system is sound.
SAUTERA governs **whether the system should be trusted at all** — whether it is
patched, observed, correctly sized, and within its supported lifecycle — and
conveys that verdict to the systems making access and placement decisions.

```
[Identity Trust]  +  [Infrastructure Trust]  =  [Complete Trust Decision]
      (ZT)                 (SAUTERA)
```

Neither half is complete alone. An authenticated user on an end-of-life,
unmonitored host is a breach with valid credentials.

### The problem

Organisations can tell you who logged in. Most cannot tell you, continuously and
with evidence, whether the infrastructure that person reached is trustworthy:

- What versions are running, and which are past end-of-support?
- Is every component actually being observed, or just assumed to be?
- Are trust decisions being enforced, or only reported in a dashboard nobody opens?
- Can any of it be shown to an auditor as a governed, traceable chain?

Compliance tooling answers this **periodically and retrospectively**. SAUTERA
answers it **continuously**, and produces a score that other systems can act on.

### How it works — the Nine Marks

SAUTERA implements a complete trust lifecycle rather than a monitoring product:

| Mark | Function |
|------|----------|
| **VIGIL** | Telemetry ingestion and trust scoring |
| **TELESCOPE** | Anomaly detection and breach signals |
| **ARBITER** | Trust decision point — policy evaluation |
| **SENTINEL** | Trust enforcement point — action across surfaces |
| **PARACLETE** | AI recommendation, human-reviewed before enforcement |
| **EMCS** | Compliance scoring — the Infrastructure Scoring Index (ISI) |
| **CHANNEL** | In-band conveyance of trust to routing and placement |
| **BEACON** | Executive visibility into trust posture |
| **COMMAND** | Governance and auditable decision authority |

VIGIL scores every component across defined domains including **Lifecycle
Health**, **Energy Efficiency**, and **Availability Integrity**, producing the ISI
— a single band-scored index that gates production deployment.

The governing doctrine is deliberately unsoftened: **end-of-life software is
Untrusted. No exceptions.** Systems that permit exceptions accumulate them until
the score means nothing.

### Why AI is governed, not autonomous

PARACLETE generates infrastructure recommendations from telemetry — but
recommendations are **human-reviewed before enforcement**, by design. A trust
platform that autonomously enforces against its own unreviewed inference is a
platform that can take down production because a model drifted. The governance
chain through COMMAND exists to keep every enforcement action attributable.

### Why this is built on AWS

SAUTERA is AWS-native, not AWS-portable:

- **Ingestion:** collector fleet on ECS, queued through SQS
- **State and scoring:** RDS PostgreSQL, ElastiCache
- **Deployment:** blue/green with health-gated cutover and automated rollback
- **Observability:** the telemetry substrate the entire scoring model depends on

SAUTERA is **complementary to AWS, not competitive with it.** It makes AWS
estates more governable and more defensible to auditors — a reason for customers
to consolidate workloads onto AWS rather than fragment them.

### Where credits go

Infrastructure trust scoring is **ingestion-bound**. Cost scales with the volume
of telemetry observed, and it is incurred *before* a customer is billed — you
cannot score infrastructure you are not yet paying to observe. Credits directly
extend the runway between building the scoring corpus and monetising it.

Specifically: `[FILL: your actual allocation, e.g. collector fleet across N
environments / multi-AZ posture for the scoring tier / load and soak testing at
production telemetry volumes]`

### Proof: SAUTERA governs a real production platform

SAUTERA is not a framework in search of an application. It governs the
engineering and go-live of **NUTMEG**, Grenada's first integrated mobility
platform — a live multi-service AWS deployment covering payments, GPS dispatch,
and stored-value wallets, built by the same team through sixteen completed
sprints. Every infrastructure decision in that platform is evaluated through the
SAUTERA trust model before it reaches production, and the ISI must be in the
HEALTHY band before deployment is permitted.

The framework was built because we needed it. It has a real estate to govern
before it has a first external customer.

### The ask

`[FILL: credit tier being requested]` in AWS Activate credits, plus technical
enablement, to `[FILL: specific milestone — e.g. "reach production-grade
multi-tenant ingestion and onboard the first three external environments"]`.

---

## Part B — Working notes (do not submit)

### B1. Which route to Activate?

You have two paths and they are not equivalent.

| | **roiquant (provider route)** | **Direct / accelerator route** |
|---|---|---|
| Speed | Fast — perk claimed as a customer | Slower; more diligence |
| Typical tier | Lower provider tier | Higher tiers where affiliated |
| Cost | Possible roiquant subscription | Free, but needs qualifying affiliation |
| Data exposure | Company data to a third-party SaaS | None beyond AWS |

**AWS Activate is generally one-bite-per-company.** Claiming a small provider
tier can foreclose a larger one. Before claiming through roiquant:

- [ ] Confirm the actual credit amount roiquant's perk delivers — not the
      headline range on their partners page
- [ ] Confirm whether a **paid roiquant plan** is required to unlock it. If
      unlocking $X in credits costs $Y in subscription, run the arithmetic
- [ ] Confirm with AWS whether claiming via a provider affects later eligibility
      for a higher tier
- [ ] Read roiquant's data retention terms. You are selling an infrastructure
      *trust* platform; the optics and the substance of handing company data to a
      third-party analytics SaaS both matter
- [ ] Verify current Activate tiers and terms directly with AWS — program
      structure and amounts change, and anything quoted secondhand may be stale

**Recommendation:** treat roiquant as the fallback. Approach AWS directly first —
SAUTERA has an unusually good story for an AWS startup relationship because it
increases the defensibility of AWS estates. That story is worth more than a
provider-tier credit grant, and it can lead to AWS partner-program conversations
that credits alone never do.

### B2. Positioning notes

**Lead with the Zero Trust gap.** "ZT tells you who; nothing tells you whether the
environment is fit" is a sharp, memorable framing that a reviewer can repeat to a
colleague. That repeatability is what gets an application advanced.

**Do not oversell the AI.** PARACLETE is recommendation-with-human-review. Said
plainly, that reads as maturity. Dressed up as autonomous AI security, it invites
scrutiny that the current build won't survive.

**Lead the proof with NUTMEG.** A framework governing a real production platform
with real money and real users is materially more credible than a framework
described in the abstract. It is also the honest answer to "who uses this?"

**Be straight about external customers.** If there are none yet, say the first
deployment is internal. `[FILL: any pilots, LOIs, or design partners]`

### B3. Other credit programs worth running in parallel

Activate is one-bite; these are separate and can be stacked:

- **Microsoft for Startups Founders Hub** — Azure credits, no funding requirement
- **Google for Startups Cloud Program** — GCP credits
- **NVIDIA Inception** — free to join; relevant once Phase 2 ML work is real
- **Twilio** — see `02`, and note it applies to NUTMEG, not SAUTERA

A multi-cloud credit position is also a legitimate product argument for SAUTERA:
an infrastructure trust platform that only scores one cloud is a narrower product
than one that scores an estate.

### B4. Pre-submission checklist

- [ ] Entity registered (`01`)
- [ ] Live website at a real domain — Activate applications are rejected without one
- [ ] Company email on the domain, not a free provider
- [ ] Every `[FILL]` resolved
- [ ] Route decided per B1 — do not claim a small tier before checking
- [ ] LinkedIn company page live
