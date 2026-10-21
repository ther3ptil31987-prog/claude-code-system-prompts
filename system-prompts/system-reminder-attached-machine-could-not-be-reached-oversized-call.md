<!--
name: "System Reminder: Attached machine could not be reached (oversized call)"
description: "Follows the could-not-be-reached notice when the failure is on this session's side rather than the machine not answering, asking the user to check that Claude is running and still connected on the machine and noting that a call too large to deliver will not succeed on a retry"
ccVersion: "2.1.304"
variables:
  - "COULD_NOT_BE_REACHED_NOTICE"
  - "REMOTE_MACHINE_NAME"
-->
${COULD_NOT_BE_REACHED_NOTICE} If Claude is not running on ${REMOTE_MACHINE_NAME}, or is no longer connected to this session, ask the user to check it; a call that was too large to deliver will not succeed on a retry.
