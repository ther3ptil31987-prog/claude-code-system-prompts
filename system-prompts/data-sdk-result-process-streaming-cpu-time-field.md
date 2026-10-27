<!--
name: "Data: SDK result process streaming CPU time field"
description: "Documents process CPU time during main-response streaming and when cloud workers report it"
ccVersion: "2.1.311"
-->
@internal CPU time, counted as in process_cpu_ms_between_turns, that the process used inside process_wall_ms_streaming. It is part of process_cpu_ms_turn. It holds what handling the streamed replies cost while they streamed, but not what the CLI does with a reply once its stream has ended. It also holds whatever else the process did meanwhile, such as a tool that starts before the reply ends, a subagent, a side request, telemetry or garbage collection. It always comes with process_wall_ms_streaming, main_stream_count and main_stream_event_count; main_stream_chunk_count can be missing. Sent only by the workers named under process_rss_mib_turn_start. On them it is present where process_cpu_ms_turn is, if a stream opened on the turn and each of its windows could be measured.
