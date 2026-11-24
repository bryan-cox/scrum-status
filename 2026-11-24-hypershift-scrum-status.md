# Work Report (2026-11-19 to 2026-11-24)

*Generated from the Obsidian daily worklog using the TaskLedger status-update workflow.*

Coverage: November 19–24 inclusive, with daily notes for November 19, 20, 23, and 24. Latest worklog activity is through November 24 at 8:06 a.m. Eastern. PR states and rehearsal evidence were checked at report time.

## 🦀 Things I've been working on

### [CNTRLPLANE-5031](https://redhat.atlassian.net/browse/CNTRLPLANE-5031) · Azure v2 CI root migration

- Merged [openshift/release #89047](https://github.com/openshift/release/pull/89047) on November 19 after a full Azure v2 rehearsal passed in UK South, including the Azure File CSI and route-controller checks, KMS secret encryption, and cleanup.

### [CNTRLPLANE-5061](https://redhat.atlassian.net/browse/CNTRLPLANE-5061) · Azure performance job migration

- Merged [openshift/release #89185](https://github.com/openshift/release/pull/89185) after the release-5.0 and release-5.1 performance periodics both passed rehearsals in UK South and produced metrics.

### [CNTRLPLANE-5029](https://redhat.atlassian.net/browse/CNTRLPLANE-5029) · Remaining Azure CI jobs

- Opened [openshift/release #89277](https://github.com/openshift/release/pull/89277) to move the release-4.22 self-managed Azure e2e jobs and the Azure deprovision periodic to UK South. The PR records passing rehearsals for the 4.22 job, the deprovision periodic, and both performance periodics. Review is in progress.

### [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969) · PR-built HyperShift v2 checks in the ARO HCP presubmit

- A targeted rehearsal of [openshift/release #88591](https://github.com/openshift/release/pull/88591) produced a passing native v2 conditions result against the provisioned HostedCluster. The latest revision lets slot-manager select the region and has a fresh rehearsal requested. The payload-capability change in [openshift/hypershift #10335](https://github.com/openshift/hypershift/pull/10335) remains in draft.

### [OCPBUGS-134941](https://redhat.atlassian.net/browse/OCPBUGS-134941) · CLI help for the infrastructure availability default

- Merged [openshift/hypershift #10324](https://github.com/openshift/hypershift/pull/10324) on November 23 to show the SingleReplica default for `--infra-availability-policy` in CLI help.

### [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) · CAPI manager metrics over TLS

- Updated [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323) to scrape CAPI manager metrics over TLS and added e2e coverage for the secured endpoint. The PR is open.

### Non-feature work / CI Infrastructure

- Consolidated the remaining AKS v1 coverage work into [CNTRLPLANE-3982](https://redhat.atlassian.net/browse/CNTRLPLANE-3982) and kept CPO compatibility and upgrade coverage under [OCPSTRAT-4074](https://redhat.atlassian.net/browse/OCPSTRAT-4074).
- The Azure v2 and performance migrations landed under [OCPSTRAT-3858](https://redhat.atlassian.net/browse/OCPSTRAT-3858). The release-4.22 and deprovision changes are the remaining job moves.

### Code Reviews

- **34 logged review/comment entries across 33 distinct PRs** with 9 review entries and 25 comment entries.
- Reviewed: [openshift/hypershift #10320](https://github.com/openshift/hypershift/pull/10320), [openshift/hypershift #7097](https://github.com/openshift/hypershift/pull/7097), [openshift/hypershift #9950](https://github.com/openshift/hypershift/pull/9950), [openshift/hypershift #10315](https://github.com/openshift/hypershift/pull/10315), [openshift/hypershift #10376](https://github.com/openshift/hypershift/pull/10376), [openshift/apiserver-network-proxy #117](https://github.com/openshift/apiserver-network-proxy/pull/117), [openshift/release #86748](https://github.com/openshift/release/pull/86748), [openshift/release #86870](https://github.com/openshift/release/pull/86870), [openshift-eng/ai-helpers #871](https://github.com/openshift-eng/ai-helpers/pull/871).
- Commented: [openshift/hypershift #10047](https://github.com/openshift/hypershift/pull/10047), [openshift/hypershift #10048](https://github.com/openshift/hypershift/pull/10048), [openshift/hypershift #10086](https://github.com/openshift/hypershift/pull/10086), [openshift/hypershift #10088](https://github.com/openshift/hypershift/pull/10088), [openshift/hypershift #10119](https://github.com/openshift/hypershift/pull/10119), [openshift/hypershift #10125](https://github.com/openshift/hypershift/pull/10125), [openshift/hypershift #10162](https://github.com/openshift/hypershift/pull/10162), [openshift/hypershift #10176](https://github.com/openshift/hypershift/pull/10176), [openshift/hypershift #10225](https://github.com/openshift/hypershift/pull/10225), [openshift/hypershift #10308](https://github.com/openshift/hypershift/pull/10308), [openshift/hypershift #10311](https://github.com/openshift/hypershift/pull/10311), [openshift/hypershift #10313](https://github.com/openshift/hypershift/pull/10313), [bryan-cox/hypershift #421](https://github.com/bryan-cox/hypershift/pull/421), [openshift/hypershift #8392](https://github.com/openshift/hypershift/pull/8392), [openshift/hypershift #9227](https://github.com/openshift/hypershift/pull/9227), [openshift/hypershift #9243](https://github.com/openshift/hypershift/pull/9243), [openshift/hypershift #9512](https://github.com/openshift/hypershift/pull/9512), [openshift/hypershift #9657](https://github.com/openshift/hypershift/pull/9657), [openshift/hypershift #9658](https://github.com/openshift/hypershift/pull/9658), [openshift/hypershift #9660](https://github.com/openshift/hypershift/pull/9660), [openshift/hypershift #9787](https://github.com/openshift/hypershift/pull/9787), [openshift/hypershift #9831](https://github.com/openshift/hypershift/pull/9831), [openshift/hypershift #9835](https://github.com/openshift/hypershift/pull/9835), [openshift/hypershift #9850](https://github.com/openshift/hypershift/pull/9850).

## ⭐ Things I plan on working on next

- Address review feedback on [openshift/release #89277](https://github.com/openshift/release/pull/89277) for [CNTRLPLANE-5029](https://redhat.atlassian.net/browse/CNTRLPLANE-5029). Follow up on the remaining old credential mounts before retiring the old Azure CI root.
- Verify the ARO HCP presubmit rehearsal on the updated region-selection change and move [openshift/release #88591](https://github.com/openshift/release/pull/88591) toward merge for [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969).
- Get [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323) reviewed for [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) and continue the AKS v1 coverage migration under [CNTRLPLANE-3982](https://redhat.atlassian.net/browse/CNTRLPLANE-3982).

[Full, detailed status available here](https://github.com/bryan-cox/scrum-status/blob/main/2026-11-24-hypershift-scrum-status.md)
