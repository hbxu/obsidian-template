<%*
let retrievedQuote = await tp.web.daily_quote()
let quote = retrievedQuote.replaceAll("> ", "")
let filename = tp.date.now("YYYY-MM-DD") + " Idea"
let yearPath = tp.date.now("YY")
await tp.file.move("/00 Inbox/" + yearPath + "/" + filename);
-%>
---
tags: [ctx-log, sa-ideate]
---
links:: [[Ideas]]

# 🗒️ <% filename %>

