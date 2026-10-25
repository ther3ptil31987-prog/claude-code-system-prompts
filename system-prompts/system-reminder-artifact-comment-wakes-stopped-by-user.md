<!--
name: "System Reminder: Artifact comment wakes stopped by user"
description: "Task notification body telling Claude that the user stopped Artifact comment watches or auto-replies, listing any pending notices discarded by the stop, and saying wakes stay off until Claude Code is restarted and the artifact is published again"
ccVersion: "2.1.310"
variables:
  - "HTML_ESCAPE_FN"
  - "DISCARDED_AUTO_REACT_RECORDS"
  - "FORMAT_DISCARDED_AUTO_REACT_RECORD_FN"
  - "IS_COMMENT_WATCH_MODE"
  - "STOPPED_WATCH_COUNT"
-->

${HTML_ESCAPE_FN(DISCARDED_AUTO_REACT_RECORDS.map(FORMAT_DISCARDED_AUTO_REACT_RECORD_FN).concat([IS_COMMENT_WATCH_MODE?STOPPED_WATCH_COUNT>0?"Comments sent to Claude no longer wake this session. Wakes stay off until the user restarts Claude Code and publishes again.":"No watch was active to stop. Wakes stay off until the user restarts Claude Code and publishes again.":STOPPED_WATCH_COUNT>0?"Auto-replies are disarmed for the rest of this session (a new session re-arms on publish; a watch this session carried is ended or stays disarmed for its continuations).":"No subscription was active to stop (a new session re-arms on publish; a watch this session carried stays disarmed for its continuations)."]).join(`

`))}
