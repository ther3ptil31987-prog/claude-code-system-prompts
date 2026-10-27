<!--
name: "Data: SDK UI prompt paint request schema"
description: "Documents agent-originated composer paint requests, their response and timeout behavior, and remote-session authorization"
ccVersion: "2.1.311"
-->
@internal Agent-originated: `prompt.paint` reached its core in a headless session (a plugin's `$.prompt.paint`), or a plugin that painted was unloaded (no `text`). The app sets one layer's runs over its composer and changes nothing else: not the draft, the caret or its undo history. A change of the draft drops every layer. Answers `{painted}`. Sent only to a client whose ui_attach named `ui_prompt_paint`; unanswered within 5 s, or unparsable, resolves `{isPainted: false}`; an error-shaped reply does not settle it. Over a remote session transport it is sent only while the session service states that the owner's account alone writes to the session, an answer is taken only as a client's own write, at the floor the session's policy enforces, in the owner's own session, and a client that gives no answer in 5 s hands the request to the next attached client that named it.
