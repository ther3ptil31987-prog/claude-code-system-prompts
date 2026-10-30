<!--
name: "Tool Parameter: PowerShell run_in_background note"
description: "Explains PowerShell background completion notices and warns stopping-session users to wait for needed results before replying"
ccVersion: "2.1.314"
variables:
  - "DOES_SESSION_STOP_AFTER_REPLY_FN"
  - "BACKGROUND_TIMEOUT_NOTE_FN"
-->
  - You can use the `run_in_background` parameter to run the command in the background. ${DOES_SESSION_STOP_AFTER_REPLY_FN()?"Only use this if you don't need the result immediately; you'll be notified if it finishes while you are still working. After your reply you may not be told when it ends, and a few minutes later it is likely stopped, so if you need its result, wait for it before you reply.":"Only use this if you don't need the result immediately and are OK being notified when the command completes later. You do not need to check the output right away - you'll be notified when it finishes."}${BACKGROUND_TIMEOUT_NOTE_FN()}
