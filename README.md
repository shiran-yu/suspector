# TraceGuard support

TraceGuard is a free Atlassian Forge app built for Codegeist 2026 by Shiran Yu (independent developer).

## Get help
- **Questions and bugs:** open an issue at https://github.com/shiran-yu/traceguard/issues. Please include your site URL, the Jira project key, the issue key
  if one issue is affected, and what you expected to see.
- **Security reports:** please report privately via https://github.com/shiran-yu/traceguard/security/advisories/new (do not open a public issue).
- Support is best effort; we aim to reply within two working days (UK time).

## Quick start
1. Install TraceGuard on your site (Jira required; Confluence optional for snapshots).
2. Open a Jira project → the **TraceGuard** tab → **Load AI radiology sample (LungScout CT)**, or classify your
   own work items with **TraceGuard** in each work item's details column (right-hand side).
3. Optional: Rovo chat → **TraceGuard Auditor**; MCP clients after an admin enables TraceGuard's tools in
   admin.atlassian.com → Apps → Sites → your site → Connected apps → TraceGuard. For your own agent (IDE, CI,
   terminal), add the open-source skill [skills/traceguard-mcp/SKILL.md](skills/traceguard-mcp/SKILL.md) (MIT).

## Common questions
- **My issues do not appear.** TraceGuard reads issues labelled `traceguard`, issues of a mapped type (User Need,
  Requirement, Hazard, Risk Control, Test, Test Case, SOUP, AI Model), or work items classified with TraceGuard in their details column.
- **No merged pull requests are shown.** Connect GitHub or Bitbucket to the site (e.g. GitHub for Atlassian);
  TraceGuard reads that activity through the Teamwork Graph.
- **The Auditor is missing in Rovo.** Rovo must be active on the site (Rovo chat in the top bar). Without it, the
  Gaps and Release tabs and "What must be re-verified if this changes?" on a work item give the same answers.
- **No Confluence space to publish to.** The snapshot needs Confluence with at least one space; create one, then
  reload the list on the Readiness and snapshot tab.
- **Does TraceGuard certify compliance?** No. It checks traceability against IEC 62304:2006+A1:2015 and
  ISO 14971:2019 and supports your quality team; it is not a compliance determination.

## Uninstall
Site admins: Jira → Apps → Manage apps → TraceGuard → Uninstall. See the privacy policy for what remains.

Privacy policy: [PRIVACY.md](PRIVACY.md)
