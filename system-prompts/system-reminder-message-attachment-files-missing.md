<!--
name: "System Reminder: Message attachment files missing"
description: "Notifies the agent that files attached to a user message could not be fetched or saved to the uploads folder, lists the affected paths when known, and says to ask the user to attach again any named upload that is not found"
ccVersion: "2.1.311"
variables:
  - "MESSAGE_FILES_MISSING_TAG"
  - "FAILED_ATTACHMENT_PATHS"
  - "ATTACHED_FILE_COUNT"
  - "IS_REPEAT_ATTEMPT"
  - "FAILED_ATTACHMENT_PATH"
  - "HTML_ESCAPE_FN"
  - "POSSIBLY_MISSING_FILE_COUNT"
  - "NO_SPACE"
  - "NO_SPACE_NOTE"
-->

<${MESSAGE_FILES_MISSING_TAG}>
${[...FAILED_ATTACHMENT_PATHS.length>0?[`${FAILED_ATTACHMENT_PATHS.length} of the ${ATTACHED_FILE_COUNT} file(s) attached to a user message could not be fetched or saved${IS_REPEAT_ATTEMPT?" again, so these paths, which the message names, may be missing":", so these paths, which the message names, were not written"}: ${FAILED_ATTACHMENT_PATHS.map((FAILED_ATTACHMENT_PATH)=>HTML_ESCAPE_FN(FAILED_ATTACHMENT_PATH.slice(1))).join(", ")}`]:[],...POSSIBLY_MISSING_FILE_COUNT>0?[`${FAILED_ATTACHMENT_PATHS.length>0?`${POSSIBLY_MISSING_FILE_COUNT} more of them may be missing too`:`${POSSIBLY_MISSING_FILE_COUNT} of the ${ATTACHED_FILE_COUNT} file(s) attached to an earlier user message may be missing from the uploads folder`}, and it is not known which. If a file that the conversation names in the uploads folder is not found, ask the user to attach it again.`]:[],...NO_SPACE?[NO_SPACE_NOTE]:[]].join(`
`)}
</${MESSAGE_FILES_MISSING_TAG}>
