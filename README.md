# Sample AAP repository

This small, safe fixture is intended for testing the AAP APME EAP workflow. It
contains no production hosts, credentials, customer data, or network-dependent
tasks.

## Suggested demo flow

1. Connect the repository to APME using the default branch.
2. Run a scan and review the findings in `site.yml` and the web role.
3. Select the use of a hard-coded package version and the missing task tags as
   remediation candidates.
4. Generate a proposed branch and pull request, then review the diff before
   merging.

The two intentional findings are marked with `# APME-DEMO-FINDING` comments.
The remaining files provide enough context for repository health, inventory,
role structure, and dependency review without requiring an AAP controller.

## Safety

The inventory uses `localhost` with a local connection. Do not replace it with
production hosts or add secrets to this fixture.

## Additional remediation fixtures

The `fixtures/` directory contains isolated examples for comparing APME
remediation behavior:

- `manual-lint-examples.yml` contains common lint findings that generally need
  human review.
- `aap-modernization-candidates.yml` contains AAP endpoint and template-ID
  patterns intended to exercise modernization rules.

These files use example-only hosts and URLs; they are not intended to run.
