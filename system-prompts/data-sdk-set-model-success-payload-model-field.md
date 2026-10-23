<!--
name: "Data: SDK set model success payload model field"
description: "Schema description for the internal model field on the set_model success payload, which reports the model the next turn runs spelled as in system/init, including alias resolution, plan-mode and refusal-fallback caveats, and which hosts send it"
ccVersion: "2.1.307"
-->
@internal The model the session's next turn runs as of this answer, spelled as system/init's `model`: an alias becomes the id it stands for, where external_metadata.model keeps an alias as sent. A family alias can also step down to an older version. Under opusplan or haiku in plan mode it names the model the setting runs outside plan mode, not the model a plan-mode turn sends to the API. A refusal fallback in a running turn, before or after this answer, can move the next turn to another model. `claude -p` writes it on its stream-json control channel, a Remote Control server-mode child's included, and so does a claude-code-server tenant. claude -p's Remote Control bridge lane and interactive Remote Control leave it out.
