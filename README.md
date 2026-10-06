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

This profile is a **pattern library**. Each repository demonstrates a reusable approach to a common
problem, published so others can adapt it, and is labelled with how far it has been taken:

| Maturity | Meaning |
|---|---|
| ![Implemented](https://img.shields.io/badge/implemented-success?style=flat-square) | Builds or imports, with tests or a repeatable check. Use as a starting point. |
| ![Working tool](https://img.shields.io/badge/working_tool-blue?style=flat-square) | Scripts or skills you can run today, validated in CI. |
| ![Design reference](https://img.shields.io/badge/design_reference-lightgrey?style=flat-square) | Architecture, prompts and tested guard code. Not a deployable solution. |

> Every repo states plainly what has been **verified** against a live environment, what is covered
> by **tests**, and what is **not yet verified**. Dated platform findings are included, because they
> save the next person days, and they are flagged when the platform moves on.

> **These are samples, not products.** Provided as is, not production ready, and not affiliated with
> or endorsed by Microsoft. Review, test and harden before any real use.

---

## Portfolio

### Agents & AI

<table>
<tr>
<td width="50%" valign="top">

#### [Agent Builder Skills](https://github.com/nbackers/copilot-studio-agent-builder-skill)

![Maturity](https://img.shields.io/badge/working_tool-blue?style=flat-square)
![Skills](https://img.shields.io/badge/5_skills-0F6CBD?style=flat-square)
![Tests](https://img.shields.io/badge/tests-17_passing-success?style=flat-square)

**Problem:** the Copilot Studio VS Code extension targets the standard harness. Agents on the
GitHub Copilot harness get no clone-edit-sync loop, so the harness built for the most capable agents
has the least local tooling.

**Approach:** a VS Code plugin whose skills scaffold, package, review and deploy those agents by
driving `pac` directly, a skill packager that catches the faults that stop a skill activating, and a
routing scorer that measures which child agent each question reached.

</td>
<td width="50%" valign="top">

#### [Retail Multi-Agent](https://github.com/nbackers/copilot-retail-multiagent)

![Maturity](https://img.shields.io/badge/design_reference-lightgrey?style=flat-square)
![Agents](https://img.shields.io/badge/orchestrator_+_4_agents-0F6CBD?style=flat-square)

**Problem:** most multi-agent demos are one agent wearing several hats. Teams cannot tell when
orchestration earns its complexity, so they over-engineer four agents that route badly.

**Approach:** an orchestrator with four domain agents and cross-cutting skills, the decision
framework for when *not* to split, an idempotent Dataverse schema script to build against, and the
same shape mapped to four other industries.

</td>
</tr>
<tr>
<td width="50%" valign="top">

#### [Document Intelligence](https://github.com/nbackers/dataverse-document-intelligence)

![Maturity](https://img.shields.io/badge/design_reference-lightgrey?style=flat-square)
![Tests](https://img.shields.io/badge/tests-43_passing-success?style=flat-square)
![AI Builder](https://img.shields.io/badge/AI_Builder-742774?style=flat-square)

**Problem:** extraction is rebuilt every project because the schema is hardcoded, scanned documents
silently return nothing, and model output is trusted as-is.

**Approach:** user-defined capture fields, scan detection with a vision fallback, output validation
that enforces the contract in code, a human validation gate, and dated AI Builder findings.

</td>
<td width="50%" valign="top">

#### [Frontline Safety Copilot](https://github.com/nbackers/frontline-safety-copilot)

![Maturity](https://img.shields.io/badge/design_reference-lightgrey?style=flat-square)
![Tests](https://img.shields.io/badge/tests-30_passing-success?style=flat-square)
![Safety](https://img.shields.io/badge/safety_critical-critical?style=flat-square)

**Problem:** safety tooling is retrospective. It records incidents well and prevents them poorly.
The procedure that matters sits in a library nobody opens at the job site.

**Approach:** a JSA sized for the two minutes a worker has, photo hazard identification, and
deterministic guards so the emergency stop, procedure allow-list and escalation never depend on the
model.

</td>
</tr>
</table>

### Apps & Components

<table>
<tr>
<td width="50%" valign="top">

#### [PCF Copilot Studio Agent](https://github.com/nbackers/pcf-copilot-studio-agent)

![Maturity](https://img.shields.io/badge/implemented-success?style=flat-square)
![Tests](https://img.shields.io/badge/tests-31_passing-success?style=flat-square)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Problem:** "how do I put my agent inside my app?" has no good published answer. Users get bounced
to a separate surface, and the SSO path can prompt them to sign in again.

**Approach:** a PCF component embedding a Copilot Studio agent in canvas apps and model-driven forms,
with OAuth card interception for silent SSO (unit tested; live tenant unverified), record context
from the host form, untrusted-context handling and an offline demo mode.

</td>
<td width="50%" valign="top">

#### [Planner Premium Automation](https://github.com/nbackers/planner-premium-automation)

![Maturity](https://img.shields.io/badge/implemented-success?style=flat-square)
![Solution](https://img.shields.io/badge/solution-source_included-742774?style=flat-square)
![Mock schema](https://img.shields.io/badge/mock_schema-included-success?style=flat-square)

**Problem:** the Planner connector does not see Planner Premium. Premium plans live in Dataverse as
`msdyn_project*`, so the Planner actions return nothing and people conclude it cannot be automated.

**Approach:** a read-only connectivity and permissions check, the table map from live metadata, an
example flow you retrofit to any process, and six recipes from read-only digests to plan templates.
Rehearse with mock tables without a Premium licence (a Dataverse environment is still needed).

</td>
</tr>
</table>

### Governance & Operations

<table>
<tr>
<td width="50%" valign="top">

#### [Copilot Credit Observability](https://github.com/nbackers/copilot-credit-observability)

![Maturity](https://img.shields.io/badge/working_tool-blue?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black)

**Problem:** organisations deploy agents with no way to answer "what will this cost at scale, and
where is it being consumed?" Cost becomes visible when capacity runs out.

**Approach:** collects consumption from the supported Power Platform licensing API with a fallback
to the admin centre endpoints, flags consumption in environments with no allocation, alerts before
capacity runs out, and allocates every credit to a cost centre for chargeback.

</td>
<td width="50%" valign="top">

#### More on the way

New patterns are published as they are generalised and tested.

Contributions and corrections are welcome, particularly **verification results** from your own
tenant. Each repo has an issue template for exactly that.

</td>
</tr>
</table>

---

## How I work

| Principle | In practice |
|---|---|
| **Generic, reusable patterns** | Each repo stands alone. No customer data, branding or configuration. |
| **Explicit about certainty** | Maturity labels, verified versus unverified, and dated findings that are revisited when the platform changes. |
| **Guardrails in code** | Where a wrong model answer matters, the rule is enforced deterministically and tested, not only asked for in a prompt. |
| **Built for handover** | Configuration over customisation. Environment variables, not hardcoded IDs. Scripts that change an environment say so. |
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

*Every repository states what it does, how far it has been taken, and what is not yet verified.*

**Sample code.** Provided as is, without warranty. Not production ready. Not an official Microsoft
product, and not affiliated with or endorsed by Microsoft.

</div>
