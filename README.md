<div align="center">

# Nathan Backers

**Senior Solution Engineer · Apps & Agents**

Microsoft Power Platform · Copilot Studio · Dataverse · PCF

[![Copilot Studio](https://img.shields.io/badge/Copilot_Studio-0F6CBD?style=for-the-badge&logo=microsoft&logoColor=white)](https://github.com/nbackers)
[![Power Platform](https://img.shields.io/badge/Power_Platform-742774?style=for-the-badge&logo=microsoftpowerplatform&logoColor=white)](https://github.com/nbackers)
[![Dataverse](https://img.shields.io/badge/Dataverse-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)](https://github.com/nbackers)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://github.com/nbackers)

</div>

---

## About

I build agents and applications on the Microsoft Power Platform, and the automation and governance
that keeps them running once they are real.

This profile is a **working portfolio**. Every repository is a generic, reusable pattern extracted
from real delivery, anonymised and documented so the community can use it.

> Each repo opens with the problem it solves, and states plainly what has been **verified** against
> a live environment versus what has been **assumed**. Documented negative findings are included,
> because they save the next person days.

---

## Portfolio

### Agents & AI

<table>
<tr>
<td width="50%" valign="top">

#### [Agent Builder Skill](https://github.com/nbackers/copilot-studio-agent-builder-skill)

![Skills](https://img.shields.io/badge/3_skills-0F6CBD?style=flat-square)
![Validator](https://img.shields.io/badge/validator-tested-success?style=flat-square)

**Problem:** the new Copilot Studio experience has limited file-based authoring, so the patterns
that decide whether an agent routes correctly are written down nowhere. Every team rediscovers
them the hard way.

**Solves:** skills for design, routing diagnosis and packaging, plus a validator catching the BOM,
name-case and archive-root faults that break an upload with unhelpful errors.

</td>
<td width="50%" valign="top">

#### [Retail Multi-Agent](https://github.com/nbackers/copilot-retail-multiagent)

![Agents](https://img.shields.io/badge/orchestrator_+_4_agents-0F6CBD?style=flat-square)
![Skills](https://img.shields.io/badge/6_cross--cutting_skills-742774?style=flat-square)

**Problem:** most multi-agent demos are one agent wearing several hats. Teams cannot tell when
orchestration earns its complexity, so they over-engineer four agents that route badly.

**Solves:** an orchestrator with four domain agents and six deliberately cross-cutting skills,
plus the decision framework for when *not* to split.

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [Document Intelligence](https://github.com/nbackers/dataverse-document-intelligence)

![AI Builder](https://img.shields.io/badge/AI_Builder-742774?style=flat-square)
![Findings](https://img.shields.io/badge/4_undocumented_findings-important?style=flat-square)

**Problem:** extraction is rebuilt every project because the schema is hardcoded, scanned documents
silently return nothing, and AI writes to the system of record unchecked.

**Solves:** user-defined capture fields, automatic scan detection with a vision fallback, and a
human validation gate before anything persists.

</td>
<td width="50%" valign="top">

#### [Frontline Safety Copilot](https://github.com/nbackers/frontline-safety-copilot)

![Vision](https://img.shields.io/badge/multimodal-0F6CBD?style=flat-square)
![Safety](https://img.shields.io/badge/safety_critical-critical?style=flat-square)

**Problem:** safety tooling is retrospective. It records incidents well and prevents them poorly.
The procedure that matters sits in a library nobody opens at the job site.

**Solves:** a JSA sized for the two minutes a worker has, hazard identification from a photo, and
controls matched to the hazard rather than the whole library.

</td>
</tr>
</table>

### Apps & Components

<table>
<tr>
<td width="50%" valign="top">

#### [PCF Agent Harness](https://github.com/nbackers/pcf-agent-harness-frontline)

![Build](https://img.shields.io/badge/build-passing-success?style=flat-square)
![Tests](https://img.shields.io/badge/tests-11_passing-success?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Problem:** "how do I put my agent inside my app?" has no good published answer. Users get bounced
to a separate surface, and the SSO path still prompts them to sign in again.

**Solves:** a PCF control embedding an agent in a Power App, with the undocumented OAuth card
interception that makes SSO silent, plus an offline demo harness.

</td>
<td width="50%" valign="top">

#### [Planner Premium Automation](https://github.com/nbackers/planner-premium-automation)

![Solution](https://img.shields.io/badge/managed_solution-742774?style=flat-square)
![Mock schema](https://img.shields.io/badge/mock_schema-included-success?style=flat-square)

**Problem:** the Planner connector does not work with Planner Premium. Premium plans live in
Dataverse as `msdyn_project*`, so the Planner actions return nothing and people conclude it cannot
be automated.

**Solves:** the full Planner-to-Dataverse mapping from live metadata, and a working solution with
a dedupe guard, testable without a Premium licence.

</td>
</tr>
</table>

### Governance & Operations

<table>
<tr>
<td width="50%" valign="top">

#### [Copilot Credit Observability](https://github.com/nbackers/copilot-credit-observability)

![Verified](https://img.shields.io/badge/verified-live_tenant-success?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)

**Problem:** organisations deploy agents with no way to answer "what will this cost at scale, and
which agent is driving it?" Cost becomes visible when capacity runs out.

**Solves:** collects consumption from the licensing endpoints the admin centre itself uses,
verified against a live tenant, with burn rate and days-to-exhaustion forecasting.

</td>
<td width="50%" valign="top">

#### More on the way

Patterns are extracted and published as they generalise cleanly.

Contributions and corrections are welcome, particularly **verification results** from your own
tenant. Several findings are marked unverified precisely so someone can close them out.

</td>
</tr>
</table>

---

## How I work

| Principle | In practice |
|---|---|
| **Anonymised, never borrowed** | Generic patterns only. No customer IP, data, branding or configuration. |
| **Explicit about certainty** | Repos separate what was verified live from what was assumed, and publish negative findings. |
| **Built for handover** | Configuration over customisation. Environment variables, not hardcoded IDs. Solutions ship disabled. |
| **Documented for the reader who is stuck** | Known gotchas, licensing traps and failure modes, not just the happy path. |

---

## Stack

![Copilot Studio](https://img.shields.io/badge/Copilot_Studio-0F6CBD?style=flat-square&logo=microsoft&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square)
![Dataverse](https://img.shields.io/badge/Dataverse-0078D4?style=flat-square&logo=microsoftazure&logoColor=white)
![Power Apps](https://img.shields.io/badge/Power_Apps-742774?style=flat-square&logo=microsoftpowerapps&logoColor=white)
![Power Automate](https://img.shields.io/badge/Power_Automate-0066FF?style=flat-square&logo=microsoftpowerautomate&logoColor=white)
![Power Pages](https://img.shields.io/badge/Power_Pages-742774?style=flat-square)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)
![PCF](https://img.shields.io/badge/PCF-0F6CBD?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)

<div align="center">

---

*Every repository states what it solves, what is verified, and what is not.*

</div>
