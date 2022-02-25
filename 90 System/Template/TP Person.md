<%*
let contactType = await tp.system.suggester(["Is a family member", "Is a friend", "Is a contact"], ["Family", "Friend", "Contact"]);
let noteTitle = await tp.system.prompt("Contact name, starting with a '@', e.g. @Bill Gates")
if (contactType !== "Contact") {
  await tp.file.move("/80 Person/" +contactType+"/" + noteTitle)
} else {
  await tp.file.move("/80 Person/" + noteTitle)
}
%>
<%* if (contactType == "Family" ) { %>
---
email: 
phone: 
dob: 
tags: [ctx-contact-person]
---
<%* } else { %> 
---
company: 'N/A'
email: 
phone: 
dob: 
tags: ['#person']
---
<%* } %>
# Contact details
|          |     |
| -------- | --- |
| Twitter  |     |
| LinkedIn |     |
| Facebook |     |
|          |     |

# Personal  life

# Notes

# References

# Links
[[<% contactType %>]]

