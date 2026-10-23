<!--
name: "Data: SDK command_lifecycle scheduled_for field"
description: "Schema description for the command_lifecycle scheduled_for field, giving the time a fired /loop wakeup was set for so a host can tell it apart from a newer pending wakeup, and why the host still needs its own time limit"
ccVersion: "2.1.307"
-->
Only beside `loop_wakeup`: the time, in epoch milliseconds, that the fired wakeup was set for; when a ScheduleWakeup call armed it, this equals the `scheduledFor` in that call's result. The fire itself can come earlier or later than that time. A host that keeps an idle session alive for a wakeup should stop waiting only when this equals the time it is waiting for: while this fire sat in the queue, a turn may have armed a newer wakeup, which is still pending. A fire that never starts (its prompt could not be prepared, the input had closed, or it was removed from the queue) sends no such frame, so the host also needs a time limit of its own past this time.
