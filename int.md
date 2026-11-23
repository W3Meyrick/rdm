## 1. Diagnose before you prescribe

> "You join and inherit an SRE function of around 40 people. Within 60 days the CTO wants to know whether we're reliable *because of* our SRE practice or *despite* it. How do you find out, and what would you show them?"

**Follow-ups**
- How do you tell real reliability from luck?
- What data would you not trust?
- Who would you talk to outside SRE?

**Strong signals**
- Separates outcomes (incidents, customer impact) from capability (detection, recovery, change safety).
- Looks for near misses and heroics that are carrying the numbers.
- Talks to product teams and the service desk, not only engineers.

**Red flags**
- Goes straight to a framework rollout, a tool or a reorg without diagnosing first.

---

## 2. From SLOs to impact tolerances

> "Our regulators think in important business services and impact tolerances. Our engineers think in SLOs and error budgets. How do you connect the two so neither one turns into theatre?"

**Follow-ups**
- What happens when an SLO is green but a business service breaches tolerance?
- Who owns the mapping?
- How do you avoid 400 SLOs that nobody reads?

**Strong signals**
- Understands that customer journeys cross many services, so a dependency model is needed.
- Knows SLOs measure steady state while impact tolerances measure how long severe disruption lasts.
- Ties both to a small number of journey-level indicators.

**Red flags**
- Treats compliance as a separate workstream.
- Doesn't know that UK operational resilience rules (PRA/FCA) or the EU's DORA exist.

---

## 3. When the error budget says stop and the business says go

> "Tell me about a time a reliability signal said stop, and someone senior with real commercial reasons said go. What happened, and would you handle it the same way again?"

**Follow-ups**
- Who made the final call?
- What did you put in front of them?
- What did it cost you politically?

**Strong signals**
- Treats the error budget as an input to a business decision, not a veto.
- Makes the risk explicit and gets it owned, for example a timeboxed exception with conditions.
- Can say honestly whether the call turned out right.

**Red flags**
- "We always stop" (rigid) or "we always ship" (no backbone).
- Error-budget policies that have never actually been enforced.

---

## 4. What really happened

> "Pick a significant incident you were close to. Tell me what the postmortem concluded, then tell me what you think actually happened."

**Follow-ups**
- What made the incident *possible*, rather than what triggered it?
- What normally stops this from happening every day?
- Did the actions change anything 12 months later?

**Strong signals**
- Sees systems and organisations, not just the technology.
- Mentions production pressure, gaps in knowledge, and handoffs between teams.
- Is sceptical of a single root cause (resilience-engineering thinking, as practised at Netflix and elsewhere).

**Red flags**
- A neat linear story ending in "human error" or "we added an alert".

---

## 5. Organisation design under real constraints

> "We have hundreds of product teams, from very mature to barely operational. Some are on GCP, some are on-prem, and some sit with vendors. Design the SRE engagement model. Where do you embed, where do you centralise, and what do you refuse to do?"

**Follow-ups**
- How does SRE avoid becoming the ops team for whoever shouts loudest?
- How do teams graduate off SRE support?
- Where does platform engineering end and SRE begin?

**Strong signals**
- Uses tiered engagement based on criticality and maturity.
- Sets explicit entry and exit criteria, with production readiness as a gate.
- Can say what they would *stop* doing.
- Has a view on the relationship with platform teams.

**Red flags**
- One model for everyone.
- A structure that assumes greenfield cloud-native teams.

---

## 6. How much resilience is enough?

> "We're heavily dependent on a single hyperscaler. The board asks: 'What happens if a GCP region, or GCP itself, has a very bad day, and what should we spend to protect against it?' How do you answer?"

**Follow-ups**
- Multi-region against multi-cloud: when is each worth it?
- How would you *prove* failover works, not just assert it?
- How do you weigh concentration risk against cost and complexity?

**Strong signals**
- Reasons about cost against risk by service tier.
- Is honest that multi-cloud often adds more risk than it removes.
- Asks for evidence from failover testing and game days.
- Is aware of the regulatory focus on third parties (DORA third-party risk, UK critical third parties).

**Red flags**
- A reflexive "go multi-cloud", or "Google's SLA covers it".

---

## 7. Human sustainability

> "How would you know your on-call is becoming unhealthy *before* good people start resigning? What would you measure, and what have you actually changed in the past when it was bad?"

**Follow-ups**
- Pages per shift is easy to count. What's harder to see?
- How do you handle a team whose service is genuinely noisy and can't be fixed quickly?
- What do you do about follow-the-sun across regions?

**Strong signals**
- Uses leading indicators such as out-of-hours pages, interrupted sleep, the share of alerts that need action, and how much work is being cancelled.
- Has a clear stance that load is a product problem, not an SRE problem.
- Has made hard calls, for example handing a pager back to a development team.

**Red flags**
- "We have a rota and a wellbeing policy."

---

## 8. Building leaders, not just teams

> "Tell me about someone you developed into a strong SRE leader. What did you do that they wouldn't have got anywhere else? And who didn't work out?"

**Follow-ups**
- How do you keep senior SREs engineering rather than becoming coordinators?
- What does your career ladder reward?
- How do you hire for judgement rather than tool knowledge?

**Strong signals**
- Specific stories, with deliberate stretch assignments and sponsorship.
- Can say candidly what went wrong with the person who didn't work out.
- Has a view on keeping senior SREs technical.

**Red flags**
- Generic talk about "mentoring" with no names or examples. A director's job is to multiply leaders.

---

## 9. Automation and AI acting on production

> "Over the next three years, where should we let automation (including AI agents) take action in production without a human in the loop, and where never? How would you govern that inside a bank?"

**Follow-ups**
- What's your blast-radius model?
- How do you audit a decision an agent made?
- What's the failure mode nobody is talking about yet?

**Strong signals**
- Thinks in terms of reversibility, scope and confidence.
- Starts with read-only diagnosis and gives agents remediation powers gradually.
- Wants audit trails and clear accountability.
- Is aware of risks such as automation surprise, skills atrophy and correlated failures.
- Neither starry-eyed nor dismissive.

**Red flags**
- "AIOps will solve alert noise", or a flat refusal to engage.

---

## 10. Intellectual honesty

> "What's a widely accepted SRE practice you've stopped believing in, or now apply very differently? What changed your mind?"

**Follow-ups**
- What would it take to change your mind back?
- What do you believe that most of your peers would disagree with?

**Strong signals**
- A considered, specific position backed by experience. Examples: blamelessness without accountability doesn't work, SLOs everywhere create noise, or a 50% toil cap is unrealistic in enterprises.
- Shows they keep learning and think for themselves.

**Red flags**
- Can't think of anything, or gives a shallow contrarian take.

---
