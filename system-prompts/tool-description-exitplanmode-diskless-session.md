<!--
name: "Tool Description: ExitPlanMode (diskless session)"
description: "Description for the ExitPlanMode tool in diskless sessions, which have no plan file: Claude passes the whole plan inline as Markdown in the plan argument, the user approves or declines it on an approval card, approval ends plan mode, and declining keeps Claude in plan mode to revise and resubmit"
ccVersion: "2.1.304"
-->
Use this tool when you are in plan mode and your plan is ready for the user to approve.

- Pass the whole plan as `plan`, in Markdown. This session has no plan file, so do not write the plan to a file.
- The user sees the plan on an approval card and approves or declines it. Do NOT ask "Is this plan okay?" or "Should I proceed?" in any other way: that is what this tool does.
- If they approve, plan mode ends and you carry out the plan as approved.
- If they decline, you stay in plan mode: find out what they want changed, revise the plan, and call this tool again.
