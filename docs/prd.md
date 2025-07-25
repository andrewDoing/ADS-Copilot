# Architecture Design Session Agent – Product Requirements Document

**Basics / Metadata**  

- Target release: August 15, 2025  
- Current status: Draft  
- Core team:  
  - Product Owner: Andrew Vineyard  
  - Engineering Lead: TBD  
  - AI/Prompt Engineer: TBD  
  - UX Designer: TBD  

---

## Objective & Success Metrics  

- **Primary KPI**: Reduce average Architecture Design Session (ADS) turnaround time by **70% within 60 days** of internal GA  
- **Secondary KPI**: ≥ 80% of PRDs and architecture docs generated by the agent receive "ready for dev" sign-off on first review  
- **Tertiary KPI**: ≥ 90% backlog population accuracy vs. human-authored epics/stories (based on peer review sample)  

---

## Background & Strategic Fit  

- Architecture Design Sessions are high-leverage but high-effort planning rituals at Microsoft. They often produce incomplete or inconsistent outputs (PRDs, architecture diagrams, backlogs).  
- This agent aims to reduce manual effort by automating draft generation using prompt-driven AI aligned to the ISE Playbook and Azure Well-Architected Framework.  
- It supports our broader strategic goal of scaling engineering throughput and minimizing time-to-planning while preserving quality.  

---

## Assumptions & Risks  

**Assumptions**  

- Prompt-tuned LLMs (Large Language Models) are capable of generating draft-quality engineering artifacts when guided by structured templates  
- Teams are open to reviewing and refining AI-generated outputs rather than authoring from scratch  
- Azure DevOps MCP (Microsoft Cloud Partner) access can be leveraged for backlog injection  

**Risks**  

- AI-generated content may include hallucinations or misalign with org-specific architectural norms  
- Poor prompt hygiene may lead to low-quality outputs or security oversights  
- Too much automation may bypass necessary human judgment for complex systems  

---

## User Personas  

- **Tech Lead (primary)**: Responsible for facilitating ADS sessions and producing PRD/architecture documentation. Needs rapid, structured drafts.  
- **Product Manager**: Needs to translate vision into scoped documentation and story breakdowns. Prefers clear traceability from goals to execution.  
- **Software Engineer**: Consumes PRD and stories. Needs outputs to be accurate and implementation-ready.  
- **Program Manager**: Tracks delivery. Needs artifacts that align with milestones and stakeholder expectations.  

---

## User Stories / Requirements  

### PRD & Architecture Generation  

- As a Tech Lead, I want to enter a few key product ideas and generate a full PRD in Atlassian format.  
- As a Tech Lead, I want a draft architecture aligned to Azure Well-Architected pillars based on the PRD.  

### Backlog Generation  

- As a Product Manager, I want epics and user stories automatically created from the PRD with traceable links to the objectives.  
- As a PM, I want stories pushed into Azure DevOps with appropriate labels, owners, and estimates.  

### Task-Specific Prompt Access  

- As a user, I want access to structured prompts for:  
  - Writing PRDs  
  - Designing Azure architectures  
  - Creating backlogs (epics/stories/tasks)  
  - Writing test/verification plans  
  - Generating sprint plans  
  - Drafting roll-out and communication plans  

### Artifact Bundling  

- As a Tech Lead, I want to download or share a complete “ADS Packet” including the PRD, architecture diagram, backlog CSV, and verification plan.

---

## Scope & Out-of-Scope  

**In Scope**  

- PRD generation based on napkin input or bullets  
- Azure architecture diagrams (text + Mermaid + ARM/bicep pseudocode)  
- Azure DevOps backlog population via MCP  
- SMART KPIs and analytics hooks auto-included in plans  
- Roll-out playbook generation for MVPs  

**Out-of-Scope**  

- Production-grade architecture validation  
- Security review automation  
- E2E DevOps pipeline deployment (out of MVP scope, potential v2)  
- AI-generated legal/disclosure content  

---

## Design References  

- [Atlassian PRD Template](https://www.atlassian.com/software/confluence/templates/product-requirements)  
- [Microsoft ISE Engineering Playbook](https://github.com/microsoft/code-with-engineering-playbook)  
- [Azure Well-Architected Framework](https://learn.microsoft.com/en-us/azure/architecture/framework/)  
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/claude/docs/prompt-engineering-guide)  

---

## Analytics / Instrumentation Plan  

- Track number of PRDs, architectures, and backlogs generated per week  
- Track % of AI-generated artifacts marked "ready" by engineering sign-off  
- Time to completion vs. manual process baseline  
- Prompt usage analytics and drop-off points  

---

## Launch & Roll-out  

**Pilot (Week 1–2)**  

- Internal MVP used by 1–2 engineering pods  
- Daily feedback loop and tuning of prompt templates  

**Internal Beta (Week 3–4)**  

- Available to all ISE engineering leads and PMs  
- Weekly patch releases based on usage feedback  

**GA (Week 5+)**  

- Documented onboarding  
- Integrated into ADS prep workflows via Teams + DevOps plugins  
- Optional: Copilot plugin integration for PRD/startup planning workflows  

---

## Open Questions  

- What DevOps permissions and scopes are needed for MCP backlog injection?  
- Should we support GitHub Projects as an alternative to Azure DevOps for backlogs?  
- What security model do we use for prompt templates (e.g., if a team wants to customize?)  
- How should we version prompt packs across teams or use cases?  
- Who owns long-term prompt refinement and performance evaluation?
