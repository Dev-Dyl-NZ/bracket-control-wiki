# Bracket Control production deployments

The merge-triggered workflow for schema-current releases was introduced in [application PR #163](https://github.com/Dev-Dyl-NZ/Bracket-App/pull/163).

The owner squash-merges the approved PR after its exact head passes the required checks. The merge starts **Deploy Production**. Review its GitHub Actions summary for the deployed revision, migration count, backup verification and health result.

The protected release operator verifies owner squash-merge provenance, exact post-merge CI, the frontend artifact and the recent database backup. It rejects a release if the candidate history includes a direct push. The private application repository uses GitHub Free and has no native branch protection or independent application-review requirement. For a schema-current release, it publishes Railway first, verifies the backend and then publishes the matching Cloudflare Pages artifact.

The owner activated compatible additive Class A automation after an isolated Railway rehearsal executed a signed synthetic migration. Production activation verified the enabled driver and its read-only preflight. The [release of the activation revision](https://github.com/Dev-Dyl-NZ/Bracket-App/actions/runs/45103649327) applied zero migrations. For future Class A changes, the same workflow applies the independently approved batch. An independent approver signs the exact migration batch, production target and PR source before the squash merge. The operator checks the signed recovery evidence, puts the site into maintenance, runs Bracket-Migrator, and verifies the committed ledger before deploying the matching backend and frontend. Missing approval or evidence blocks the release. An uncertain migration keeps the journal and maintenance protection in place for reconciliation.

Potentially disruptive Class B migrations require explicit approval and scheduled manual maintenance. Destructive Class C migrations require separate authorisation, verified recovery evidence and a migration-specific manual procedure.

Maintainers can find the activation and reconciliation steps in the [application runbook](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/OPERATOR-RELEASE.md), the pre-merge signature format in [signed migration approval](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/MIGRATION-APPROVAL.md) and the emergency procedure in [controlled production migrations](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/MIGRATOR-SERVICE.md).
