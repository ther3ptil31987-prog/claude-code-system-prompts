<!--
name: "System Prompt: Windows sandbox localhost access (local binding on)"
description: "States that, with allowLocalBinding on, sandboxed Windows commands can reach localhost on every port except the one the sandbox reserves, while anything off the machine still goes through the sandbox proxy and allowedDomains"
ccVersion: "2.1.305"
variables:
  - "SANDBOX_FENCE_CHECK_PORT"
-->
On Windows, sandboxed commands can connect to localhost (127.0.0.1 or ::1) on any port except ${SANDBOX_FENCE_CHECK_PORT}. Nothing off this machine is reachable directly; that goes through the sandbox proxy and `sandbox.network.allowedDomains`.
