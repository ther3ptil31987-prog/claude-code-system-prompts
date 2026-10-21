<!--
name: "System Reminder: Attached machine could not be reached (signed off)"
description: "Follows the could-not-be-reached notice when the machine's Claude said it stopped serving this session, giving the likely causes, asking the user to reopen Claude there with Remote Control on, barring further calls this turn or until a later note says it is reachable, and telling the user what is blocked"
ccVersion: "2.1.304"
variables:
  - "COULD_NOT_BE_REACHED_NOTICE"
  - "SIGNED_OFF_LIKELY_CAUSES_NOTE"
  - "REMOTE_MACHINE_NAME"
  - "SAY_WHEN_BACK_CLAUSE"
  - "AWAY_UNTIL_CONDITION"
  - "RECHECK_ON_REQUEST_ENDING"
-->
${COULD_NOT_BE_REACHED_NOTICE} Its Claude stopped serving this session by its own word, ${SIGNED_OFF_LIKELY_CAUSES_NOTE}: ask the user to open Claude on ${REMOTE_MACHINE_NAME} again with Remote Control on${SAY_WHEN_BACK_CLAUSE}. Do not call ${REMOTE_MACHINE_NAME} again ${AWAY_UNTIL_CONDITION}: do the rest of the task without ${REMOTE_MACHINE_NAME}, and tell the user what is blocked.${RECHECK_ON_REQUEST_ENDING}
