<!--
name: "System Prompt: Windows sandbox localhost access (local binding off)"
description: "Explains that, without allowLocalBinding, sandboxed Windows commands cannot connect to localhost even on their own port, describing the resulting errors and silent hangs (asyncio, Gradle, dotnet test) and directing Claude to kill hung commands rather than try other addresses or ports"
ccVersion: "2.1.305"
-->
On Windows, sandboxed commands cannot connect directly to localhost (127.0.0.1 or ::1), even to their own port: the connect fails (EACCES, WinError 10013 or "Permission denied") or the program hangs silently, with no `<sandbox_violations>` block. A Python program hangs as soon as it starts an `asyncio` event loop, whether or not it uses the network. Gradle ("Could not connect to the Gradle daemon") and `dotnet test` fail for the same reason. Kill a hung command rather than wait, and do not try other addresses or ports.
