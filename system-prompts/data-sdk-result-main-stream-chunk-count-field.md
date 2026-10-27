<!--
name: "Data: SDK result main stream chunk count field"
description: "Documents the count of runtime fetch chunks across main streams and when the count is absent"
ccVersion: "2.1.311"
-->
@internal In how many chunks the runtime's fetch handed over the bodies of those streams. It is not the number of socket reads, several of which can make one chunk. Against main_stream_event_count it shows how the API's events arrive grouped, though the two do not divide evenly: a chunk can end inside an event, keepalive comments and pings are chunks that bring no event, and a stream that failed or was aborted can count one chunk whose events were never read. Absent, never 0, when a stream's chunks were not counted, as on Bedrock, Vertex, Foundry and Mantle, with the byte watchdog off, or for a stream still open when this result is built.
