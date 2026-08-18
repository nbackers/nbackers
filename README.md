# Nathan Backers

**Senior Solution Engineer — Apps & Agents**

I build on the Microsoft Power Platform: Copilot Studio agents, Power Apps code apps, PCF
components, Dataverse extensibility, and the automation and governance that holds it together.

This profile is a working portfolio. Every repository here is a **generic, reusable pattern**
extracted from real delivery — anonymised, documented, and published so the community can use it.
Each one starts with the problem it solves, and is explicit about what has been verified versus
what has been assumed.

---

## Portfolio

### Agents & AI

**[copilot-studio-agent-builder-skill](https://github.com/nbackers/copilot-studio-agent-builder-skill)**
*Skills that build, review and package agents for the new Copilot Studio experience.*

> **The problem:** the new Copilot Studio experience has limited file-based authoring support, and
> the Copilot Skills extension doesn't cover it. So the patterns that decide whether an agent routes
> correctly aren't written down anywhere, and every team rediscovers them the same way — usually by
> splitting into four agents that then route badly.

**Solves:** three skills covering design, routing diagnosis and packaging — with the one-agent versus
orchestrator test, routing driven by `description` rather than name, and a validator catching the
BOM, name-case and archive-root problems that break a skill upload with unhelpful errors.

---

**[copilot-retail-multiagent](https://github.com/nbackers/copilot-retail-multiagent)**
*Multi-agent orchestration reference implementation for retail operations.*

> **The problem:** most "multi-agent" demos are a single agent wearing several hats. Teams can't tell
> when orchestration genuinely earns its complexity, so they either over-engineer four agents where
> one would do, or build one overloaded agent that routes badly.

**Solves:** an orchestrator with four domain agents and six deliberately *cross-cutting* skills that
each span two or three domains — demonstrating the case where orchestration is actually justified,
alongside the counter-example and the decision framework separating them. One script rebrands the
whole set to any schema.

---

**[dataverse-document-intelligence](https://github.com/nbackers/dataverse-document-intelligence)**
*Configurable prompt-driven document processing into Dataverse.*

> **The problem:** document-processing builds are rebuilt from scratch every time because the
> extraction schema is hardcoded. Scanned documents silently return nothing. And AI writes straight
> to the system of record with no human control point, which is exactly what governance teams reject.

**Solves:** a configuration UI where users define their own capture fields; automatic detection of
scanned documents with fallback to a vision prompt; confidence and explicit `missingInformation`
surfaced for human validation; and nothing written to Dataverse until a person confirms. Documents
four undocumented AI Builder behaviours, each of which costs a day to find.

---

### Apps & Components

**[frontline-safety-copilot](https://github.com/nbackers/frontline-safety-copilot)**
*Proactive field safety, JSA and hazard identification from a photo.*

> **The problem:** frontline safety tooling is retrospective — it records incidents well and prevents
> them poorly. Job safety analysis is a form completed after the fact from memory, and the safe work
> method statement for the task sits in a document library nobody opens on a phone at the job site.

**Solves:** a job safety analysis sized for the two minutes a worker actually has, hazard
identification from a photo of the work area, controls matched by hazard type and task rather than
the whole procedure library, and a workflow that branches on what was found. Unmatched hazards are
escalated as findings rather than quietly dropped.

---

**[pcf-agent-harness-frontline](https://github.com/nbackers/pcf-agent-harness-frontline)**
*Embedding a Copilot Studio agent inside a Power App.*

> **The problem:** "how do I put my agent inside my app?" has no good published answer. Users get
> bounced out to a separate chat surface, which breaks the task they were doing and strips the agent
> of everything it could have known. Auth is the hard part and most samples skip it — so users
> already signed in are asked to sign in again, which is what SSO was meant to prevent.

**Solves:** a PCF component embedding an agent directly in a Power App, with both auth paths and the
undocumented OAuth card interception that makes SSO silent, screen context passed on conversation
start, and an offline scenario harness for demos that don't depend on the network.

---

### Automation & Governance

**[planner-premium-automation](https://github.com/nbackers/planner-premium-automation)**
*Automating Planner Premium — via Dataverse, not the Planner connector.*

> **The problem:** the Planner connector doesn't work with Planner Premium. Premium plans are Project
> for the web plans living in Dataverse as `msdyn_project*` tables, so the Planner actions return
> nothing and people conclude Planner Premium can't be automated at all.

**Solves:** documents the full Planner-to-Dataverse mapping from live metadata, and ships a working
managed solution — configured by environment variables, with a dedupe guard so repeated triggers
never duplicate cards, plus mock-schema scripts so it can be tested without a Premium licence.

---

**[copilot-credit-observability](https://github.com/nbackers/copilot-credit-observability)**
*Admin visibility over Copilot Studio credit consumption.*

> **The problem:** organisations are deploying agents with no way to answer "what will this cost at
> scale, and which agent is driving it?" Consumption data is spread across the admin centre and
> undocumented APIs, so cost surfaces only when capacity runs out — which makes agent rollout a
> governance risk rather than a managed programme.

**Solves:** collects consumption from the licensing endpoints the admin centre itself uses — verified
against a live tenant — and reports credits by agent, environment and message type, with burn rate,
days-to-exhaustion forecasting and threshold alerting. Documents the correct token audience, which is
the detail most guidance gets wrong.

---

## How I work

- **Anonymised, never borrowed.** Everything here is a generic pattern. No customer IP, data, branding or configuration.
- **Explicit about certainty.** Repos separate what was verified against a real environment from what was assumed. Documented negative findings are included, because they save the next person days.
- **Built for handover.** Configuration over customisation — environment variables, not hardcoded IDs. Solutions ship disabled so nothing runs before it's been checked.
- **Documented for the reader who's stuck.** Known gotchas, licensing traps and failure modes, not just the happy path.

---

## Areas

`Copilot Studio` · `AI agents & orchestration` · `MCP` · `Power Apps code apps` · `PCF` ·
`Dataverse` · `Power Automate` · `Power Pages` · `ALM & governance` · `React / TypeScript` · `C#` · `PowerShell`
