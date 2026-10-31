<!--
name: "Data: Ultrathink availability in session initialization"
description: "Documents the ultrathink_available initialization field and how hosts interpret its value"
ccVersion: "2.1.315"
-->
@internal True when typing `ultrathink` runs the turn at xhigh effort on this frame's `model`, and when the session is already at xhigh or max, where the turn stays as it is. The terminal colors the word by this rule, and a host colors it only while this is true. After system/per_turn_effort_changed, treat this as false until the next init. Absent means unknown: a host with no answer yet colors nothing. The same answer as get_settings' applied.ultrathinkAvailable. Sent by the stream-json (Agent SDK) host.
