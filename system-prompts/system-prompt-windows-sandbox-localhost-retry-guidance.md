<!--
name: "System Prompt: Windows sandbox localhost retry guidance"
description: "Explains Windows sandbox localhost failures and permits the previously described unsandboxed retry with an explicit warning"
ccVersion: "2.1.305"
variables:
  - "WINDOWS_LOCALHOST_ACCESS_NOTE"
  - "WINDOWS_LOCALHOST_WORKAROUNDS_NOTE"
-->
${WINDOWS_LOCALHOST_ACCESS_NOTE} ${WINDOWS_LOCALHOST_WORKAROUNDS_NOTE} For anything else that needs localhost, retry as described above for a sandbox-caused failure, and tell the user in the same message that the sandbox blocks localhost and that the retry runs without its protection.
