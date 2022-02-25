<%*
let filename = await tp.system.prompt("Provide a new name for the 'View'")
await tp.file.move("/50 View/" + filename);
-%>
---
tags: [ctx-start-here]
---

# 🟢<% filename %>

## Inbox
```dataviewjs
let currentFileLinkWithName = "[[" + dv.current().file.name + "|" + dv.current().file.name + "]]"
let folder = '"00 Inbox"'
let foundPages = dv.pages(folder).where(p => p.links == currentFileLinkWithName)
dv.list(foundPages.file.link)
```

## Ideate
```dataviewjs 
let currentFileLink = "[[" + dv.current().file.name + "]]"
let tags = ' and #sa-ideate and -#ctx-start-here'
let folders = ' and -"90 System" and -"00 Inbox"'
let from = currentFileLink + tags + folders
let foundPages = dv.pages(from)
dv.list(foundPages.file.link)
```

## Prototype
```dataviewjs 
let currentFileLink = "[[" + dv.current().file.name + "]]"
let tags = ' and #sa-prototype and -#ctx-start-here'
let folders = ' and -"90 System" and -"00 Inbox"'
let from = currentFileLink + tags + folders
let foundPages = dv.pages(from)
dv.list(foundPages.file.link)
```

## Test
```dataviewjs 
let currentFileLink = "[[" + dv.current().file.name + "]]"
let tags = ' and #sa-test and -#ctx-start-here'
let folders = ' and -"90 System" and -"00 Inbox"'
let from = currentFileLink + tags + folders
let foundPages = dv.pages(from)
dv.list(foundPages.file.link)
```

# General
```dataviewjs
let currentFileLink = "[[" + dv.current().file.name + "]]"
let tags = ' and -#ctx-start-here'
let folders = ' and -"90 System"'
let from = currentFileLink + tags + folders
let foundPages = dv.pages(from)
dv.list(foundPages.file.link)
```
