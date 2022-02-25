<%*
let meetingName = await tp.system.prompt("What is the name of the Meeting?")
let filename = tp.date.now("YYYY-MM-DD") + " " + meetingName + " Meeting Minutes"
let yearPath = tp.date.now("YY")
await tp.file.move("/00 Inbox/" + yearPath + "/" + filename)
-%>
---
tags: [ctx-log, to-do]
---
links:: [[<% meetingName %>]]

- [ ] Send out the meeting minutes for <% meetingName %>!

# ⏲️ <% filename %>

# Agenda

