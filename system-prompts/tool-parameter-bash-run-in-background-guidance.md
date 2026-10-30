<!--
name: "Tool Parameter: Bash run_in_background guidance"
description: "Explains Bash run_in_background behavior and that commands do not need a trailing ampersand"
ccVersion: "2.1.314"
variables:
  - "ARE_BACKGROUND_SHELLS_KEPT_ELSEWHERE_FN"
  - "BACKGROUND_TIMEOUT_NOTE_FN"
  - "BACKGROUND_SHELL_LIFETIME_NOTE_FN"
  - "BACKGROUND_PERSISTENCE_NOTE_FN"
-->
You can use the `run_in_background` parameter to run the command in the background. ${ARE_BACKGROUND_SHELLS_KEPT_ELSEWHERE_FN()?"Only use this if you don't need the result immediately; you'll be notified if it finishes while you are still working.":"Only use this if you don't need the result immediately and are OK being notified when the command completes later. You do not need to check the output right away - you'll be notified when it finishes."} You do not need to use '&' at the end of the command when using this parameter.${BACKGROUND_TIMEOUT_NOTE_FN()}${BACKGROUND_SHELL_LIFETIME_NOTE_FN()}${BACKGROUND_PERSISTENCE_NOTE_FN()}
