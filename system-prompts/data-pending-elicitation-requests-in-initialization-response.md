<!--
name: "Data: Pending elicitation requests in initialization response"
description: "Documents pending MCP elicitation requests returned in an initialization response and how clients handle duplicates"
ccVersion: "2.1.315"
-->
elicitation requests that this CLI process sent and that are not yet answered or withdrawn (sibling of pending_permission_requests), each as it was sent, so a client that joins after an MCP server asked can still show the question. Present (possibly empty) on a success `initialize` response when this CLI lists them, which not every session does yet; absence says nothing about what is pending. Receivers must tolerate the same request_id also arriving as a live or replayed control_request frame and render it once.
