# Sanitized video submitter CI snapshot

A sanitized **subset** of submitter source and isolated tests, published to validate query-only receipts and safe health diagnostics. This is not a deployment repository, release package, or the complete production workbench.

The original private repository and its history/PRs remain unchanged. This repository has a fresh history. No production copy library, audio, video, brand images, saved task box, pending record, account settings or deployment documents are included. Project labels and deployment endpoints are replaced by examples; example hosts are not service addresses. Test count contracts retain their shape.

## Tests

```
python -B tools/run_submitter_tests.py
python -B tools/test_portable_v14.py
python -B tools/test_portable_update.py
```

45 isolated submitter/contract tests, 7 portable boundary tests and 3 synthetic update/rollback tests. No real task is submitted. These fixtures do not validate a real company-to-home production batch. Public CI success does not turn a blocked private Actions job green or authorize a release.

## Behavior

Query mode only reads recorded request IDs; it never initiates an unattempted POST. Resuming an unsubmitted stage requires separate confirmation and retains the original input/IDs. Unknown results are not resent. Health diagnostics preserve whitelisted status and field differences without arbitrary response bodies or credentials.

## Scope and rights

The production workbench, voice client, copy/material data, media tools and deployment details are omitted. Source publication alone does not grant an additional license beyond applicable law. Do not deploy this example configuration to real machines.
