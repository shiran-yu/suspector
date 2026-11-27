# Suspector support

Suspector is a free Atlassian Forge app built for Codegeist 2026 by Shiran Yu (independent developer).

![A merged pull request re-opens the tests that relied on it: Suspector's panel on an AI model work item (fictional sample project, synthetic data)](img/suspect-tests.png)

## Get help
- **Questions and bugs:** open an issue at https://github.com/shiran-yu/suspector/issues. Please include your site URL, the Jira project key, the issue key
  if one issue is affected, and what you expected to see.
- **Security reports:** please report privately via https://github.com/shiran-yu/suspector/security/advisories/new (do not open a public issue).
- Support is best effort; we aim to reply within two working days (UK time).

## Quick start
1. Install Suspector on your site (Jira required; Confluence optional for snapshots).
2. Open a Jira project → the **Suspector** tab → **Load AI radiology sample (LungScout CT)**, or classify your
   own work items with **Suspector** in each work item's details column (right-hand side).
3. Optional: Rovo chat → **Suspector Audit Prep**; MCP clients after an admin enables Suspector's tools in
   admin.atlassian.com → Apps → Sites → your site → Connected apps → Suspector. For your own agent (IDE, CI,
   terminal), add the open-source skill [skills/suspector-mcp/SKILL.md](skills/suspector-mcp/SKILL.md) (MIT).

## Common questions
- **My issues do not appear.** Suspector reads issues labelled `traceguard`, issues of a mapped type (for example
  User Need, Stakeholder Need, Requirement, System Requirement, Hazard, Risk Control, Test Case, Verification, SOUP,
  AI Model), or work items classified with Suspector in their details column.
- **No merged pull requests are shown.** Connect GitHub or Bitbucket to the site (e.g. GitHub for Atlassian);
  Suspector reads that activity through the Teamwork Graph.
- **The Suspector Audit Prep agent is missing in Rovo.** Rovo must be active on the site (Rovo chat in the top bar). Without it, the
  Gaps and Release tabs and "What must be re-verified if this changes?" on a work item give the same answers.
- **No Confluence space to publish to.** The snapshot needs Confluence with at least one space; create one, then
  reload the list on the Readiness and snapshot tab.
- **Does Suspector certify compliance?** No. It checks traceability against IEC 62304:2006+A1:2015 and
  ISO 14971:2019 and supports your quality team; it is not a conformity determination, and release decisions stay
  with your qualified people.

## Tested on requirements we did not write
The Open Patient-Controlled Analgesia Infusion Pump System Requirements 1.0.0 (SAnToS TR 2018-4-1; SAnToS Lab,
Kansas State University; first draft by Brian R. Larson), simulated requirements for a mock infusion pump published
for research and standards development, are licensed CC BY-SA 3.0 (https://creativecommons.org/licenses/by-sa/3.0/);
source: http://pub.santoslab.org/open-pca-pump/artifacts/Open-PCA-Pump-Requirements.pdf. We imported them into a Jira
project by the document's own citations: 8 goals as Stakeholder Needs, 24 exception cases as Hazards (our mapping)
and 143 requirements as System Requirements, with plain Jira links. The findings concern citations as written, not
content. Suspector reported, among others: no requirement reaches goals G6 and G7 (the authentication and
confidentiality requirements R8.1.0 and R8.2.0 cite use case UC1 or nothing); 70 of the 143 requirements reach no
goal (43 cite nothing, 23 a standard, a paper, "many EC" or "all UC and EC", which our import does not link, 2 the
placeholder "FDA ??", 1 use case UC7, which lists no goals, 1 "EC23b §4.2.22", whose section is EC22's). Readiness is
10% because only traced goals (5 of 8) can score without tests or risk estimates; this is not a judgement of the
document. Adapted by us; not affiliated with or endorsed by its authors or Kansas State University.

## Uninstall
Site admins: Jira → Apps → Manage apps → Suspector → Uninstall. See the privacy policy for what remains.

## Disclaimer
Suspector is a traceability and documentation aid for teams that build medical-device software. It is not a
medical device and is not intended for diagnosis, treatment or any clinical decision. It does not process patient
data. Readiness scores, gaps and findings are indicators for qualified people to review. They are not a
determination of conformity with IEC 62304, ISO 14971, ISO 13485, 21 CFR Part 820 or any other standard or
regulation, and not regulatory or legal advice. Clause numbers refer to IEC 62304:2006+A1:2015 and ISO 14971:2019;
standard text is not reproduced, so use your licensed copies. FDA guidance is summarised in our own words; guidance
is non-binding, so check the current version on fda.gov. If you use this software in your quality management
system, validate it for your intended use (ISO 13485:2016 clause 4.1.6; FDA Computer Software Assurance guidance).
LungScout CT and QuantMap are fictional products with synthetic data; the Open PCA requirements are credited above.
Not affiliated with or endorsed by IEC, ISO, FDA, MHRA, Kansas State University, Atlassian, GitHub or Anthropic.

Privacy policy: [PRIVACY.md](PRIVACY.md) · Terms of use: [TERMS.md](TERMS.md)
