<!--
name: "Data: SDK result process model-request turn count field"
description: "Documents the per-session count of earlier process turns that sent a main-conversation model request, including skipped and repeated values"
ccVersion: "2.1.311"
-->
@internal Number of earlier turns of this CLI process that sent a main-conversation model request: 0 is the process's first turn to reach the model, not the conversation's first. Turns that sent a request and then were stopped, deferred a tool or failed with an error subtype count but carry no value, so values can skip. Where one process hosts several sessions, each has its own count, from 0 each time the process starts hosting it. Present where time_to_request_phases_ms is. A worker that Anthropic hosts, with telemetry on, also sends it when a model turn ends in a result of this subtype with is_error true (an API error, a refused structured output). That result has none of the time_to_request_ or process_ fields beside it. If that turn sent no request, the value is the one its request would have had, so the next turn repeats it.
