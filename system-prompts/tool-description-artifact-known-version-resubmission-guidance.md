<!--
name: "Tool Description: Artifact known-version resubmission guidance"
description: "Provides the merge-and-refetch guidance appended to an identical-content Artifact publish refusal, naming either the live version's source or a known newer version's source"
ccVersion: "2.1.302"
variables:
  - "MERGE_TARGET_VERSION_PHRASE"
  - "REFETCH_CONFIRMATION_CLAUSE"
-->
. Merge your edits onto ${MERGE_TARGET_VERSION_PHRASE} source (handed to you or read in the turn that refused this content; if neither, fetch the artifact's URL first) and publish the merged result. If your content genuinely already includes that version's changes, ${REFETCH_CONFIRMATION_CLAUSE} publish again
