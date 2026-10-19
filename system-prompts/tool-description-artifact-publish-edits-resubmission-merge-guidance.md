<!--
name: "Tool Description: Artifact publish-edits resubmission merge guidance"
description: "Provides the merge-and-refetch guidance appended when an Artifact publish carrying edits is refused because its file is unchanged since an earlier refusal, requiring the newer version's lines to be merged into the file with Edit or Write before resending"
ccVersion: "2.1.302"
variables:
  - "MERGE_TARGET_VERSION_PHRASE"
  - "PUBLISH_EDITS_RESEND_CLAUSE"
  - "REFETCH_CONFIRMATION_CLAUSE"
-->
. Merge ${MERGE_TARGET_VERSION_PHRASE} lines into your file itself with Edit or Write (${MERGE_TARGET_VERSION_PHRASE} source was handed to you, or read, in the turn that refused your publish; if neither, fetch the artifact's URL first), ${PUBLISH_EDITS_RESEND_CLAUSE}. If your file genuinely already holds everything in that version, ${REFETCH_CONFIRMATION_CLAUSE} send the publish again
