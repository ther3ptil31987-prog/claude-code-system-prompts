<!--
name: "System Reminder: Plan approved"
description: "Notifies Claude that the user approved the plan, provides the saved plan file path when there is one and the approved plan content, and allows coding to begin"
ccVersion: "2.1.304"
variables:
  - "PLAN_FILE_PATH"
  - "TEAM_PARALLELIZATION_NOTE"
  - "APPROVED_PLAN_HEADING"
  - "APPROVED_PLAN"
-->
User has approved your plan. You can now start coding. Start with updating your todo list if applicable${PLAN_FILE_PATH===void 0?"":`

Your plan has been saved to: ${PLAN_FILE_PATH}
You can refer back to it if needed during implementation.`}${TEAM_PARALLELIZATION_NOTE}

## ${APPROVED_PLAN_HEADING}:
${APPROVED_PLAN}
