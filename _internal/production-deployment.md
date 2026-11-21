# Bracket Control production deployments

The merge-triggered release process is prepared in [app PR](https://github.com/Dev-Dyl-NZ/Bracket-App/pull/163). Activation and live verification are pending.

Once enabled, the owner approves the exact PR in conversation and the authorised assistant squash-merges it through the owner GitHub account, or the owner squash-merges it directly. Both actions start **Deploy Production**. Review its GitHub Actions summary for the deployed revision and the health result.

The protected release operator verifies the approved merge history, exact post-merge CI, the frontend artifact and the recent database backup. It publishes Railway first, verifies the backend, then publishes Cloudflare Pages and verifies the matching production revisions. A candidate with pending schema changes stays in the separate migration procedure until an automatic migration lane is accepted.

Maintainers can find the protected operator procedure in the [application runbook](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/OPERATOR-RELEASE.md).
