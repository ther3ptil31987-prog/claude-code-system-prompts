<!--
name: "Tool Description: Project local_file read-only workflow"
description: "Explains that local_file is read-only, including long-line workarounds, and how to save changes through a new working file"
ccVersion: "2.1.311"
variables:
  - "HAS_LONG_LINES"
  - "READ_TOOL_NAME"
  - "GREP_TOOL_NAME"
  - "BASH_TOOL_NAME"
  - "CONTENT_SEARCH_TOOL_OR_COMMAND"
-->
local_file is for reading only${HAS_LONG_LINES?`. One of its lines is too long for ${READ_TOOL_NAME} to page through, because ${READ_TOOL_NAME}'s offset and limit count lines. ${READ_TOOL_NAME} with no offset or limit gives only the first part of the file. ${READ_TOOL_NAME} with an offset and limit gives whole lines, or an error if those lines do not fit. The file is too large for project_read to return inline. ${GREP_TOOL_NAME} shows a line or a match of over 500 characters as [Omitted long matching line]. With output_mode `content`, `-o` true and a pattern such as `.{0,200}term.{0,200}`, ${GREP_TOOL_NAME} shows each match of term with up to 200 characters on each side. In ${BASH_TOOL_NAME}, `grep -ob 'term' /path/of/local_file | head` gives the byte offset of each match of term, counted from 0. `tail -c +START /path/of/local_file | head -c 20000` gives 20000 bytes from byte START, counted from 1: START is an offset plus 1, or any number from 1 to size_bytes.`:`: read the parts you need with ${READ_TOOL_NAME}'s offset and limit, or search it with ${CONTENT_SEARCH_TOOL_OR_COMMAND}.`} Edits to ${HAS_LONG_LINES?"local_file":"it"} never reach the project, and project_write rejects it as local_path. To change the document or make a file from it, run `cat /path/of/local_file > new-name` in the working directory, where new-name is a name that no file there has, and work on that file. To save a change, call project_write with the document's path and that file as local_path. If the document is an upload such as a PDF, that saves a new text document and leaves the upload as it is.
