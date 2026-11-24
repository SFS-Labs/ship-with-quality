# Quality remediation notes

Findings from the first Code Quality preview on this repository:

- `src/` contains duplicated validation logic that Code Quality flags as a maintainability finding.
- Test coverage is reported for the Python and JavaScript suites and is now published to Code Quality from the test workflow.

Plan and status:

1. Collapse the duplicated validation branch into a single helper. *(open)*
2. Publish coverage from the test workflow so the coverage signal is visible on pull requests. *(done)*
3. Enforce the quality and coverage thresholds with a ruleset once the signals are stable. *(done — the ruleset targets `main`, requires the Code Quality check and a 80% coverage threshold; it was first evaluated in evaluate mode before being set to active.)*
