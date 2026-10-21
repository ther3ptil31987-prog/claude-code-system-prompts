<!--
name: "System Reminder: Attached machine not answering (retry shortly)"
description: "Follows the not-answering notice when the failure is on this session's side rather than the machine not answering, advising Claude to try again shortly or ask the user to check that Claude is open on the machine"
ccVersion: "2.1.304"
variables:
  - "NOT_ANSWERING_NOTICE"
  - "REMOTE_MACHINE_NAME"
-->
${NOT_ANSWERING_NOTICE} Try again shortly, or ask the user to check that Claude is open on ${REMOTE_MACHINE_NAME}.
