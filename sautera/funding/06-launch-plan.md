# NUTMEG Launch Plan — Dual US/Grenadian Citizen

**Owner status:** US citizen **and** Grenadian citizen.
**Supersedes** the structural reasoning in `01`–`05`. Those remain useful for
detail and for the record of what was ruled out; this is the plan.
**Not legal or tax advice.** §7 lists what must be confirmed and by whom.

---

## 1. The answer

> **Register a Grenadian private limited company. Own 100% of it yourself.
> File Form 8832 to have it treated as a disregarded entity for US tax.
> Build nothing else until you have revenue.**

That is the whole structure. One entity, one owner, one election.

---

## 2. What Grenadian citizenship changes

Substantially more than it looks. Every one of these was live friction in the
earlier documents and is now simply gone:

| Was a problem | Status now |
|---|---|
| WiPay won't onboard a foreign entity | Local company, local citizen director, local ID. Routine. |
| Foreign company must also register as an external company in Grenada | Not applicable — you are local |
| Alien landholding licence / foreign investment restrictions | Not applicable |
| Local bank account hard to open | Citizen opening a local business account. Normal. |
| Work permit to operate | Not applicable |
| "Foreign company running Grenadian transport" optics with driver associations, schools, ministries | Reversed — you are Grenadian, building for Grenada |
| Needing a US parent for credibility | Never real; now obviously unnecessary |

The legitimacy point is not a positioning trick. A Grenadian citizen building
Grenada's first integrated transport platform, named for the national symbol, is
the strongest possible position in the rooms where you need cooperation:
driver associations, school administrations, the transport and education
ministries. Do not dilute it with an offshore wrapper.

---

## 3. What it does NOT change — read this part twice

**Grenadian citizenship gives you exactly zero relief from US tax.**

The US taxes its citizens on **worldwide income**, regardless of any other
citizenship, regardless of where you live, regardless of where the company is.
Dual citizenship is irrelevant to this. There is no election, no treaty
position, and no structure that changes it.

Anyone who tells you otherwise is either wrong or selling something. See §6.

The only thing that ends US tax obligations is renouncing US citizenship, which
triggers an exit tax under §877A and is wildly disproportionate to a
pre-revenue transport app. Named here only so you know the actual shape of the
problem: **there is no clever way out, so stop looking for one and just get the
classification right.**

---

## 4. Why disregarded, not a corporation

Both are legal. One is obviously better for where you are.

| | Disregarded (Form 8832) | Corporation (CFC) |
|---|---|---|
| US form | 8858 | **5471** |
| Penalty if missed | $10,000 | $10,000 + open statute of limitations on your entire return |
| GILTI | Doesn't apply | Applies to undistributed profit |
| **Pre-revenue losses** | **Flow through to your 1040** | **Trapped in the CFC** |
| Complexity | Low | High |

You are pre-revenue with real costs — AWS, Twilio, development time. Under
disregarded treatment those losses land on your return and can offset other
income **now**. Under CFC treatment they sit inside the company doing nothing
until it has income to absorb them.

Revisit when NUTMEG is profitable and you want to retain earnings in Grenada
rather than distribute. That is a good problem and years away. Corporation
treatment plus a §962 election is the tool then, not now.

### 4.1 The 75-day clock

Form 8832 can be made effective up to **75 days before** the date it is filed.
File it within 75 days of the company's formation and the election applies from
day one — no gap where default classification governs.

**Miss that window and you may be stuck with the default for the first period.**
Put the date in your calendar the day the company is registered.

---

## 5. The sequence

### This week — nothing here waits on anything else

1. **Register the domain. Build a real website. Set up email on that domain.**
   Apple *requires* a publicly available, functional site on your own domain and
   a work email on it — a registrar parking page is explicitly rejected
   (`04` §1). AWS Activate and Twilio both expect a live site too. **One task
   unblocks three things and depends on nothing. It is the single highest-leverage
   item in the entire plan.**

2. **Check two country dropdowns — ten minutes.** Start Apple's organization
   enrollment and Google's Play Console signup, look for Grenada in the entity
   country selector, abandon both before payment. See `04` §6. This closes the
   largest remaining unknown for free.

