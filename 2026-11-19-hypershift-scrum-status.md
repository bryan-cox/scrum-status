# Work Report (2026-11-17 to 2026-11-19)

*Generated from the Obsidian daily worklog using the TaskLedger status-update workflow.*

Coverage: November 17–19 inclusive, with all three daily notes available. Latest collected activity is through November 19 at 08:05 Eastern (13:05:47 UTC). Public PR states were checked at report time; changes after the worklog cutoff are called out below.

## 🦀 Things I've been working on

### [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) · CAPI manager metrics over TLS

- Opened [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323) to serve CAPI manager metrics through kube-rbac-proxy over TLS and regenerate the affected fixtures. The PR remains open.

### [OCPBUGS-134941](https://redhat.atlassian.net/browse/OCPBUGS-134941) · Show the infrastructure availability default

- Opened [openshift/hypershift #10324](https://github.com/openshift/hypershift/pull/10324) to show the SingleReplica default for `--infra-availability-policy` in the CLI. The PR remains open.

### [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969) · PR-built HyperShift v2 presubmit

- Merged the ARO HCP adapter changes in [Azure/ARO-HCP #8018](https://github.com/Azure/ARO-HCP/pull/8018) on November 17.
- Continued the CI integration in [openshift/release #88591](https://github.com/openshift/release/pull/88591) and opened draft [openshift/hypershift #10335](https://github.com/openshift/hypershift/pull/10335) to filter bootstrap capabilities against the payload schema. Both remain open.
- Investigated rehearsal failures during cluster creation. The source notes do not establish that the v2 conditions check ran successfully.

### [CNTRLPLANE-5031](https://redhat.atlassian.net/browse/CNTRLPLANE-5031) · Azure v2 CI root migration

- Opened [openshift/release #89047](https://github.com/openshift/release/pull/89047) to move Azure v2 jobs to the UK South root, investigated rehearsal failures, and retried after infrastructure fixes.
- The worklog records successful Azure KMS checks, with NodePool and route-controller checks still needing follow-up. The PR remains open.

### [CNTRLPLANE-5019](https://redhat.atlassian.net/browse/CNTRLPLANE-5019) · Dependabot PR titles

- Merged [openshift/hypershift #10326](https://github.com/openshift/hypershift/pull/10326) on November 19 to prefix Dependabot PR titles while preserving conventional commit messages. The worklog also records verification of the title-handling cases and CI checks.

### [CNTRLPLANE-4852](https://redhat.atlassian.net/browse/CNTRLPLANE-4852) · Weekday Dependabot updates

- Merged [openshift/hypershift #10347](https://github.com/openshift/hypershift/pull/10347) on November 19 to run Dependabot updates every weekday.
- The related trigger-plugin proposal, [openshift/release #89133](https://github.com/openshift/release/pull/89133), closed without merging at 08:39 Eastern, after the worklog cutoff. It is not counted as merged work.

### Verification reports and test plans

- Merged the verification report for [CNTRLPLANE-4338](https://redhat.atlassian.net/browse/CNTRLPLANE-4338) in [hypershift-community/test-results-verification #15](https://github.com/hypershift-community/test-results-verification/pull/15) on November 18.
- Recorded merge follow-up for the control-plane integration projections plan, [CNTRLPLANE-4343](https://redhat.atlassian.net/browse/CNTRLPLANE-4343) / [hypershift-community/test-results-verification #16](https://github.com/hypershift-community/test-results-verification/pull/16). That PR merged on November 16, before this reporting window.

### Non-feature work / CI Infrastructure

- Refined ARO HCP presubmit migration and validation planning under [OCPSTRAT-3557](https://redhat.atlassian.net/browse/OCPSTRAT-3557).
- Refined Azure CI migration scope and retirement planning under [OCPSTRAT-3858](https://redhat.atlassian.net/browse/OCPSTRAT-3858).
- Refined the Terraform and Argo CD provisioning scope under [CNTRLPLANE-5030](https://redhat.atlassian.net/browse/CNTRLPLANE-5030) and the migration-first adoption plan under [CNTRLPLANE-5032](https://redhat.atlassian.net/browse/CNTRLPLANE-5032).

### Code Reviews

- **35 logged review/comment entries across 32 distinct PRs**: 9 review entries and 26 comment entries. Repeated activity on one PR counts once in the distinct total.
- Reviewed: [openshift/hypershift #10000](https://github.com/openshift/hypershift/pull/10000), [openshift/hypershift #10299](https://github.com/openshift/hypershift/pull/10299), [openshift/hypershift #10320](https://github.com/openshift/hypershift/pull/10320), [openshift/release #88354](https://github.com/openshift/release/pull/88354), [openshift/release #88475](https://github.com/openshift/release/pull/88475), [openshift/release #89046](https://github.com/openshift/release/pull/89046), [openshift/hypershift #9227](https://github.com/openshift/hypershift/pull/9227), [openshift/hypershift #9795](https://github.com/openshift/hypershift/pull/9795), [openshift/hypershift #9950](https://github.com/openshift/hypershift/pull/9950).
- Commented: [openshift/hypershift #10162](https://github.com/openshift/hypershift/pull/10162), [openshift/hypershift #10208](https://github.com/openshift/hypershift/pull/10208), [openshift/hypershift #10299](https://github.com/openshift/hypershift/pull/10299), [openshift/hypershift #10313](https://github.com/openshift/hypershift/pull/10313), [bryan-cox/hypershift #421](https://github.com/bryan-cox/hypershift/pull/421), [openshift/hypershift #10047](https://github.com/openshift/hypershift/pull/10047), [openshift/hypershift #10048](https://github.com/openshift/hypershift/pull/10048), [openshift/hypershift #10086](https://github.com/openshift/hypershift/pull/10086), [openshift/hypershift #10088](https://github.com/openshift/hypershift/pull/10088), [openshift/hypershift #10119](https://github.com/openshift/hypershift/pull/10119), [openshift/hypershift #10125](https://github.com/openshift/hypershift/pull/10125), [openshift/hypershift #10176](https://github.com/openshift/hypershift/pull/10176), [openshift/hypershift #10225](https://github.com/openshift/hypershift/pull/10225), [openshift/hypershift #10308](https://github.com/openshift/hypershift/pull/10308), [openshift/hypershift #10311](https://github.com/openshift/hypershift/pull/10311), [openshift/hypershift #8392](https://github.com/openshift/hypershift/pull/8392), [openshift/hypershift #9243](https://github.com/openshift/hypershift/pull/9243), [openshift/hypershift #9512](https://github.com/openshift/hypershift/pull/9512), [openshift/hypershift #9657](https://github.com/openshift/hypershift/pull/9657), [openshift/hypershift #9658](https://github.com/openshift/hypershift/pull/9658), [openshift/hypershift #9660](https://github.com/openshift/hypershift/pull/9660), [openshift/hypershift #9787](https://github.com/openshift/hypershift/pull/9787), [openshift/hypershift #9831](https://github.com/openshift/hypershift/pull/9831), [openshift/hypershift #9835](https://github.com/openshift/hypershift/pull/9835).

## 🚧 Blockers

- The ARO HCP v2 presubmit rehearsals recorded in the worklog stopped during cluster creation before the v2 check.
- Azure v2 rehearsal follow-up still includes NodePool tests and route-controller startup; retries alone do not establish success.

## ⭐ Things I plan on working on next

- Recheck the Azure v2 retry and move [openshift/release #89047](https://github.com/openshift/release/pull/89047) toward review and merge for [CNTRLPLANE-5031](https://redhat.atlassian.net/browse/CNTRLPLANE-5031).
- Continue the payload-capability fix and CI integration for [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969), then obtain a rehearsal that reaches the v2 conditions check.
- Get review and merge progress on the CAPI metrics TLS fix for [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) and CLI default fix for [OCPBUGS-134941](https://redhat.atlassian.net/browse/OCPBUGS-134941).
- Continue the migration and Git-managed provisioning planning recorded in the worklog.

[Full, detailed status available here](https://github.com/bryan-cox/scrum-status/blob/main/2026-11-19-hypershift-scrum-status.md)
