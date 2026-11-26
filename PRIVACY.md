# Suspector privacy policy

_Last updated: 2026-11-25. Vendor: Shiran Yu (independent developer). Contact: https://github.com/shiran-yu/suspector/issues._

Suspector is an Atlassian Forge app for Jira and Confluence that checks design-control traceability for
medical-device software (IEC 62304, ISO 14971, FDA PCCP). It runs entirely on Atlassian's Forge platform
("Runs on Atlassian"): it has no servers of its own, makes no calls outside Atlassian, and uses no AI service of
its own.

## What Suspector reads
- **Jira**, in the project you open it in: issue summaries, issue types, labels, issue links and Suspector's own
  issue property (`traceguard`).
- **Confluence**: the space you name when you publish a snapshot.
- **Teamwork Graph** (read only): development activity linked to traced Jira issues — pull-request titles and
  status, commit IDs and messages, build and deployment names and states, their times and URLs. This is used
  in memory to decide which verifications are out of date. Only the URL of each pull request or deployment and the
  time Suspector first saw it are kept in Forge storage (a merged pull request's time can move with later edits).

## What Suspector writes, and only when you or an agent you instruct asks it to
- **Jira**: the `traceguard` issue property (item kind, test results and times, risk estimates, model versions,
  review times), labels (`traceguard`, `tg-<kind>`, `traceguard-sample`), issue links, new issues (sample data or
  trace items you create) and short audit comments ("Suspector: result recorded: PASS."). Jira attributes each
  comment to the person who made the change, as it does for any comment.
- **Confluence**: snapshot pages you publish.
- **Forge storage** (per installation, per project): the software safety class you select, metadata of the
  last snapshot (time, readiness score, number of gaps, page URL and title), and the first-seen times of pull
  requests and deployments described above.

## Who is responsible
The developer named above, and not Atlassian, is responsible for the privacy, security and integrity of any data
Suspector processes. Atlassian operates the platform Suspector runs on.

## Personal data and patient data
Suspector stores no personal data in its own storage. It does not copy names, email addresses or account IDs.
Jira and Confluence content it reads or writes stays in your Atlassian site under Atlassian's privacy policy
(https://www.atlassian.com/legal/privacy-policy).
Suspector is not designed for patient data. Do not put protected health information (PHI) or other patient data in
the issues, comments or pages it reads.

## AI features
The Suspector Audit Prep agent runs in Atlassian Rovo, and Suspector's tools can be called from MCP clients through
Atlassian's MCP server after an administrator enables them and a user signs in with OAuth. Both are operated by
Atlassian under Atlassian's terms; Suspector itself makes no calls to a language model.

## Where data lives and how long
Everything stays in your Atlassian site. Forge storage is kept in the Atlassian region(s) your site uses (data
residency follows the host Atlassian app). If you uninstall Suspector, its Forge storage is soft-deleted and then
removed at the end of Atlassian's retention period for Forge hosted storage; reinstalling within 21 days can relink
the old data. The Jira issue properties, labels, comments and Confluence pages it created remain in your site until
you delete them.

## Sharing
Suspector does not sell, share or transfer data to anyone. The vendor has no access to your site's data.

## Changes
Changes to this policy are published at this address with a new date. Terms of use: [terms.md](terms.md).
