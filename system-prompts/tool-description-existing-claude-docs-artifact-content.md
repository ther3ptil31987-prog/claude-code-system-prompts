<!--
name: "Tool Description: Existing Claude Docs artifact content"
description: "Directs updates into the Claude Docs document bound to an artifact rather than creating another document"
ccVersion: "2.1.299"
variables:
  - "ARTIFACT_ID_JSON"
  - "FORMAT_DOCS_CONTAINER_REF_FN"
  - "ARTIFACT_ID"
  - "HAS_DOCS_INSTRUCTIONS"
-->
Its content is a Claude Docs document that already exists; its Claude Docs id is this Artifact's own id, ${ARTIFACT_ID_JSON}. Read it once with the Claude Docs connector (`read`, ref {"object":"project","id":${ARTIFACT_ID_JSON}}) for its tab and root-node ids, then write into it (`batch` / `update`, ${FORMAT_DOCS_CONTAINER_REF_FN(ARTIFACT_ID)})${HAS_DOCS_INSTRUCTIONS?" as the instructions below describe":""} — do not create another; only if Claude Docs says there is no such document${HAS_DOCS_INSTRUCTIONS?", bind one as those instructions describe":" does it need one created and bound to this Artifact"}. Nothing is published to this URL for its content
