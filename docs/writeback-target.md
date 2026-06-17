# Forms Writeback Target

This document embeds a small GitHub-backed Form Contract used by authenticated
e2e runs. The form is intentionally compact because the repository itself is the
mutable part of the test: writeback checks create disposable branches and pull
requests that write JSON results under `results/`.

<Form src="../forms/writeback-target.form.yaml" />

## Test Contract

- Public anonymous review routes can render this document without mutating the
  repository.
- Authenticated submission tests can submit values through Commentary storage.
- Staging and release writeback tests can write results to a unique branch and
  open a pull request without touching stable demo repositories.

