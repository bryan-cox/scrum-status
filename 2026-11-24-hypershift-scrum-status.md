# Work Report (2026-11-19 to 2026-11-24)

*Generated from the Obsidian daily worklog using the TaskLedger status-update workflow.*

Coverage: November 19–24 inclusive, with daily notes for November 19, 20, 23, and 24. Latest worklog activity is through November 24 at 8:06 a.m. Eastern. GitHub PR states and Prow rehearsal results were rechecked on November 24. The later CAPI metrics update is dated separately.

## 🦀 Things I've been working on

### [CNTRLPLANE-5031](https://redhat.atlassian.net/browse/CNTRLPLANE-5031) · Azure v2 CI root migration

- The OpenShift merge bot merged [openshift/release #89047](https://github.com/openshift/release/pull/89047) on November 19. The full Azure v2 rehearsal passed in UK South on the earlier revision `6d27eb2`.

### [CNTRLPLANE-5061](https://redhat.atlassian.net/browse/CNTRLPLANE-5061) · Azure performance job migration

- The OpenShift merge bot merged [openshift/release #89185](https://github.com/openshift/release/pull/89185). The release-5.0 and release-5.1 performance rehearsals both passed in UK South on `47b6630` and each produced metrics files.

### [CNTRLPLANE-5029](https://redhat.atlassian.net/browse/CNTRLPLANE-5029) · Remaining Azure CI jobs

- [openshift/release #89277](https://github.com/openshift/release/pull/89277) is **open**. It proposes moving the release-4.22 self-managed Azure e2e jobs and deprovision periodic to UK South. The 4.22 e2e, deprovision, and both performance rehearsals passed on `4b5650f`. On `5d5f1b4`, deprovision passed and the 4.22 e2e rerun was pending when checked.

### [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969) · Native HyperShift v2 conditions in the ARO HCP presubmit

- An earlier rehearsal of [openshift/release #88591](https://github.com/openshift/release/pull/88591) on `c2be601` passed one native HyperShift v2 conditions test using a build of HyperShift main. The rerun for slot-manager region selection on `4e598cf` was pending when checked. The payload capability change in [openshift/hypershift #10335](https://github.com/openshift/hypershift/pull/10335) remains an open draft.

### [OCPBUGS-134941](https://redhat.atlassian.net/browse/OCPBUGS-134941) · CLI help for the infrastructure availability default

- The OpenShift merge bot merged [openshift/hypershift #10324](https://github.com/openshift/hypershift/pull/10324) on November 23 to show the SingleReplica default for `--infra-availability-policy` in CLI help.

### [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) · CAPI manager metrics over TLS

- The worklog records HTTP metrics and PodMonitor changes in [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323). A later update at 9:35 a.m. Eastern added the TLS implementation and an e2e test. The PR remains open.

### Non-feature work / CI Infrastructure

- Closed [CNTRLPLANE-3455](https://redhat.atlassian.net/browse/CNTRLPLANE-3455) and [CNTRLPLANE-3456](https://redhat.atlassian.net/browse/CNTRLPLANE-3456) as duplicates of the AKS v1 coverage epic [CNTRLPLANE-3982](https://redhat.atlassian.net/browse/CNTRLPLANE-3982). CPO compatibility and upgrade coverage is tracked under [OCPSTRAT-4074](https://redhat.atlassian.net/browse/OCPSTRAT-4074).
- The Azure CI migration is tracked under [OCPSTRAT-3858](https://redhat.atlassian.net/browse/OCPSTRAT-3858).

### Code Reviews

- **34 logged review/comment entries across 33 distinct PRs** with 9 review entries and 25 comment entries.
- Reviewed: [openshift/hypershift #10320](https://github.com/openshift/hypershift/pull/10320), [openshift/hypershift #7097](https://github.com/openshift/hypershift/pull/7097), [openshift/hypershift #9950](https://github.com/openshift/hypershift/pull/9950), [openshift/hypershift #10315](https://github.com/openshift/hypershift/pull/10315), [openshift/hypershift #10376](https://github.com/openshift/hypershift/pull/10376), [openshift/apiserver-network-proxy #117](https://github.com/openshift/apiserver-network-proxy/pull/117), [openshift/release #86748](https://github.com/openshift/release/pull/86748), [openshift/release #86870](https://github.com/openshift/release/pull/86870), [openshift-eng/ai-helpers #871](https://github.com/openshift-eng/ai-helpers/pull/871).
- Commented: [openshift/hypershift #10047](https://github.com/openshift/hypershift/pull/10047), [openshift/hypershift #10048](https://github.com/openshift/hypershift/pull/10048), [openshift/hypershift #10086](https://github.com/openshift/hypershift/pull/10086), [openshift/hypershift #10088](https://github.com/openshift/hypershift/pull/10088), [openshift/hypershift #10119](https://github.com/openshift/hypershift/pull/10119), [openshift/hypershift #10125](https://github.com/openshift/hypershift/pull/10125), [openshift/hypershift #10162](https://github.com/openshift/hypershift/pull/10162), [openshift/hypershift #10176](https://github.com/openshift/hypershift/pull/10176), [openshift/hypershift #10225](https://github.com/openshift/hypershift/pull/10225), [openshift/hypershift #10308](https://github.com/openshift/hypershift/pull/10308), [openshift/hypershift #10311](https://github.com/openshift/hypershift/pull/10311), [openshift/hypershift #10313](https://github.com/openshift/hypershift/pull/10313), [bryan-cox/hypershift #421](https://github.com/bryan-cox/hypershift/pull/421), [openshift/hypershift #8392](https://github.com/openshift/hypershift/pull/8392), [openshift/hypershift #9227](https://github.com/openshift/hypershift/pull/9227), [openshift/hypershift #9243](https://github.com/openshift/hypershift/pull/9243), [openshift/hypershift #9512](https://github.com/openshift/hypershift/pull/9512), [openshift/hypershift #9657](https://github.com/openshift/hypershift/pull/9657), [openshift/hypershift #9658](https://github.com/openshift/hypershift/pull/9658), [openshift/hypershift #9660](https://github.com/openshift/hypershift/pull/9660), [openshift/hypershift #9787](https://github.com/openshift/hypershift/pull/9787), [openshift/hypershift #9831](https://github.com/openshift/hypershift/pull/9831), [openshift/hypershift #9835](https://github.com/openshift/hypershift/pull/9835), [openshift/hypershift #9850](https://github.com/openshift/hypershift/pull/9850).

## ⭐ Things I plan on working on next

- Check the 4.22 e2e rerun and address review feedback on [openshift/release #89277](https://github.com/openshift/release/pull/89277) for [CNTRLPLANE-5029](https://redhat.atlassian.net/browse/CNTRLPLANE-5029). Follow up on the remaining old credential mounts before retiring the old Azure CI root.
- Verify the ARO HCP presubmit rehearsal on the updated region-selection change and move [openshift/release #88591](https://github.com/openshift/release/pull/88591) toward merge for [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969).
- Get [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323) reviewed for [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) and continue the AKS v1 coverage migration under [CNTRLPLANE-3982](https://redhat.atlassian.net/browse/CNTRLPLANE-3982).

[Full, detailed status available here](https://github.com/bryan-cox/scrum-status/blob/main/2026-11-24-hypershift-scrum-status.md)
