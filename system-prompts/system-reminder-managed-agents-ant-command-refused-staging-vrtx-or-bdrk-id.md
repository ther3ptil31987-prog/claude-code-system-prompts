<!--
name: "System Reminder: Managed Agents ant command refused (staging, vrtx or bdrk ID)"
description: "Tells Claude its ant command was not run because it holds an agent_, env_ or vlt_ ID followed by staging_, vrtx_ or bdrk_, forbids running it another way, and directs asking the developer where the ID came from and marking managed-agents-secure report rows CAN'T TELL"
ccVersion: "2.1.305"
-->
Claude Code did not run this command: it holds an ID starting agent_, env_ or vlt_ then staging_, vrtx_ or bdrk_, which `ant` commands may not use. Do not run the command another way: tell the developer which ID was refused and ask where it came from. If this is part of /claude-api managed-agents-secure, mark each report row that needs it CAN'T TELL.
