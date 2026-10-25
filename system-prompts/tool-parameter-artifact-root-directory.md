<!--
name: "Tool Parameter: Artifact root directory"
description: "Describes the Artifact tool root parameter, a base directory for resolving relative files sources that never changes published paths, and when it may stand alone for Artifact-type artifacts"
ccVersion: "2.1.309"
variables:
  - "IS_ARTIFACT_TYPE_CREATION_ENABLED"
-->
Base directory that relative SOURCE paths resolve against (like a bundler root) — saves retyping a long build prefix. ${IS_ARTIFACT_TYPE_CREATION_ENABLED?"Never changes the published path of a `files` entry":"Never changes published paths"}. Relative to the working directory, or absolute within it or your scratchpad directory (so files fetched or built there publish without copying). Requires `files`${IS_ARTIFACT_TYPE_CREATION_ENABLED?" — except for an Artifact made from an Artifact type (or being created from one), where it may stand alone: a data `file_path` is then served at its path relative to `root`, unless a `files` map entry states its served path. Send it with every such publish, set to the folder that holds the Artifact's files at their served paths":""}.
