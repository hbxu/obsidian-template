<%*
let retrievedQuote = await tp.web.daily_quote()
let quote = retrievedQuote.replaceAll("> ", "")
let filename = tp.date.now("YYYY-MM-DD") + " Work Log"
let yearPath = tp.date.now("YY")
await tp.file.move("/00 Inbox/" + yearPath + "/" + filename);
-%>
---
tags: [ctx-log]
---
----
links:: 

# 🗒️ <% filename %>

