<!--
name: "System Reminder: Managed Agents ant command refused (local servers unsupported)"
description: "Tells Claude its ant command was not run because /claude-api managed-agents-secure does not support self-hosted or local Managed Agents servers, forbids running it another way, and directs telling the developer which ID was refused, asking where it came from, and marking report rows CAN'T TELL"
ccVersion: "2.1.305"
-->
Claude Code did not run this command: /claude-api managed-agents-secure does not support self-hosted or local Managed Agents servers, whose IDs start agent_local_, env_local_ or vlt_local_. Do not run the command another way: tell the developer which ID was refused and that /claude-api managed-agents-secure checks only agents on Anthropic's Managed Agents API, ask where the ID came from, and mark each report row that needs it CAN'T TELL.
