# Work Report (2026-11-24 to 2026-11-26)

*Generated from the Obsidian daily worklog using the TaskLedger status-update workflow.*

Coverage: November 24–26 inclusive, with daily notes for November 24 (full day), November 25 (a single entry) and November 26 (no work entries). The worklog's latest watermark is November 26 at 8:08 a.m. Eastern. GitHub PR states, checks and Jira status were rechecked on November 26 at 9:05 a.m. Eastern.

## 🦀 Things I've been working on

### [CNTRLPLANE-5036](https://redhat.atlassian.net/browse/CNTRLPLANE-5036) · e2e-aro-hcp-presubmit on main

- Opened [openshift/release #89370](https://github.com/openshift/release/pull/89370) and pushed the fix to auto-run the optional `e2e-aro-hcp-presubmit` on main, plus Jira priority and assignee updates. The OpenShift merge bot merged it on November 25 at 2:28 a.m. Eastern.
- The presubmit now runs automatically but still optional; making it required on main and release-4.20 through 5.2 is the remaining work under this ticket.

### [CNTRLPLANE-5029](https://redhat.atlassian.net/browse/CNTRLPLANE-5029) · Remaining Azure self-managed CI jobs

- The OpenShift merge bot merged [openshift/release #89277](https://github.com/openshift/release/pull/89277) on November 24 at 10:45 a.m. Eastern, moving the remaining Azure self-managed e2e jobs to the UK South root.
- Opened [openshift/release #89358](https://github.com/openshift/release/pull/89358) for the documentation follow-up pointing the self-managed Azure rules at the UK South root. It is **open**; the required Prow checks passed on `d6ac5e30` and `tide` is pending. `pj-rehearse` could not determine affected jobs because the branch base was stale, so it reported no rehearsal rather than a failure. jparrill has commented.

### [CNTRLPLANE-4969](https://redhat.atlassian.net/browse/CNTRLPLANE-4969) · HyperShift v2 conditions in the ARO HCP presubmit

- Iterated on the slot-manager region selection and regional weights, then reported the corrected rehearsal passing on `4e598cffd5b` with slot-manager choosing `centralus` and the v2 conditions testcase passing. Removed the hold, and the OpenShift merge bot merged [openshift/release #88591](https://github.com/openshift/release/pull/88591) on November 24 at 1:08 p.m. Eastern.
- The related payload capability change, [openshift/hypershift #10335](https://github.com/openshift/hypershift/pull/10335), is still an **open draft** on `7bf3b68f` and has not changed since November 18.

### [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851) · CAPI manager metrics over TLS

- Pushed the CAPI manager metrics work in [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323): HTTP metrics with a PodMonitor first, then reworked to serve metrics over TLS through kube-rbac-proxy, with a regenerated test fixture and a new e2e check. The PR is **open** on `5c0b2e75`; unit tests and `verify` pass, while `lint` failed and one Konflux enterprise-contract job for the control-plane-operator failed.

### [OCPSTRAT-4022](https://redhat.atlassian.net/browse/OCPSTRAT-4022) · [CNTRLPLANE-5035](https://redhat.atlassian.net/browse/CNTRLPLANE-5035) · Replace the aks-e2e presubmit with the ARO HCP v2 suite

- OCPSTRAT-4022 moved to In Progress with the 5.2 target version and its product and doc contacts filled in; CNTRLPLANE-5035 moved to In Progress. Both carry the change to make the ARO HCP presubmit required and retire the e2e-aks presubmit.

### Non-feature work / CI Infrastructure

- Closed [CNTRLPLANE-3981](https://redhat.atlassian.net/browse/CNTRLPLANE-3981) and [CNTRLPLANE-4867](https://redhat.atlassian.net/browse/CNTRLPLANE-4867); [OCPSTRAT-3557](https://redhat.atlassian.net/browse/OCPSTRAT-3557) is now Release Pending with a 5.1 fix version.
- Continued hardening the dependency auto-approver in [openshift-eng/ship-help-bot #1374](https://github.com/openshift-eng/ship-help-bot/pull/1374): the repair is published from the manager and an environment can block its own metadata server. The PR is **open** on `ab96fe80`.
- The Azure CI migration remains tracked under [OCPSTRAT-3858](https://redhat.atlassian.net/browse/OCPSTRAT-3858).
- Interviewed three candidates with Cesar.

### Code Reviews

- **1 logged review/comment entry in this window**: commented on [openshift/hypershift #9850](https://github.com/openshift/hypershift/pull/9850) (Azure private Key Vault validation through the private router), which celebdor merged on November 26.

## ⭐ Things I plan on working on next

- Make the `e2e-aro-hcp-presubmit` required on main and release-4.20 through 5.2 and retire the e2e-aks presubmit for [CNTRLPLANE-5036](https://redhat.atlassian.net/browse/CNTRLPLANE-5036), [CNTRLPLANE-5035](https://redhat.atlassian.net/browse/CNTRLPLANE-5035) and [OCPSTRAT-4022](https://redhat.atlassian.net/browse/OCPSTRAT-4022).
- Get [openshift/release #89358](https://github.com/openshift/release/pull/89358) reviewed and merged to close out the Azure CI move in [CNTRLPLANE-5029](https://redhat.atlassian.net/browse/CNTRLPLANE-5029).
- Fix the `lint` and Konflux failures on [openshift/hypershift #10323](https://github.com/openshift/hypershift/pull/10323) and get it reviewed for [OCPBUGS-140851](https://redhat.atlassian.net/browse/OCPBUGS-140851); refresh or land the [openshift/hypershift #10335](https://github.com/openshift/hypershift/pull/10335) draft.

[Full, detailed status available here](https://github.com/bryan-cox/scrum-status/blob/main/2026-11-26-hypershift-scrum-status.md)
