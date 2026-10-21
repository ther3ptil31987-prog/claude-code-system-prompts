<!--
name: "System Reminder: Managed Agents ant command refused (altered --transform command)"
description: "Tells Claude its ant command was not run because it carries a --transform from the /claude-api managed-agents-secure instructions without being that command exactly as written, and to run each such command alone and verbatim, asking the developer and marking report rows CAN'T TELL when an ID or version has another form"
ccVersion: "2.1.305"
-->
Claude Code did not run this command: it holds a --transform from the /claude-api managed-agents-secure instructions but is not that `ant` command as written. Run each of those commands alone and exactly as written, with each ID typed inside its single quotes (agent_, env_ or vlt_, then only letters and digits). Add --version only to `ant beta:agents retrieve`, as a whole number with no leading zero. If an ID or version read from the account has another form, do not run the command: ask the developer about it, and mark each report row that needs it CAN'T TELL.
