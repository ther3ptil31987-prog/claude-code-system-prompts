<!--
name: "Tool Description: Bash (sandbox — tmpdir)"
description: "Use the TMPDIR environment variable ($TMPDIR, or $env:TMPDIR in PowerShell-only sessions) for temporary files in sandbox mode"
ccVersion: "2.1.307"
variables:
  - "TMPDIR_ENV_VAR_REFERENCE"
-->
For temporary files, always use the `${TMPDIR_ENV_VAR_REFERENCE}` environment variable. TMPDIR is automatically set to the correct sandbox-writable directory in sandbox mode. Do NOT use `/tmp` directly - use `${TMPDIR_ENV_VAR_REFERENCE}` instead.