3. **Book the US international tax specialist.** Screen on: *"Do you prepare
   Forms 5471 and 8858, and have you made §962 elections?"* Vague answer, next
   candidate. Bring the questions in §7.

### Then, in order

4. **Confirm the entity form with the specialist before filing anything.**
   Treas. Reg. §301.7701-2(b)(8) lists foreign entity types permanently
   classified as corporations, with Form 8832 unavailable forever. Commonwealth
   Caribbean jurisdictions appear on that list. **Grenada's entry is unverified.**
   Register the wrong form and you are locked into CFC treatment for the life of
   the company.
5. **Register the company** at the Grenada corporate registry, in the form the
   specialist names.
6. **File Form 8832** within 75 days (§4.1).
7. **Open the local bank account. Onboard WiPay.**
8. **D-U-N-S number** — check whether one already exists before requesting.
   Apple says ~5 business days; plan for weeks (`04` §2.1).
9. **Apple + Google organization developer accounts.**
10. **Then** the funding applications in `02` and `03`, and S-21 app store
    submission.

---

## 6. What not to do

Everything on this list will be suggested to you by someone. All of it is wrong
for your situation.

- **Don't form a US LLC to hold NUTMEG.** Solves nothing operationally; if
  single-member it's disregarded anyway and adds only admin; links NUTMEG,
  SAUTERA and CLIVE for liability instead of separating them. (`05` §4)
- **Don't incorporate in Barbados**, or anywhere else regional. You'd need
  Grenada registration anyway, you'd add a currency layer to driver payouts,
  and the treaty everyone cites is neutralised for US citizens by the saving
  clause.
- **Don't buy an offshore or IBC structure.** As a US citizen these are actively
  worse: CFC treatment, possible PFIC exposure, Form 5471, and a compliance
  profile that reads badly. They are sold hard to dual citizens. The pitch is
  always some version of "legally invisible to the IRS." That does not exist for
  a US citizen.
- **Don't chase a low-tax jurisdiction.** Low local tax means low foreign tax
  credit, so you hand the difference to the IRS instead. Offshore is worth far
  less to US persons than its reputation.
- **Don't use a general accountant.** Forms 5471/8858 and GILTI are routinely
  missed by competent generalists. Penalties start at $10,000 before any tax is
  owed.
- **Don't renounce US citizenship over this.** §877A exit tax, and it is
  absurdly disproportionate to the problem.
- **Don't wait for a perfect structure before shipping.** The structure above is
  correct and takes weeks. S-17 through S-24 are the actual work.

---

## 7. Take these to the specialist

1. Is Grenada on the §301.7701-2(b)(8) per se list, and **which Grenadian entity
   form preserves the check-the-box option?** *(Before registration — this is
   irreversible.)*
2. Confirm disregarded treatment beats CFC treatment pre-revenue, and name the
   trigger to switch later.
3. Calendar the Form 8832 filing deadline from the registration date.
4. FBAR and Form 8938: what is reportable once the Grenadian account opens, and
   does signature authority pull in anything else?
5. Does the **school wallet** — holding customer funds — change any of the above?
6. **Residence:** if you are a bona fide resident of Grenada, FEIE (Form 2555)
   can shelter a *salary* from NUTMEG — but it does **not** shelter GILTI or
   Subpart F inclusions. If you remain resident in a US state, check whether that
   state follows the federal foreign provisions; several don't.

---

## 8. Still unverified, and honestly so

Two things could not be confirmed from this environment, because irs.gov,
law.cornell.edu, ecfr.gov, govinfo.gov and support.google.com are all blocked by
its network egress policy:

1. **Grenada's entry (if any) on the §301.7701-2(b)(8) per se list.** Closed by
   the specialist, before registration.
2. **Grenada on Google Play's supported-locations table**, and Grenada in
   Apple's enrollment country selector. Closed by you, in ten minutes, per §5.2.

Every US tax figure in these documents comes from corroborating practitioner
secondary sources rather than the statute. Treat them as planning-grade and have
them confirmed.

**Neither unknown blocks step 1.** Start the website today.
