<!--
name: "System Reminder: Attached machine not answering"
description: "Opens the notice that an attached machine is not answering and the call did not run, most often because its Claude is not connected to this session (not running, computer asleep or offline, or reconnecting after another session used it); the retry or stop-calling guidance is appended separately"
ccVersion: "2.1.304"
variables:
  - "REMOTE_MACHINE_NAME"
-->
${REMOTE_MACHINE_NAME} is not answering right now, most often because its Claude is not connected to this session (Claude is not running on ${REMOTE_MACHINE_NAME}, the computer is asleep or offline, or it is reconnecting after another session used it); the call did not run.
