---
<%* tp.tag = "daily/"+tp.file.title.split('-')[0]+"/"+tp.file.title.split('-')[1] %>tags: <% tp.tag %>
---
# <% tp.file.title %>

<< [[<% tp.date.now("YYYY-MMM-DD", -1, tp.file.title, "YYYY-MMM-DD") %>]] | [[<% tp.date.now("YYYY-MMM-DD", 1, tp.file.title, "YYYY-MMM-DD") %>]]>>

## Notes
<% tp.file.cursor() %>

<% tp.file.include("[[_TodosPartial]]") %>

<% tp.file.include("[[_IncomingOutgoingPartial]]") %>