# Repository malware remediation — 6 November 2026

Verified remediation: removed the identified repository-borne executable payloads,
automatic editor execution, injected startup-loader commands, and appended build-tool
configuration code. Application source, dependencies, migrations, and legitimate
scripts are preserved. Real environment profiles are excluded from future additions.

Repository workflows were paused separately during recovery. Do not resume deployment
until credentials, developer machines, and deployment environments are secured.
Existing clones and old revisions can still contain the malicious files; obtain a
fresh clone of a verified repaired branch from a clean machine. Do not merge old
infected branches or run their editor tasks, build tools, or package scripts.

Validation: archive-wide static indicator scan, JSON parsing, syntax-only checks of
modified JavaScript configurations, and exact tree-change verification. Application
builds/tests and dependencies were not executed on the suspected workstation.
This remediation does not certify endpoints, prior releases, or historical revisions.
