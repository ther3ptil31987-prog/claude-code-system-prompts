<!--
name: "Data: Self-hosted runner diff-finds-nested-repository exec path notice"
description: "Runner startup notice that, with --diff-finds-nested-repository on and sessions started through a custom exec path or command hook, the launcher must pass the runner's arguments first and start a Claude Code release at least as new as the runner"
ccVersion: "2.1.307"
variables:
  - "SESSION_EXEC_PATH"
-->
[runner] --diff-finds-nested-repository is on and sessions start through ${SESSION_EXEC_PATH}. If that is a script, it must put nothing before "$@" when it starts Claude Code (options after "$@" are fine): with an option of its own first, this option is off for the session; the session still runs, and this log then has a "[changes pane] repository not shown" line. The Claude Code it starts must be this runner's release or later; an older one exits with "unknown option '--runner-declares=…'". See "Pass every argument through" in the operator guide.
