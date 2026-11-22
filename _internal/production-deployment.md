# Bracket Control production deployments

The merge-triggered workflow for schema-current releases was introduced in [application PR #163](https://github.com/Dev-Dyl-NZ/Bracket-App/pull/163).

The owner squash-merges the approved PR after its exact head passes the required checks. The merge starts **Deploy Production**. Review its GitHub Actions summary for the deployed revision, migration count, backup verification and health result.

The protected release operator verifies the approved merge history, exact post-merge CI, the frontend artifact and the recent database backup. For a schema-current release, it publishes Railway first, verifies the backend and then publishes the matching Cloudflare Pages artifact.

Once the migration lane has passed isolated Railway acceptance and the owner has activated it, the same workflow handles compatible additive Class A changes. An independent approver signs the exact migration batch, production target and PR source before the squash merge. The operator checks the signed recovery evidence, puts the site into maintenance, runs Bracket-Migrator, and verifies the committed ledger before deploying the matching backend and frontend. Missing approval or evidence blocks the release. An uncertain migration keeps the journal and maintenance protection in place for reconciliation.

Potentially disruptive Class B migrations require explicit approval and scheduled manual maintenance. Destructive Class C migrations require separate authorisation, verified recovery evidence and a migration-specific manual procedure.

Maintainers can find the activation and reconciliation steps in the [application runbook](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/OPERATOR-RELEASE.md), the pre-merge signature format in [signed migration approval](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/MIGRATION-APPROVAL.md) and the emergency procedure in [controlled production migrations](https://github.com/Dev-Dyl-NZ/Bracket-App/blob/main/docs/MIGRATOR-SERVICE.md).
