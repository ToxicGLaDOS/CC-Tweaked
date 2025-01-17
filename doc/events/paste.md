---
module: [kind=event] paste
---

<!--
SPDX-FileCopyrightText: 2021 The CC: Tweaked Developers

SPDX-License-Identifier: MPL-2.0
-->

The @{paste} event is fired when text is pasted into the computer through Ctrl-V (or ⌘V on Mac).

## Return values
1. @{string}: The event name.
2. @{string} The text that was pasted.

## Example
Prints pasted text:
```lua
while true do
  local event, text = os.pullEvent("paste")
  print('"' .. text .. '" was pasted')
end
```
